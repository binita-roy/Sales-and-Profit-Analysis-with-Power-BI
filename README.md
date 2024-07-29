# Sales-and-Profit-Analysis-with-Power-BI
This repository contains an in-depth analysis of Adidas Sales dataset for the period of 2020 to 2021 in USA using Power BI. This dataset was collected from Kaggle and includes the sales, profit, and product information from different retailers across different states of USA.
## Objectives
The primary objective of this analysis is to develop a dynamic, interactive dashboard to visualize the sales and profit trends over the years in different locations, identifying the most successful product and the sales performance of the retailers in order to facilitate with data-driven decision-making.
## Data
•	The dataset was collected from Kaggle
https://www.kaggle.com/datasets/ahmedabbas757/dataset
•	The extent of this dataset is limited to USA for the period of 2020 to 2021
•	An overview of the columns of the dataset can be viewed in the following snapshot
<div align="center">
<img width="181" alt="Dataset_Adidas Sales Data" src="https://github.com/user-attachments/assets/35dfce6e-0a5f-46f9-951b-78fd259a7806">

## Overview
The analysis is structured into three dashboards including:
1.	**Sales and Profit Analysis:** Provides an interactive dashboard to visualize the trends of sales, profit, cost of goods sold, profit margin, and important KPIs of sales and profit over the analysis period across different regions of USA.
2.	**Product Comparison:** Provides key insights into the performance of the products to identify the most successful product based on the sales amount, profit, profit margin, and the total units sold by the retailers at different locations.
3.	**Retailer Breakdown:** Provides a dashboard for breaking down the retailer information into more details and enabling to find out which retailers generated the highest amount of sales in which sales method as well as a comprehensive analysis of average profit margin and target profit margin.
## Workflow
1.	**Data Import:** Downloaded the Adidas Sales dataset from Kaggle and imported it into Power BI Dsktop.
2.	**Data Transformation:** Utilized the Power Query to check the data quality and errors and prepared it for the analysis by cleaning and formatting.
3.	**New Measure and Column:** Utilized the DAX (Data Analysis Expressions) functions of Power BI to create the following columns and measures:
```Profit Margin = 'data_sales (1)'[Operating Profit] / 'data_sales (1)'[Total Sales]```
`Total Amount of Sales = 'data_sales (1)'[Price per Unit] * 'data_sales (1)'[Units Sold]`
`Profit = 'data_sales (1)'[Total Amount of Sales] * 'data_sales (1)'[Profit Margin]`
`Cost_of_Good_Sold = 'data_sales (1)'[Total Amount of Sales] - 'data_sales (1)'[Profit]`
`Target Profit by Year = 5000000`
`Target Profit Margin = 0.5`
`Target Sales by Year = 10000000`
`Maximum Profit Margin = 1.0`
`Number of Sales Above Target Profit Margin = SUMX('data_sales (1)', IF('data_sales (1)'[Profit Margin] > [Target Profit Margin], 1, 0))`
`Number of Sales Below Target Profit Margin = SUMX('data_sales (1)', IF('data_sales (1)'[Profit Margin] < [Target Profit Margin], 1, 0))`
4.	**Data Visualization:** Used different data visualization options such as Card, KPI, Line chart, Map, Pie chart, and so on to visualize the key insights of the dataset.
5.	**Interaction with the Visuals:** Utilized the “Slicer” visual for exploring the dashboard using the dropdowns and tiles to filter the Year, Retailer, Product by Gender, Product, and State to uncover the trends and patterns based on the filters.
## Dashboards
The snapshots of the dashboards are attached below to get a glimpse of the dashboards.
![image](https://github.com/user-attachments/assets/a4152b1a-099a-4615-a534-acf92da25fc4)
![image](https://github.com/user-attachments/assets/3453d03f-b3bb-4a20-87c3-263ae1824e6d)
![image](https://github.com/user-attachments/assets/b3aaffb0-cdec-4468-b557-16adf64c2b10)
## Acknowledgements:
•	Microsoft Power BI for facilitating the data analysis and visualization.
•	Kaggle for providing the Adidas Sales dataset.
## Author:
Binita Roy
## Contact:
For any inquiries or collaborations, please reach out via email: [binitaroy1312@gmail.com] (binitaroy1312@gmail.com)




