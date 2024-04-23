<link rel="stylesheet" href="style.css">
<nav>
    <ul>
        <li><a href="#">Database Design</a>
            <ul>
                <li><a href="#">ER Model</a></li>
                <li><a href="#">Normalization</a></li>
                <li><a href="#">SQL Query</a></li>
            </ul>
        </li>
        <li><a href="#">Covid Cases</a></li>
        <li><a href="#">GDP</a></li>
        <li><a href="#">Temperature</a></li>
        <li><a href="#">Vaccines</a></li>
        <li><a href="#">Other Visualization</a></li>
    </ul>
</nav>



# <span style="background-color: yellow;">Database Design</span>
Link: [ER Model](http://baidu.com "Link to ER Model") | [Normalization](http://baidu.com "Link to Normalization") | [SQL Query](http://baidu.com "Link to SQL Query")

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

*Primary key*: (Country, Year, Month)

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
				
