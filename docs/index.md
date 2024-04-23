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
### - *Covid Cases*:

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


### - *Economic*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  |                                                                               |
| Continent                |                                                                               |
| Year                     |                                                                               |
| Population               |                                                                               |
| Land                     |                                                                               |
| PopulationDensity        |                                                                               |
| AgriculturePer           |                                                                               |
| ExportPer                |                                                                               |
| ImportPer                |                                                                               |
| IndustryPer              |                                                                               |
| HealthExpenditurePer     |                                                                               |
| EducationExpenditurePer  |                                                                               |
| ServicePer               |                                                                               |
| GDP                      |                                                                               |
| InflationRate            |                                                                               |
| Unemployment             |                                                                               |

*Primary key*: (Country, Year)

Original dataset: https://www.kaggle.com/datasets/yusufglcan/country-data


- ### *Temperature*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| AreaCode                 |                                                                               |
| Country                  |                                                                               |
| Year                     |                                                                               |
| Month                    |                                                                               |
| AvgTemperature           |                                                                               |

*Primary key*: (Country, Year, Month)

Original dataset: https://www.fao.org/faostat/en/#data/ET/metadata
Reference:
https://data.giss.nasa.gov/gistemp/
https://www.columbia.edu/~mhs119/Temperature/
https://earthobservatory.nasa.gov/world-of-change/global-temperatures
https://www.kaggle.com/datasets/gauravduttakiit/global-temperature?select=GlobalLandTemperaturesByCountry.csv


### - *Vaccines*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  |                                                                                 |
| Year                     |                                                                                 |
| Month                    |                                                                                 |
| PeopleVaccinated         |                                                                                 |
| PeopleFullyVaccinated    |                                                                                 |
| MonthlyVaccinations      |                                                                                 |
| PeopleVacPerHundred      |                                                                                 |
| PeopleFullyVacPerHundred |                                                                                 |

*Primary key*: (Country, Year, Month)
				
Original dataset: https://www.kaggle.com/datasets/gpreda/covid-world-vaccination-progress?resource=download

Country location: https://www.kaggle.com/datasets/paultimothymooney/latitude-and-longitude-for-every-country-and-state
