# Manufacturer-Analysis-using-Power-BI

# Project Overview
This Power BI project provides a Manufacturer Analysis dashboard with insights into:

Urban vs. rural market performance
Revenue by product category and country
Year-over-year growth trends
Manufacturer contributions comparison
Key features:

Interactive visualizations with drill-down capabilities
Year-over-year comparisons
Geographical revenue distribution maps
Product category performance metrics
The project demonstrates skills in data modeling, DAX calculations, and creating visualizations, turning raw data into actionable insights for business decisions.

# Data Sources
1) Sales data (CSV file)
2) Product catalog (Excel file)
3)Geographic information (CSV file)

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

Sales to Product (many-to-one on ProductID)
Sales to Geography (many-to-one on ZipCountry)
Sales to Date (many-to-one on Date)
Product to Manufacturer (many-to-one on ManufacturerID)
