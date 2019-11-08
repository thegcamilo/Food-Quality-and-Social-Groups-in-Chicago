# What Is the Food Quality of Different Chicago Social Groups?

# Abstract
There is a large variation across the quality of food available across the world due to economic and cultural variations. In order to analyze the inequality of quality of food across different social and economic groups, we aim to inspect the correlation between food quality and other social and economic factors, such as income level and race, in a local level. By using data on food inspections in Chicago and supporting data, we aim to understand how inequalities found in the city are also instituted in the food available to different communities.
With our work, we plan to infer whether neglected groups are also left with lower quality food, which could lead to various diseases and social isolation. With our results, we aim to raise awareness to the distribution of food across a global metropolis, showing whether prejudice can also be found in the food available to Chicago citizens.


# Research Questions
* How does the quality of food differ across Chicago’s regions depending on their dominant race, income level, and crime activity?
* Is the food available to socially neglected groups of lower quality than the one available to majorities in the city of Chicago?
* Do food inspection authorities favor certain neighborhoods based on their demographics?
* Do some particular restaurants suffer from low quality food distribution based on restaurant type and origin?
* Does the quality of food differ across different stores of the same chain of restaurant?


# Dataset
<!-- List the dataset(s) you want to use, and some ideas on how do you expect to get, manage, process and enrich it/them. Show us you've read the docs and some examples, and you've a clear idea on what to expect. Discuss data size and format if relevant. -->
* Food Inspection: https://www.kaggle.com/chicago/chicago-food-inspections
  * Main dataset of our project. It contains information about food inspections in Chicago, their results, location, and risk, for example.
* GeoJson: *
    - By neighbourhoods : https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Neighborhoods/bbvz-uum9
    - By community areas : https://data.cityofchicago.org/Facilities-Geographic-Boundaries/Boundaries-Community-Areas-current-/cauq-8yn6/data
  * We want to analyze if there is any difference between the quality of food in different areas of the city of Chicago. For that, we need a division of the city. This work was already done by the city and we can use it by importing the GeoJSON file that they provide using the library Folium.
* Socioeconomic factors: https://data.cityofchicago.org/Health-Human-Services/Per-Capita-Income/r6ad-wvtk
  * A dataset in CSV format containing 6 socioeconomic indicators for community areas of Chicago. These include:
    * Unemployment
    * Education
    * Per capita income level
    * Poverty level
    * Crowded housing percentage
    * Age distribution
    * Economic hardship index, a combination of the other variables. Higher hardship index scores indicate worse economic conditions. 
  * We may want to use any combinations of these columns to check if there are correlations between failed food inspections and higher hardship indexes/lower income/etc.
* Race: http://www.justicemap.org/index.php?gsLayer=plural&gfLon=-87.65542953&gfLat=41.8725146&giZoom=13&
  * An SQL database containing the ethnicity of the population in percentage per each block of the US. We only need is a small part of the dataset, more specifically the city of Chicago. The first thing to do with this data will be a filtering to extract the information for the city of Chicago and use this data to check if there is a food quality bias based on the race of the habitants of particular neighbourhood. 
* Crime: https://data.cityofchicago.org/Public-Safety/Crimes-2001-to-present/ijzp-q8t2
  * A dataset that reflects reported incidents of crime that occured in the city of Chicago. For each crime, we have access to the (approximate) location and the information about whether it led to an arrest or not. We want to use this dataset to see if the crime rate by community area is correlated with the quality of food in that same area. The dataset can be exported in .CSV format and thus be analyzed easily using Pandas.
* Dataset with general information about Chicago: https://data.cityofchicago.org/Health-Human-Services/Chicago-poverty-and-crime/fwns-pcmk
  * A dataset that describes public health significance by community area. It is indeed an interesting dataset for our project as it offers informations about educational level and unemployment rates in addition to what we already have. We might find interesting correlations between these factors and quality food as well. The data can be exported to a .CSV file.

# A List of Internal Milestones Up Until Project Milestone 2
* November 1st - Document all datasets
* November 6th - Code the map plotting pipeline
* November 13th - Clean data from all datasets 
* November 18th - Calculate correlation between food quality and supporting data
* November 22nd - Plot results of data analysis
* November 25th - Milestone 2 report


# Questions for TAs
Add here some questions you have for us, in general or project-specific.
