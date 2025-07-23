<link rel="stylesheet" href="style.css">
<nav>
    <ul>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/">Database Design</a>
            <ul>
                <li><a href="/Data_Visualization_Covid_Temp_GDP/ER/">ER Model</a></li>
                <li><a href="/Data_Visualization_Covid_Temp_GDP/Norm/">Normalization</a></li>
                <li><a href="/Data_Visualization_Covid_Temp_GDP/Query/">SQL Query</a></li>
            </ul>
        </li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Cases/">Covid Cases</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/GDP/">GDP</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Temp/">Temperature</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Vac/">Vaccines</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Visual/">Other Visualization</a></li>
    </ul>
</nav>



# <span style="background-color: yellow;">SQL Query</span>

## 1.Extract Covid-19 Case Trends for Specific Countries

```sql
SELECT * FROM Covid_Data WHERE Country = 'China' ORDER BY Year, Month;
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S1.png" width="90%" alt="SQL Query result 1">

```sql
SELECT * FROM Covid_Data WHERE Country = 'USA' ORDER BY Year, Month;
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S2.png" width="90%" alt="SQL Query result 2">


## 2.Join Economic Data with Health Data to Analyze Correlations

```sql
SELECT e.*, c.CumulativeTotalCases, c.CumulativeTotalDeaths
FROM Economic_Data e
JOIN Covid_Data c ON e.Country = c.Country AND e.Year = c.Year
WHERE e.Country = 'China';
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S3.png" width="90%" alt="SQL Query result 3">

<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S4.png" width="90%" alt="SQL Query result 4">

```sql
SELECT e.Year, e.GDP, e.Unemployment, c.CumulativeTotalCases, c.CumulativeTotalDeaths
FROM Economic_Data e
JOIN Covid_Data c ON e.Country = c.Country AND e.Year = c.Year
WHERE e.Country = 'China'
ORDER BY e.Year;
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S5.png" width="90%" alt="SQL Query result 5">


## 3.Connect Covid-19 Case Data with Temperature Data

```sql
SELECT c.*, t.AvgTemperature
FROM Covid_Data c
JOIN Temperature_Data t ON c.Country = t.Country AND c.Year = t.Year AND c.Month = t.Month
WHERE c.Country = 'China';
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S6.png" width="90%" alt="SQL Query result 6">


```sql
SELECT c.*, t.AvgTemperature
FROM Covid_Data c
JOIN Temperature_Data t ON c.Country = t.Country AND c.Year = t.Year AND c.Month = t.Month
WHERE c.Country = 'India';
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S7.png" width="90%" alt="SQL Query result 7">


## 4.Connect Covid-19 Cases with Economic Data

```sql
SELECT c.*, e.GDP, e.Unemployment
FROM Covid_Data c
JOIN Economic_Data e ON c.Country = e.Country AND c.Year = e.Year
WHERE c.Country = 'China';
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S8.png" width="90%" alt="SQL Query result 8">

```sql
SELECT c.*, e.GDP, e.Unemployment
FROM Covid_Data c
JOIN Economic_Data e ON c.Country = e.Country AND c.Year = e.Year
WHERE c.Country = 'India';
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/S9.png" width="90%" alt="SQL Query result 9">


## 5.Create Index and View

```sql
CREATE INDEX idx_monthly_new_cases ON Covid_Data(MonthlyNewCases);
CREATE VIEW View_Covid_Monthly_Summary AS
SELECT 
  Country, 
  Year, 
  Month, 
  CumulativeTotalCases, 
  MonthlyNewCases
FROM Covid_Data;
```
<br>

```sql
CREATE INDEX idx_gdp_year ON Economic_Data(GDP, Year);
CREATE VIEW View_Economic_Indicators AS
SELECT 
  Country, 
  Year, 
  GDP, 
  InflationRate, 
  Unemployment
FROM Economic_Data;
```
<br>

```sql
CREATE INDEX idx_temperature_year_month ON Temperature_Data(Year, Month);
CREATE VIEW View_Avg_Temperature AS
SELECT 
  AreaCode, 
  Country, 
  Year, 
  Month, 
  AVG(AvgTemperature) AS MonthlyAvgTemperature
FROM Temperature_Data
GROUP BY AreaCode, Country, Year, Month;
```
<br>

```sql
CREATE INDEX idx_fully_vaccinated ON Vaccination_Data(PeopleFullyVaccinated);
CREATE VIEW View_Vaccination_Progress AS
SELECT 
  Country, 
  Year, 
  Month, 
  PeopleVaccinated, 
  PeopleFullyVaccinated
FROM Vaccination_Data;
```
<br>

### To verify index:
```sql
SHOW INDEX FROM Covid_Data;
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/index.png" width="90%" alt="index">

### To verify views:
```sql
DESCRIBE View_Covid_Monthly_Summary; 
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/view.png" width="90%" alt="view">

