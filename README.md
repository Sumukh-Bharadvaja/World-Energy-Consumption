# World Energy Consumption Analysis

## Overview
This repository contains a Tableau workbook (`World_Energy_Consumption.twb`) dedicated to the visualization and analysis of world energy consumption data. The workbook provides insightful visualizations that cover various aspects of energy consumption across different countries and through the years, showcasing trends, comparisons, and key insights into how energy consumption has evolved globally.

# Data Cleaning
Before creating the visualizations, the dataset underwent a thorough cleaning process. The Jupyter notebook (`Data_cleaning.ipynb`) included in this repository details every step taken to ensure data quality. This process involved:

- Removing duplicates and irrelevant entries
- Normalizing data formats
- Handling missing values appropriately
- Ensuring data consistency and accuracy

The cleaned data was saved into a `reworked_dataset`, which serves as the foundation for the Tableau visualizations.

# Tableau worksheet

The workbook in Tableau contains various pre-configured visualizations. Users can interact with the charts and graphs to gain insights into energy consumption patterns across different countries and time periods.

- The data is divided into important energy sources Renewable and Non rennewable.
- World population and world energy production has been created using geolocation plot as well as bar chart
- Functions to determine change has been done using calculation field with following code:
- 1. For indicating the change with arrows : IF SUM([Production]) > LOOKUP(SUM([Production]), -1) THEN "△" ELSEIF SUM([Production]) < LOOKUP(SUM([Production]), -1) THEN "▽" ELSE "" END
- 2. For indicating the overll percentage increase in the production : (SUM([Production]) - LOOKUP(SUM([Production]), -1)) / LOOKUP(SUM([Production]), -1) * 100

- Finally interactive dashboard has been created to view the production as well as per capita and population of the countries.

## Tableau Public Visualization
The visualizations created from this cleaned dataset are available for public viewing on Tableau Public. You can explore the interactive dashboard by following this link: [World Energy Consumption Dashboard](https://public.tableau.com/app/profile/sumukh.bharadvaja.shivaram/viz/World_Energy_Consumption/Dashboard2?publish=yes).

This repository highlights the world energy consumption as well as production for period of 30 years(1990-2022)