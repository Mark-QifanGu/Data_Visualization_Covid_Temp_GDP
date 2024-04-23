<link rel="stylesheet" href="style.css">
<nav>
    <ul>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/docs/">Database Design</a>
            <ul>
                <li><a href="/ER/index.md">ER Model</a></li>
                <li><a href="/Norm/index.md">Normalization</a></li>
                <li><a href="/Query/index.md">SQL Query</a></li>
            </ul>
        </li>
        <li><a href="/Cases/index.md">Covid Cases</a></li>
        <li><a href="/GDP/index.md">GDP</a></li>
        <li><a href="/Temp/index.md">Temperature</a></li>
        <li><a href="/Vac/index.md">Vaccines</a></li>
        <li><a href="/Visual/index.md">Other Visualization</a></li>
    </ul>
</nav>



# <span style="background-color: yellow;">Database Design</span>
Link: [ER Model](ER/ "Link to ER Model") | [Normalization](../Norm/index.md "Link to Normalization") | [SQL Query](../Query/index.md "Link to SQL Query")

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
				
