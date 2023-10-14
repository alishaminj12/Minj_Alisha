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
- **TOTAL_Revenue & TOTAL_Price**: A macro perspective, understanding overall revenue and price dynamics can be predictive.

# Exploratory Data Analysis

Exploratory Data Analysis (EDA) is a critical step in understanding the patterns, relationships, and structures within our data. For this project, we primarily focused on understanding the electricity sales trends in Maryland across different sectors.

## 1. Time Series Analysis of Sales Trends

### a) Time Series Plot with Plotly

![Time Series Plot with Plotly](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha/blob/main/data/Time%20Series%20Plot%20with%20Plotly.png)

**Insight:**  
From the time series plot, we observe that electricity consumption in the residential sector has shown a steady increase over the years. This indicates a growing demand in residential settings. Meanwhile, the commercial and industrial sectors present a fluctuating pattern, potentially influenced by economic or industrial cycles.

### b) Monthly Sales Distribution for Maryland (2022)

![Monthly Sales Distribution for Maryland - 2022](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha/blob/main/data/Monthly%20Sales%20Distribution%20for%20Maryland%20-%202022.png)

**Insight:**  
The bar chart showcases the distribution of monthly sales for residential electricity. Peaks may suggest months of higher sales. This can help in identifying months with unusually high or low sales, which is critical for business operations.

## 2. Seasonal Patterns in Residential Sales

### a) Average Monthly Residential Sales Over the Years

![Seasonal Patterns](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha/blob/main/data/Seasonal%20Patterns.png)

**Insight:**  
The seasonal plot reveals discernible patterns:

- **Summer Peak:** There is a notable peak during the summer months, particularly in July and August. This rise can likely be attributed to the increased use of air conditioning systems, fans, and other cooling devices.
  
- **Winter Rise:** Winter months, especially January, also witness a surge, possibly due to the reliance on electric heaters and increased indoor electricity-dependent activities.

- **Stable Spring and Fall:** Consumption levels during April, May, September, and October are relatively consistent, likely due to milder temperatures reducing the need for extensive heating or cooling.

- **Lowest in Fall:** November records the lowest average sales, possibly because it’s positioned after the summer peak and before the winter rise. The mild weather during this period might minimize the need for intensive heating or cooling.


## 3. Bivariate Analysis

### a) Correlation Heatmap

![Correlation Heatmap](https://github.com/DATA-606-2023-FALL-THURSDAY/Minj_Alisha/blob/main/data/Correlation%20Heatmap.png)

The heatmap reveals the following insights:
- Strong positive correlations between several predictors.
- A notably high correlation between `TOTAL_Revenue` and `TOTAL_Price` (0.85), implying a consistent pricing strategy across the board.
- `RESIDENTIAL_Sales` shows significant positive relationships with both `RESIDENTIAL_Revenue` and `RESIDENTIAL_Price`. This suggests that sales in the residential sector are likely influenced by both price and revenue dynamics.
- It's crucial to note that correlation doesn't necessarily imply causation. However, these findings do provide valuable insights into potential relationships and factors influencing residential electricity sales in Maryland.

