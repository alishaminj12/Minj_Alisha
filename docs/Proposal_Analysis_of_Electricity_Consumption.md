# Analysis of Electricity Consumption: Sales, Revenue, and Prices from 2010-2022

### Author: Alisha Minj

* [GitHub Profile](#) - Alisha Minj's GitHub
* [LinkedIn Profile](#) - Alisha Minj's LinkedIn
* [PowerPoint Presentation](#) - Link to be updated
* [YouTube Demo](#) - Link to be updated


## Background

**Electricity consumption** and its associated metrics such as sales, revenue, and prices have always been vital in gauging a region's development and energy needs. Recognizing the dynamics of these elements facilitates informed decision-making for policymakers, businesses, and consumers.

### What is it about?

This research scrutinizes the electricity consumption trends, focusing on sales, revenue, and prices.

### Why does it matter?

Accurate evaluation can streamline energy policies, lead to intelligent business ventures, and heighten awareness regarding energy consumption patterns among consumers.


## Data

- **Data Sources**: Data acquired from EIA's [official website](https://www.eia.gov/electricity/data.php).
- **Data Size**: 1655 KB
- **Data Shape**: (8313, 24)
- **Time Period**: Data spans from 2010 to 2022.
- **Each Row Represents**: Electricity metrics for a particular state in a specific month and year.

### Data Dictionary

| Column Name               | Data Type | Definition                                          | Potential Values                                   |
|---------------------------|-----------|-----------------------------------------------------|----------------------------------------------------|
| Year                      | Object    | Year of data entry                                  | 2010-2022                                          |
| Month                     | Object    | Month of data entry                                 | Jan-Dec                                            |
| State                     | Object    | US State                                            | All US States                                      |
| RESIDENTIAL_Revenue       | Object    | Revenue from residential sales                      | Numerical values in Thousand Dollars               |
| RESIDENTIAL_Sales         | Object    | Sales in the residential sector                     | Numerical values in Megawatthours                  |
| RESIDENTIAL_Customers     | Object    | Count of residential customers                      | Numerical values                                   |
| RESIDENTIAL_Price         | Object    | Price in the residential sector                     | Numerical values in Cents/kWh                      |
| COMMERCIAL_Revenue        | Object    | Revenue from commercial sales                       | Numerical values in Thousand Dollars               |
| COMMERCIAL_Sales          | Object    | Sales in the commercial sector                      | Numerical values in Megawatthours                  |
| COMMERCIAL_Customers      | Object    | Count of commercial customers                       | Numerical values                                   |
| COMMERCIAL_Price          | Object    | Price in the commercial sector                      | Numerical values in Cents/kWh                      |
| INDUSTRIAL_Revenue        | Object    | Revenue from industrial sales                       | Numerical values in Thousand Dollars               |
| INDUSTRIAL_Sales          | Object    | Sales in the industrial sector                      | Numerical values in Megawatthours                  |
| INDUSTRIAL_Customers      | Object    | Count of industrial customers                       | Numerical values                                   |
| INDUSTRIAL_Price          | Object    | Price in the industrial sector                      | Numerical values in Cents/kWh                      |
| TRANSPORTATION_Revenue    | Object    | Revenue from transportation sales                   | Numerical values in Thousand Dollars               |
| TRANSPORTATION_Sales      | Object    | Sales in the transportation sector                   | Numerical values in Megawatthours                  |
| TRANSPORTATION_Customers  | Object    | Count of transportation customers                   | Numerical values                                   |
| TRANSPORTATION_Price      | Object    | Price in the transportation sector                  | Numerical values in Cents/kWh                      |
| TOTAL_Revenue             | Object    | Total revenue from all sectors                      | Numerical values in Thousand Dollars               |
| TOTAL_Sales               | Object    | Total sales from all sectors                        | Numerical values in Megawatthours                  |
| TOTAL_Customers           | Object    | Total count of customers from all sectors           | Numerical values                                   |
| TOTAL_Price               | Object    | Average price across all sectors                    | Numerical values in Cents/kWh                      |


## Exploratory Data Analysis (EDA)

An exhaustive exploration of the dataset unfolded, accentuating pivotal variables:

* **Summary Statistics**: An analysis was conducted to gauge the distribution and essential tendencies of key metrics.
* **Visualizations**: Leveraging Plotly Express, visuals were crafted to expose trends, distributions, and relationships.
* **Data Cleaning**: Ensured the data was devoid of missing values and duplicates.
* **Data Transformations and Feature Engineering**: This paved the path for predictive modeling.

### Key Insights from EDA:

1. **Seasonal Patterns**: Electricity consumption presented prominent seasonal patterns with conspicuous spikes during specific intervals.
2. **State-wise Consumption**: Certain states continually exhibited heightened electricity consumption, pointing towards regional determinants such as industrial activity and population density influencing demand.
3. **Correlation Metrics**: A discernible correlation between `RESIDENTIAL_Revenue` and `RESIDENTIAL_Sales` was noted, hinting at a proportional relationship.


