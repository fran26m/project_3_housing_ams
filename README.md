# Amsterdam Case Study
# Housing Affordability and Access to Public Services

## Overview

This project analyzes the relationship between housing prices and the availability of public amenities across Amsterdam. Using geospatial analysis, we explored how access to healthcare facilities, leisure amenities, and grocery shops varies between postal code areas (PC4) and whether these differences are associated with housing prices.

The project combines geographic information, housing data, and data visualization to identify spatial patterns that may support urban planning and housing policy.

---

## Data Sources

1. [OpenStreetMap / Geofabrik](https://download.geofabrik.de/europe/netherlands/noord-holland.html) geospatial data: Points of Interest (POIs), including:
- Health amenities: hospitals, clinics, pharmacies, and doctors' practices.
- Leisure amenities: parks, sports facilities, cinemas, and other recreational locations.
- Grocery shops: supermarkets, convenience stores, and bakeries.
- Administrative boundary of the Municipality of Amsterdam, used to clip the study area.

2. [Amsterdam Municipality Open Data](https://data.amsterdam.nl/):
- API: Public geospatial dataset containing the locations of glass recycling containers across Amsterdam.
- PC4 postal code boundaries.
- Number of house units per postal code.

3. [Housing Prices](https://github.com/jangboolee/amsterdam-housing-2025/tree/main) Dataset:
- Average housing prices by PC4 postal code.

---

## Problem Statement

How are health, leisure and grocery amenities distributed across Amsterdam?
Which postal codes have the highest concentration of amenities?
Is there a relationship between amenity availability and housing prices?
Which type of amenity shows the strongest correlation with house prices?

---

## Findings

The analysis shows that amenities are unevenly distributed across Amsterdam. Grocery shops present the strongest positive relationship with housing prices, while health amenities show a weaker positive correlation and leisure amenities a weak negative correlation. Overall, amenity availability alone does not explain differences in housing prices, suggesting that additional factors such as accessibility, location and neighborhood characteristics also play an important role.

---

## Full Report

A detailed report of the analysis can be found here:

[📄 Housing Affordability and Access to Public Services](./AmsterdamCaseStudy_Housing.pdf)

---

## Methodology

Data Cleaning
Selected only the required variables from each dataset.
Removed unnecessary POI categories.
Checked and handled missing values.
Standardized postal code formats across datasets.
Geospatial Analysis.
Imported geographic data using GeoPandas.
Clipped the North Holland POI dataset to the Amsterdam municipality.
Performed a spatial join to assign every Point of Interest to its corresponding PC4 postal code.
Aggregated amenities by postal code.
Data Analysis.
Classified POIs into three categories: health, , leisure, and grocery shops.
Counted amenities per postal code.
Calculated the number of amenities per 1,000 house units to allow fair comparisons between neighborhoods.
Merged amenity counts with housing price data.
Calculated Pearson correlation coefficients.
Data Visualization: using choropleth maps, bar charts, scatter plots with regression lines, correlation heatmap and comparative postcode maps.


Technologies and libraries
- Python
- Pandas
- GeoPandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Future improvements

Incorporating additional amenity categories (education, transportation, culture).
Including socioeconomic variables such as income and population density.
Measuring accessibility using travel distance instead of simple amenity counts.
Performing predictive modeling to estimate housing prices using multiple explanatory variables.
Extending the analysis to other Dutch cities for comparison.


---

## Project management

Organized using [Trello Kanban Board Board](https://trello.com/b/nOq6BNLy/my-trello-board)

---

## Authors

Created as an project for the Ironhack Data Analysist Program.
