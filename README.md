# Superstore Sales & Profitability Analysis

## Project Overview
In this project, I performed a comprehensive data analysis for a retail Superstore using Python. The dataset covers four years of sales and profit data (2014-2017). My goal was to explore the business's growth patterns and evaluate the efficiency of sales operations across different regions and categories

## Problem Statement
While the Superstore saw a significant increase in total sales volume in 2017, the net profit did not grow at a proportional rate.  A visual analysis of the trends indicates that the cost of generating sales is rising, leading to a visible decline in overall profit margins. 
The core objective of this analysis is to investigate this divergence and identify the specific factors, whether regional, categorical, or operational, that are suppressing profitability.

## Methodology:

### Data Collection & Understanding
    - Dataset Size: 9,994 records and 21 features.
    - Time Frame: Data spans from January 2014 to December 2017.
    - data frame: containing categorical (regional, category, sub-category) and non-categorical (Sales, Profit, Discount, quantity)
    - Key Metrics: Focused on Sales, Profit, and Discount to identify the drivers of business performance.

### Data Integrity: Performed data cleaning:
    - Handled date formats
    - Standardized category names
    - Identified and removed duplicate records to ensure unique transactions and to prevent overcounting.
    - Verified that there were no missing values in critical columns.

### Exploratory Data Analysis (EDA):

**Sales vs. Profit (The Big Picture)**
![Sales vs Profit Trend](Superstore-Profitability-Analysis/graphs/Negative_Profit_Trend_2014-2017.png)
            
**Sales vs. Profit Margin (The Efficiency)**
![Sales vs Profit Margin Trend](graphs/Overall_Profit_VS_ProfitMargin_trend_(yearly).png)
> **Insight:** While the total Sales volume shows a healthy upward trend, the **Profit Margin** is decreasing in specific months. This indicates that we are selling more but earning less per unit, likely due to high operational costs or aggressive discounting.
                
**Segmentation:**
![Category wise profit Trend](graphs/Category_Vs_Profit_(2016-2017).png)

**Region-wise Profit Loss of Office Supplies Sub-Category in 2017:**
![region wise profit Trend](graphs/Region_Wise_Profit.png)
        
**Drilling Down (Sub-Category Insights):**
![Sub-Category Graph](graphs/Central_Region_Sub-Categories_of_Office_Supplies_in_2017_(Profit_Vs_Sales).png)
        Insight: Within Furniture, Tables are causing the maximum loss. Also, in Office Supplies, Binders are showing high variance in profit.
        
**Root Cause:**
![Impact of Discount on Average Profit (Overall Store)](graphs/Sub-Category_Losses_at_Specific_Discount_Rates.png)
> To pinpoint the exact cause of profit leakage in 2017, I filtered the data for the Central Region and analyzed the relationship between Sub-Categories and Discount levels. By aggregating the total profit for discounts above 30%, it became evident that Binders at an 80% discount rate were the single largest contributor to the regional loss.
        
**The Big Picture: Overall Impact of Discounts:**
![Discount vs Profit](graphs/Impact_of_Discount_on_Average_Profit_(Overall_Store).png)
        To verify if this was a broader trend, I analyzed the average profit across all discount levels for the entire store. As shown in the chart above, profit remains positive until the 20% threshold, after which any further discounting leads to a sharp decline into negative territory.







