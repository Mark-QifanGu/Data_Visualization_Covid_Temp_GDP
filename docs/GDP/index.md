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



# <span style="background-color: yellow;">Economic and GDP</span>

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
