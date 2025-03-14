# GGIS407 Project: Relationship between broadband accessibility and socioeconomic factors

## Project Overview
Broadband connectivity is widely recognized as an important infrastructure that supports education, economic development, telehealth, and civic participation. Due to rapid innovations, broadband technologies have developed from 3G and 4G to 5G, which now offers transformative speed to perform more challenging tasks such as autonomous driving, augmented/virtual reality, etc. Despite steady national improvements in broadband adoption, significant disparities exist along socioeconomic lines. <br><br>
Therefore, this project aims to study how 5G mobile broadband accessibility varies across the U.S. in relation to key socioeconomic factors including income, education level, and population density, in order to better understand the digital divide. It integrates 5G coverage data from FCC National Broadband Map with demographic and socioeconomic datasets from American Community Survey to identify areas where advanced broadband services are lacking and analyze the implications for social and economic equity. The analysis is conducted on a county level because of data availability and the amount of details it provides with an area unit smaller than the states. <br><br>
To set up a clear direction for the project, here are the questions that I aim to answer and my hypotheses:
1. <b>Question</b>: How does high-speed broadband coverage correlate with median income? <br/>
   <b>Hypothesis</b>: High-speed broadband coverage is highly and positively correlated with median income in a county.

2. <b>Question</b>: What is the relationship between education attainment and high-speed broadband coverage? <br/>
   <b>Hypothesis</b>: The higher the education attained by the population in a county, the higher the percentage of high-speed broadband coverage.
   
3. <b>Question</b>: Is there a correlation population density and broadband coverage? <br/>
   <b>Hypothesis</b>: Yes, population density in a county is highly and positively correlated with broadband coverage.

## Data source
- FCC National Broadband Map, https://broadbandmap.fcc.gov/data-download/nationwide-data?version=jun2024
- United States Census Bureau (American Community Survey), https://data.census.gov/table
    - Table DP05 ACS Demographic and Housing Estimates
    - Table S1501 Educational Attainment
    - Table S1901 Income in the Past 12 Months (in 2023 Inflation-Adjusted Dollars)
- United States Census Bureau -- Cartographic Boundary Files, https://www.census.gov/geographies/mapping-files/time-series/geo/cartographic-boundary.html

## Analysis method
The analysis process includes 
   - merging datasets and dropping missing values
   - creating visualizations, specifically overlaying layers to study spatial relationships
   - running a regression analysis
   - interpretation of the result

## Conclusion
<b>Conclusion 1</b>: The hypothesis is false. The choropleth map might show some overlapping clusters which implies correlation, but according to the regression analysis, high-speed broadband is not highly correlated with median household income in a county. <br>
<b>Conclusion 2</b>: The hypothesis is false. According to the regression analysis, bigger populations with higher education attainment does not associate with higher percentage of high-speed broadband coverage. Some counties with lower highly educated populations also have access to 5G services. <br>
<b>Conclusion 3</b>: The hypothesis is true. According to the log-linear regression model, population density in a county is highly and positively correlated with its broadband coverage.

## Limitations and Future work
There are some limitations to my work. For example, all the variables used in this project are aggregated at the county level. This aggregation can mask intra-county differences, leading to an overgeneralized picture of broadband coverage within each region. Also, by only conducting simple regressions, I have not accounted for spatial autocorrelations, where observations in neighboring counties may be more similar to each other than counties that are far apart. If data is available, we can use smaller geographic units for the variables in this project such as neighborhoods. Accounting for spatial autocorrelations, models such as spatial autoregressive can be used. The analysis is conducted with only dataset of a single year which makes it quite limited to discover more interesting patterns. Tracking 5G coverage and socioeconomic variables over multiple years might show trends and allow us to observe how these variables grow over time.

