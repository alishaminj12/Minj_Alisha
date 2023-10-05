# Analysis of Electricity Consumption: Sales, Revenue, and Prices from 2010-2023

**Author**: Alisha Minj  
**Prepared for**: UMBC Data Science Master’s Degree Capstone  

🔗 **GitHub**: [Alisha Minj's GitHub](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha)  
🔗 **LinkedIn**: [Alisha Minj's LinkedIn](https://www.linkedin.com/in/alisha-minj)  
🔗 **PowerPoint Presentation**: [To be updated]  
🔗 **YouTube Demo**: [To be updated] 


## Background

Electricity consumption and its associated metrics such as sales, revenue, and prices have always been an integral part of evaluating a region's development and energy needs. Understanding the dynamics of these factors helps policymakers, businesses, and consumers make informed decisions.

- **What is it about?**  
  This analysis explores the electricity consumption trends in terms of sales, revenue, and prices.

- **Why does it matter?**  
  Proper analysis can lead to improved energy policy decisions, smarter business investments, and increased awareness about energy consumption patterns among consumers.

- **Research Questions**:
  1. How has the electricity consumption pattern changed from 2010 to 2023?
  2. Which states have seen the most significant changes in their consumption patterns?
  3. How do sales correlate with revenue and prices?


## Data

- **Data Sources**: Data acquired from EIA's [official website](https://www.eia.gov/electricity/data.php).
- **Data Size**: 1655 KB
- **Data Shape**: (8313, 24)
- **Time Period**: Data spans from January 2010 to July 2023.
- **Each Row Represents**: Electricity metrics for a particular state in a specific month and year.

### Data Dictionary

| Column Name                | Data Type | Definition                                       | Potential Values                             |
|----------------------------|-----------|--------------------------------------------------|----------------------------------------------|
| Year                       | Object    | Year of data entry                               | 2010-2023                                    |
| Month                      | Object    | Month of data entry                              | Jan-Dec                                      |
| State                      | Object    | US State                                         | All US States                                |
| Data Status                | Object    | Status of the data entry                         | Final (2010-2021), Preliminary (2022-2023)   |
| RESIDENTIAL_Revenue        | Object    | Revenue from residential sales                   | Numerical values in Thousand Dollars         |
| RESIDENTIAL_Sales          | Object    | Sales in the residential sector                  | Numerical values in Megawatthours            |
| RESIDENTIAL_Customers      | Object    | Count of residential customers                   | Numerical values                             |
| RESIDENTIAL_Price          | Object    | Price in the residential sector                  | Numerical values in Cents/kWh                |
| COMMERCIAL_Revenue         | Object    | Revenue from commercial sales                    | Numerical values in Thousand Dollars         |
| COMMERCIAL_Sales           | Object    | Sales in the commercial sector                   | Numerical values in Megawatthours            |
| COMMERCIAL_Customers       | Object    | Count of commercial customers                    | Numerical values                             |
| COMMERCIAL_Price           | Object    | Price in the commercial sector                   | Numerical values in Cents/kWh                |
| INDUSTRIAL_Revenue         | Object    | Revenue from industrial sales                    | Numerical values in Thousand Dollars         |
| INDUSTRIAL_Sales           | Object    | Sales in the industrial sector                   | Numerical values in Megawatthours            |
| INDUSTRIAL_Customers       | Object    | Count of industrial customers                    | Numerical values                             |
| INDUSTRIAL_Price           | Object    | Price in the industrial sector                   | Numerical values in Cents/kWh                |
| TRANSPORTATION_Revenue     | Object    | Revenue from transportation sales                | Numerical values in Thousand Dollars         |
| TRANSPORTATION_Sales       | Object    | Sales in the transportation sector               | Numerical values in Megawatthours            |
| TRANSPORTATION_Customers   | Object    | Count of transportation customers                | Numerical values                             |
| TRANSPORTATION_Price       | Object    | Price in the transportation sector               | Numerical values in Cents/kWh                |
| TOTAL_Revenue              | Object    | Total revenue from all sectors                   | Numerical values in Thousand Dollars         |
| TOTAL_Sales                | Object    | Total sales from all sectors                     | Numerical values in Megawatthours            |
| TOTAL_Customers            | Object    | Total count of customers from all sectors        | Numerical values                             |
| TOTAL_Price                | Object    | Average price across all sectors                 | Numerical values in Cents/kWh                |

**Target for ML Model**: `RESIDENTIAL_Sales`  

**Potential Predictors**:
- **Year and Month**: Time variables can capture temporal patterns and seasonality in the data.
- **State**: Different states might have distinct consumption patterns.
- **RESIDENTIAL_Revenue & RESIDENTIAL_Price**: To understand how sales correspond to revenue and price changes in the residential sector.
- **COMMERCIAL_Sales & INDUSTRIAL_Sales**: Consumption in other sectors can indirectly affect or reflect residential consumption trends.
- **TOTAL_Revenue & TOTAL_Price**: A macro perspective, understanding overall revenue and price dynamics can be predictive.
- **Data Status**: Can be used to weigh recent observations differently since they're preliminary.


## Exploratory Data Analysis (EDA)

A comprehensive EDA will be performed focusing on:
- Summary statistics of key variables.
- Visualizations showcasing the trend and distribution of the target variable and predictors.
- Data cleansing activities to handle missing values and duplicates.
- Transformation and feature engineering, if necessary.


## Model Training

- **Models to be used**: Linear Regression, Random Forest, and ARIMA models.
- **Training Strategy**: Data will be split into an 80/20 train-test split.
- **Packages**: Primarily `scikit-learn`, `statsmodels`, and ARIMA.
- **Environment**: Local development, with potential to extend to Google CoLab.
- **Performance Metrics**: Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared value.


## Application of the Trained Models

A web application will be developed to allow users to:
- Input their state and month-year to get predictions on electricity sales.
- View historical trends and metrics.
- Developed using **Streamlit** due to its simplicity and integration capabilities.

## Conclusion

_[After analysis, summarize your findings, limitations, and discuss future directions and potential applications.]_


## References

- [U.S. Energy Information Administration (EIA)](https://www.eia.gov/electricity/data.php) - EIA's official website  
_[Add other references as applicable]_
