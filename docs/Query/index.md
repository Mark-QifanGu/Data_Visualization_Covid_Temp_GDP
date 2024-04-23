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
        <li><a href="//Data_Visualization_Covid_Temp_GDPTemp/">Temperature</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Vac/">Vaccines</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Visual/">Other Visualization</a></li>
    </ul>
</nav>



# <span style="background-color: yellow;">SQL Query</span>

## 1.Extract Covid-19 Case Trends for Specific Countries

```sql
SELECT * FROM Covid_Data WHERE Country = 'China' ORDER BY Year, Month;
```
<img src="https://raw.githubusercontent.com/Mark-QifanGu/Data_Visualization_Covid_Temp_GDP/main/images/2NF.png" width="90%" alt="Normalization 2NF">

