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



# <span style="background-color: yellow;">Database Design</span>
Link: [ER Model](ER/ "Link to ER Model") | [Normalization](Norm/ "Link to Normalization") | [SQL Query](Query/ "Link to SQL Query")

## Overview of the Datasets:
- ### *Covid Cases*:

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  | Designates the Country in which the the row's data was observed.              |
| Year                     | Designates the year of observation of the row's data.                         |
| Month                    | Designates the month of observation of the row's data.                        |
| CumulativeTotalCases     | Designates the cumulative number of confirmed cases as of the row's month, for the row's country.|
| MonthlyNewCases          | Designates the monthly new number of confirmed cases on the row's date, for the row's country.|
| ActiveCases              | Designates the number of active cases (i.e., confirmed cases that still didn't recover nor die) on the row's date, for the row's country.|
| CumulativeTotalDeaths    | Designates the cumulative number of confirmed deaths as of the row's month, for the row's country.|
| MonthlyNewDeaths         | Designates the monthly new number of confirmed deaths on the row's month, for the row's country.|

*Primary key*: (Country, Year, Month)

Original dataset: https://www.kaggle.com/datasets/josephassaker/covid19-global-dataset


- ### *Economic*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  | The country of the data row                                                     |
| Continent                | The continent of the country                                                    |
| Year                     | The year of the data row.                                                       |
| Population               | The total population of a country reflects its size and demographic composition.|
| Land                     | The area of land.                                                             |
| PopulationDensity        | Population density measures the number of individuals living per unit of area, providing insights into urbanization and land usage.|
| AgriculturePer           | This metric measures the contribution of the agricultural sector to a nation's economy.|
| ExportPer                | Export as a percentage of GDP illustrates a country's global trade competitiveness and its reliance on international markets.|
| ImportPer                | Import as a percentage of GDP demonstrates a country's dependence on foreign goods and services.|
| IndustryPer              | Industrial activities as a percentage of GDP signify the role of manufacturing and industry in a country's economy.|
| HealthExpenditurePer     | This metric reflects the proportion of a country's GDP allocated to healthcare, highlighting its commitment to public health.|
| EducationExpenditurePer  | The percentage of GDP spent on education signifies a nation's investment in its human capital and future workforce.|
| ServicePer               | The service sector's percentage of GDP shows the importance of services in economic activities.|
| GDP                      | GDP measures the total economic output of a country, reflecting its economic health and performance.|
| InflationRate            | The inflation rate indicates the rate at which the general price level of goods and services rises, affecting a country's purchasing power.|
| Unemployment             | The unemployment number of the country for that year.                         |

*Primary key*: (Country, Year)

Original dataset: https://www.kaggle.com/datasets/yusufglcan/country-data


- ### *Temperature*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| AreaCode                 | An areacode for each country.                                                 |
| Country                  | The country name for the row of data.                                         |
| Year                     | The year for the row of data.                                                 |
| Month                    | The month for the row of data.                                                |
| AvgTemperature           | The average temperature for the country in that month.                        |

*Primary key*: (Country, Year, Month)<br>
Original dataset: https://www.fao.org/faostat/en/#data/ET/metadata<br>
Reference:<br>
https://data.giss.nasa.gov/gistemp/<br>
https://www.columbia.edu/~mhs119/Temperature/<br>
https://earthobservatory.nasa.gov/world-of-change/global-temperatures<br>
https://www.kaggle.com/datasets/gauravduttakiit/global-temperature?select=GlobalLandTemperaturesByCountry.csv<br>

(Notice: We used the monthly average temperature difference plus the standard baseline monthly average temperature for 2012, which come from two datasets. Therefore, there might be mismatches in the country names, such as one dataset using 'USA' and another using 'United States of America'. In this case, we simply used the method of an inner join.)

- ### *Vaccines*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  | This is the country for which the vaccination information is provided.         |
| Year                     | Year for the data entry.                                                       |
| Month                    | Month for the data entry.                                                      |
| PeopleVaccinated         | A person, depending on the immunization scheme, will receive one or more (typically 2) vaccines; at a certain moment, the number of vaccination might be larger than the number of people.|
| PeopleFullyVaccinated    | This is the number of people that received the entire set of immunization according to the immunization scheme (typically 2); at a certain moment in time, there might be a certain number of people that received one vaccine and another number (smaller) of people that received all vaccines in the scheme.|
| MonthlyVaccinations      | For a certain month, the number of vaccination for that date/country           |
| PeopleVacPerHundred      | Ratio (in percent) between population immunized and total population up to the date in the country.|
| PeopleFullyVacPerHundred | Ratio (in percent) between population fully immunized and total population up to the date in the country.|

*Primary key*: (Country, Year, Month)
				
Original dataset: https://www.kaggle.com/datasets/gpreda/covid-world-vaccination-progress?resource=download

- ### *Country location*: https://www.kaggle.com/datasets/paultimothymooney/latitude-and-longitude-for-every-country-and-state
