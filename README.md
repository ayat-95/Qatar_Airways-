# 📊 Global Superstore (Qatar Airways) - Sales Dashboard

## 🏢 Overview

This dashboard provides insights into Qatar Airways' **Global Superstore Sales**, analyzing revenue, profit margins, and customer trends across different markets.

## Sales & Profit
![image](https://github.com/user-attachments/assets/d4655588-23b9-42c9-b988-2a649f242515)

## Market Compare
![image](https://github.com/user-attachments/assets/6369caf6-c1b3-4b36-841f-a5185b255c38)



## 🔑 Key Metrics

- **Total Sales for Each Market**:
  ```DAX
  Total Sales = SUM(Orders[Sales])
  ```
- **Total Profit for Each Market**:
  ```DAX
  Total Profit = SUM(Orders[Profit])
  ```
- **Profit Margin Calculation**:
  ```DAX
  Profit Margin = DIVIDE([Total Profit], [Total Sales]) * 100
  ```
  - **High Profit Margin (40%-60%)**: Efficient market with low costs.
  - **Moderate Profit Margin (20%-30%)**: Profitable but may need cost optimization.
  - **Low Profit Margin (<10%)**: High costs or low revenue indicate issues.
  - **Negative Profit Margin**: The market is operating at a loss and requires immediate attention.

## 📊 Customer Insights

- **Unique Customers in the Last Month**:
  ```DAX
  Last Month Sales =  
  CALCULATE(DISTINCTCOUNT(Orders[Customer ID]),  
            DATESINPERIOD(Orders[Date], MAX(Orders[Date]), -1, MONTH))
  ```
  - **Key Components**:
    - `CALCULATE()`: Filters data to last month.
    - `DISTINCTCOUNT()`: Counts unique customers.
    - `DATESINPERIOD()`: Filters data within a 1-month window.

## 📊 Market Analysis & Visualization

- **Best-Performing Markets**:

  - **Profit Margin**: Higher margins indicate efficiency.
  - **Total Sales & Profit**: High demand signals strong markets.
  - **Unique Customers**: Indicates customer engagement.


