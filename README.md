# Data-Cleaning-and-Transformation-using-python
# Energy Analysis

This repository contains a solution for analyzing energy data using pandas in Python. The analysis involves merging and processing multiple datasets to derive insights about energy supply, renewable energy production, GDP, and scientific journal contributions.

## Dataset Description

The analysis uses the following datasets:

1. **Energy Indicators**: This dataset provides information about energy supply and renewable electricity production for various countries. It is sourced from the United Nations and is available in the file `Energy Indicators.xls`.

2. **World Bank GDP**: This dataset contains GDP data for countries from 1960 to 2015. It is sourced from the World Bank and is available in the file `world_bank.csv`.

3. **Scimago Journal and Country Rank**: This dataset ranks countries based on their contributions to energy engineering and power technology research. It is available in the file `scimagojr-3.xlsx`.

## Solution Steps

The analysis follows these steps:

### Step 0: Data Cleaning and Preparation

- Load the Energy Indicators dataset, clean and transform the data, and create a DataFrame named `energy` with relevant columns.

### Step 1: Load World Bank GDP Data

- Load the World Bank GDP dataset, clean and transform the data, and create a DataFrame named `GDP`.

### Step 2: Load Scimago Journal and Country Rank Data

- Load the Scimago Journal and Country Rank dataset and create a DataFrame named `ScimEn`.

### Step 3: Merge and Filter Datasets

- Merge the energy, GDP, and ScimEn datasets based on the country name.
- Retain only the top 15 countries by Scimagojr Rank.
- Keep the last 10 years (2006-2015) of GDP data.
- Create a new DataFrame named `merged` with the merged and filtered data.

### Step 4: Lost Entries Calculation

- Calculate the number of entries lost during the merging process.

### Step 5: Average GDP Calculation

- Calculate the average GDP over the last 10 years for each country.
- Return a Series named `avgGDP` with the average GDP for the top 15 countries, sorted in descending order.

### Step 6: Mean Energy Supply per Capita

- Calculate the mean energy supply per capita across all countries.

### Step 7: Maximum Renewable Percentage

- Identify the country with the highest percentage of renewable energy and the corresponding percentage.

### Step 8: Maximum Self-Citation Ratio

- Create a new column that represents the ratio of self-citations to total citations.
- Identify the country with the highest ratio of self-citations.

### Step 9: High Renewable Countries

- Create a new column that indicates whether a country has a renewable energy percentage above the median.
- Return a series named `HighRenew` with the index as the country name, sorted in ascending order of rank.

### Step 10: Grouping by Continent

- Group the countries by continent and calculate the sample size, sum, mean, and standard deviation of the estimated population for each continent.
- Return a DataFrame with the index named `Continent` and columns `['size', 'sum', 'mean', 'std']`.

## Results

The analysis provides various insights into energy supply, renewable energy production, GDP, and scientific journal contributions. The results are available in the output
