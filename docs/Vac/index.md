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
        <li><a href="//Data_Visualization_Covid_Temp_GDP/Temp/">Temperature</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Vac/">Vaccines</a></li>
        <li><a href="/Data_Visualization_Covid_Temp_GDP/Visual/">Other Visualization</a></li>
    </ul>
</nav>



# <span style="background-color: yellow;">Vaccinations</span>

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
