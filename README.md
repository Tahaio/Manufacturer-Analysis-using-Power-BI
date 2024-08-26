# Manufacturer-Analysis-using-Power-BI

# Project Overview
This Power BI project provides a Manufacturer Analysis dashboard with insights into:

1) Urban vs. rural market performance
2) Revenue by product category and country
3) Year-over-year growth trends
4) Manufacturer contributions comparison

Key features:
- Interactive visualizations with drill-down capabilities
- Year-over-year comparisons
- Geographical revenue distribution maps
- Product category performance metrics
  
The project demonstrates skills in data modeling, DAX calculations, and creating visualizations, turning raw data into actionable insights for business decisions.

# Data Sources
- Sales data (CSV file)
- Product catalog (Excel file)
- Geographic information (CSV file)

# Data Cleaning and Preparation
1) Removed duplicate entries in the sales data
2) Standardized date formats across all tables
3) Created a custom column 'ZipCountry' by concatenating Zip and Country fields
4) Handled missing values in the product catalog by imputing with category averages

# Data Modeling
The data model consists of the following tables and relationships:

1) Sales (fact table)
2) Product (dimension table)
3) Manufacturer (dimension table)
4) Geography (dimension table)
5) Date (dimension table)
![modeling](https://github.com/user-attachments/assets/07fba750-399d-486c-9c7e-803eaa5ace24)


Key relationships:
- Sales to Product (many-to-one on ProductID)
- Sales to Geography (many-to-one on ZipCountry)
- Sales to Date (many-to-one on Date)
- Product to Manufacturer (many-to-one on ManufacturerID)

# DAX Measures and Calculations
1) Total Revenue: Total Revenue = SUM(Sales[Revenue])
2) PY Sales: PY Sales = CALCULATE(SUM(Sales[Revenue]), SAMEPERIODLASTYEAR('Date'[Date]))
3) Year-over-Year Growth: YoY Growth = DIVIDE(SUM(Sales[Revenue]) - [PY Sales], [PY Sales])
4) % Growth: % Growth = DIVIDE(SUM(Sales[Revenue]) - [PY Sales], [PY Sales])

   
Key measures explained:

- Total Revenue: Calculates the sum of all revenue in the Sales table.
- PY Sales: Calculates the sales for the same period in the previous year.
- YoY Growth: Calculates the year-over-year growth in absolute terms.
- % Growth: Calculates the year-over-year growth as a percentage.

These measures form the foundation for our trend analysis and performance comparisons across different time periods.

# Visualizations
1) Revenue by Category (Stacked Bar Chart)
2) Sum of Revenue by Country (Map)
3) Revenue and Growth Trend by Year (Combo Chart)
4) Top Manufacturers by Revenue (Tree Map)
5) Sales Distribution: Urban vs Rural (Pie Chart)
6) Key Performance Indicators (Card Visuals)

![main dashboard](https://github.com/user-attachments/assets/01b92b39-eb43-4553-9cac-8d0604d5f3c9)

# Key Insights
1) Urban sales contribute to 97.28% of total revenue
2) The 'Extreme' category shows the highest growth at 61.94%
3) USA is the top market by revenue
4) There's a consistent upward trend in revenue from 2014 to 2021
![filtered 1](https://github.com/user-attachments/assets/c01b94f4-60b7-445a-a7ce-4927432bbda1)
![filtered 2](https://github.com/user-attachments/assets/d4c25e1e-d9b4-45b9-84e3-ed7c8737a1f6)

# Future Improvements
1) Incorporate more granular geographic data for deeper regional analysis
2) Add predictive analytics for sales forecasting
3) Implement what-if parameters for scenario analysis

