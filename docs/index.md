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

Country location: https://www.kaggle.com/datasets/paultimothymooney/latitude-and-longitude-for-every-country-and-state
