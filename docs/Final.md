# Analysis of Electricity Consumption: Sales, Revenue, and Prices from 2010-2022

**Author**: Alisha Minj  
**Prepared for**: UMBC Data Science Master’s Degree Capstone  

🔗 **GitHub**: [Alisha Minj's GitHub](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha)  
🔗 **LinkedIn**: [Alisha Minj's LinkedIn](https://www.linkedin.com/in/alisha-minj)  
🔗 **PowerPoint Presentation**: [To be updated]  
🔗 **YouTube Demo**: [To be updated] 

## **Background**

Electricity serves as the backbone of modern societies, driving economies and enabling technological advancements. Its consumption patterns provide insights into a region's growth, technological adoption, and socio-economic dynamics. This study focuses on Maryland, a state in the Mid-Atlantic region of the US, known for its diverse landscapes and economic activities ranging from industrial manufacturing to agriculture.

**What is it about?**
This analysis aims to dissect the electricity consumption in Maryland over a 12-year period from 2010 to 2022. Specifically, we will explore various metrics like electricity sales, revenues, and prices across different sectors such as residential, commercial, and industrial.

**Why does it matter?**
Understanding electricity consumption patterns is crucial for several reasons:
1. **Economic Indicators:** Electricity consumption often parallels economic activity. A rise in industrial electricity demand might indicate an upswing in manufacturing and production activities.
2. **Policy Implications:** Insights from consumption patterns can guide state policymakers in framing energy policies, infrastructure development, and sustainability initiatives.
3. **Future Forecasting:** Analyzing past trends helps utility companies and state planners in predicting future demand, ensuring the state's energy needs are met without compromising on sustainability or causing undue strain on resources.

**Research Questions:**
Given the scope of the analysis, our primary research questions are:
1. How has electricity consumption in Maryland evolved over the 12-year period across different sectors?
2. What are the driving factors behind the observed trends in sales, revenue, and prices?
3. Are there discernible seasonal patterns in electricity consumption, and if so, what might be causing them?
4. How does the electricity consumption in Maryland compare with national averages or with neighboring states?

## **Data**

- **Description**: This dataset provides insights into electricity consumption metrics of various US states over the span of 12 years.
- **Data sources**: Data acquired from [EIA's official website](https://www.eia.gov/). EIA (U.S. Energy Information Administration) is a principal agency responsible for collecting, analyzing, and disseminating energy information to inform policy-making and public understanding.
- **Data size**: 1655 KB
- **Data shape**: 
  - 8313 rows
  - 24 columns
- **Time period**: Data spans from 2010 to 2022.
- **Each Row Represents**: Electricity metrics for a particular state in a specific month and year.

### **Data Dictionary**

| Column Name               | Data Type | Definition                                       | Potential Values                            |
|---------------------------|-----------|--------------------------------------------------|---------------------------------------------|
| Year                      | Object    | Year of data entry                               | 2010-2022                                   |
| Month                     | Object    | Month of data entry                              | Jan-Dec                                     |
| State                     | Object    | US State                                         | All US States                               |
| RESIDENTIAL_Revenue       | Object    | Revenue from residential sales                   | Numerical values in Thousand Dollars        |
| RESIDENTIAL_Sales         | Object    | Sales in the residential sector                  | Numerical values in Megawatthours           |
| RESIDENTIAL_Customers     | Object    | Count of residential customers                   | Numerical values                            |
| RESIDENTIAL_Price         | Object    | Price in the residential sector                  | Numerical values in Cents/kWh               |
| COMMERCIAL_Revenue        | Object    | Revenue from commercial sales                    | Numerical values in Thousand Dollars        |
| COMMERCIAL_Sales          | Object    | Sales in the commercial sector                   | Numerical values in Megawatthours           |
| COMMERCIAL_Customers      | Object    | Count of commercial customers                    | Numerical values                            |
| COMMERCIAL_Price          | Object    | Price in the commercial sector                   | Numerical values in Cents/kWh               |
| INDUSTRIAL_Revenue        | Object    | Revenue from industrial sales                    | Numerical values in Thousand Dollars        |
| INDUSTRIAL_Sales          | Object    | Sales in the industrial sector                   | Numerical values in Megawatthours           |
| INDUSTRIAL_Customers      | Object    | Count of industrial customers                    | Numerical values                            |
| INDUSTRIAL_Price          | Object    | Price in the industrial sector                   | Numerical values in Cents/kWh               |
| TRANSPORTATION_Revenue    | Object    | Revenue from transportation sales                | Numerical values in Thousand Dollars        |
| TRANSPORTATION_Sales      | Object    | Sales in the transportation sector               | Numerical values in Megawatthours           |
| TRANSPORTATION_Customers  | Object    | Count of transportation customers                | Numerical values                            |
| TRANSPORTATION_Price      | Object    | Price in the transportation sector               | Numerical values in Cents/kWh               |
| TOTAL_Revenue             | Object    | Total revenue from all sectors                   | Numerical values in Thousand Dollars        |
| TOTAL_Sales               | Object    | Total sales from all sectors                     | Numerical values in Megawatthours           |
| TOTAL_Customers           | Object    | Total count of customers from all sectors        | Numerical values                            |
| TOTAL_Price               | Object    | Average price across all sectors                 | Numerical values in Cents/kWh               |

**Target for ML Model**: `RESIDENTIAL_Sales`  

**Potential Predictors**:
- **Year and Month**: Time variables can capture temporal patterns and seasonality in the data.
- **State**: Different states might have distinct consumption patterns.
- **RESIDENTIAL_Revenue & RESIDENTIAL_Price**: To understand how sales correspond to revenue and price changes in the residential sector.
- **COMMERCIAL_Sales & INDUSTRIAL_Sales**: Consumption in other sectors can indirectly affect or reflect residential consumption trends.
- **TOTAL_Revenue & TOTAL_Price**: A macro perspective, understanding overall revenue and price dynamics can be predictive.2.
