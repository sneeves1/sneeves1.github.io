# Fruit and the City: Measuring the Accuracy of Public Science

# Abstract
Participatory science, also known as citizen science, is defined as the collection and analysis of data by members of the general public. Participatory science can be a valued method for researchers as it allows for mass data collection. Without participatory science, data may be overly expensive or impossible to obtain. Participatory science data collection can produce biased or inaccurate data if participants are not educated in the subject matter, there is not a wide variety of participants, or if there is not sufficient spatial coverage of data. This presentation analyzes the spatial patterns of the data to detect spatial biases along lines of income and race/ethnicity. Early findings of this exploratory study has produced metrics to analyze bias of the Falling Fruit database across Baltimore, Maryland; Portland, Oregon; and Philadelphia, PA. Falling Fruit is a non-profit organization containing an interactive tree inventory of urban fruit trees. The aim of this project is to promote foraging in urban environments. 

# Methods
For the methods of this study, tree inventories for the 200 largest cities/metropolitan areas within the United States were researched and collected if data was available. Only about 15-20 city tree inventories were collected. Tree inventories are databases created typically by city governments to keep record of trees around their cities. Inventories typically keep records of tree attributes such as species, size, conditions, and where the can be found within the city. The entire Falling Fruit database was collected as well. After tree data was collected, census data was also collected through the use of RStudio and a package made for R called tidycensus and tigris. Data collected from the census included retrieving shapefiles for: city boundaries, county census tracts (which were later clipped to the extent of the city boundaries), water features, and census tract data for median household income, and race/ethnicity in 2020. The city tree inventories were filtered for tree species that produced edible fruit, and a new inventory of edible fruit tree species was crreated to compare to the Falling Fruit inventory for each city. The percentage of capture rate of Falling Fruit was calculated by dividing the Falling Fruit data by the city fruit tree inventory. The statistics of the capture rate of Falling Fruit trees was caclulated to gather a median value across the city. A new column that labeled the tracts as above or below the city median was created, and maps were visualized to shoe the capture rate median against BIPOC percent and median household income.

# Results
R markdowns for each city can be found [here.](scripts.md)
<br><br/>
<img src="Baltimore_Median.png?raw=true"/> Fig. 1: The left map compares census tract capture rate against the median capture rate city-wide in Baltimore, Maryland. The map on the right displays the percent Black Indiginous People of Color (BIPOC) per census tract. The two maps together show a comparison of capture rate median against BIPOC population percentages.
<br><br/>

<img src="Baltimore_mhhi.png?raw=true"/> Fig. 2: The left map compares census tract capture rate against the median capture rate city-wide in Baltimore, Maryland. The map on the right displays the median household income per census tract. The two maps together show a comparison of capture rate median against median household income.
<br><br/>

<img src="Portland_Median.png?raw=true"/> Fig. 3: The left map compares census tract capture rate against the median capture rate city-wide in Portland, Oregon. The map on the right displays the percent Black Indiginous People of Color (BIPOC) per census tract. The two maps together show a comparison of capture rate median against BIPOC population percentages.
<br><br/>

<img src="Portland_mhhi.png?raw=true"/> Fig. 4: The left map compares census tract capture rate against the median capture rate city-wide in Portland, Oregon. The map on the right displays the median household income per census tract. The two maps together show a comparison of capture rate median against median household income.
<br><br/>

<img src="Philly_Median.png?raw=true"/> Fig. 5: The left map compares census tract capture rate against the median capture rate city-wide in Philadelphia, Pennsylvania. The map on the right displays the percent Black Indiginous People of Color (BIPOC) per census tract. The two maps together show a comparison of capture rate median against BIPOC population percentages.
<br><br/>

<img src="philly_mhhi.png?raw=true"/>Fig. 6: The left map compares census tract capture rate against the median capture rate city-wide in Philadelphia, Pennsylvania. The map on the right displays the median household income per census tract. The two maps together show a comparison of capture rate median against median household income.
<br><br/>


<table>

<tr>

<th>Above/Below City-Wide Median</th>

<th>Portland BIPOC</th>

<th>Baltimore BIPOC</th>

<th>Philadelphia BIPOC</th>

</tr>

<tr>

<td>No Fruit Trees</td>

<td>12.0%</td>

<td>96.2%</td>

<td>No Data</td>

</tr>

<tr>

<td>Below</td>

<td>32.8%</td>

<td>80.7%</td>
  
<td>65.0%</td>

</tr>

<tr>

<td>Above</td>

<td>25.6%</td>

<td>57.4%</td>

<td>59.4%</td>

</tr>

</table>
Table 1: This table shows the average percent BIPOC popultation for each category shown on the capture rate median map for the cities of Baltimore, MD; Portland, OR; and Philadelphia, PA.

<table>

<tr>

<th>Above/Below City-Wide Median</th>

<th>Portland BIPOC</th>

<th>Baltimore BIPOC</th>

<th>Philadelphia BIPOC</th>

</tr>

<tr>

<td>No Fruit Trees</td>

<td>$105,889</td>

<td>$37,591</td>

<td>No Data</td>

</tr>

<tr>

<td>Below</td>

<td>$72,956</td>

<td>$46,884</td>

<td>$43,025</td>

</tr>

<tr>

<td>Above</td>

<td>$82,496</td>

<td>$70,480</td>

<td>$60,431</td>

</tr>

</table>
Table 2: This table shows the average median household income for each category shown on the capture rate median map for the cities of Baltimore, MD; Portland, OR; and Philadelphia, PA.

# Conclusion
After looking at the data, a trend across the three cities show that areas that have a Falling Fruit capture rate that were higher than the city-wide median capture tend to have a higher median household income, and lower BIPOC population percentages. One exception to this trend is the areas with no fruit tree data in Philadelphia. Both categories had no census data to work with so it can be assumed that no one lives in these census tracts. Along with no data from the census, aerial photography shows that these areas with no fruit tree data also happen to be areas for industrial purposes, so it would be safe to assume that no one lives in these areas. Another exception to this trend is the No fruit Trees average for Portland. There was one census tract that had no fruit trees collected by the Portland city government, so there was no data to go off of. There were Falling Fruit entries in this area, but no fruit tree inventory data. This could mean that this census tract is an area that has not been recorded by the city government of Portland, and will most likely skew the data table in this way. 
Because this study is an ongoing study and this presentation only displays early findings, the next steps are to look at data from other cities that fall within the largest 200 cities in the United States. So far, tree inventories from about 15 other cities have been collected for furthur study.
