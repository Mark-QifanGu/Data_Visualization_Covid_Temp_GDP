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
- *Covid Cases*:

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| Country                  |                                                                               |
| Year                     |                                                                               |
| Month                    |                                                                               |
| CumulativeTotalCases     |                                                                               |
| MonthlyNewCases          |                                                                               |
| ActiveCases              |                                                                               |
| CumulativeTotalDeaths    |                                                                               |
| MonthlyNewDeaths         |                                                                               |

*Primary key*: (Country, Year, Month)

- *GDP*：

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

- *Temperature*：

| Attributes               | Explanation                                                                     |
| :----------------------- | :------------------------------------------------------------------------------ |
| AreaCode                 |                                                                               |
| Country                  |                                                                               |
| Year                     |                                                                               |
| Month                    |                                                                               |
| AvgTemperature           |                                                                               |

*Primary key*: (Country, Year, Month)

- *Vaccines*：

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
				
