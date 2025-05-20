# Sales Insights for Technium Hardware

## Problem Statement

Technium Hardware is a company that supplies computer hardware and peripherals to many clients across India. Technium Hardware has its head office in Delhi and it has many regional offices all over India.

In recent times, Technium Hardware has been facing a challenge. Their market has been growing rapidly and as a result of this, it has become difficult for the company to gather accurate insights of its business performance. 

Previously, all insights about company performance were gathered verbally over the phone from different regional managers. However, this proved to be ineffective as the insights gathered were neither accurate not reliable. 

The company finds that its overall sales are declining and it is unable to make sense of its numbers due to the huge volumes presented in multiple excel files. Moreover, the company is unable to identify the areas on which it must focus due to the poor quality of insights.

(*Note: "Technium Hardware" is a fictional company name used for demonstration purposes in this project.*)


## Required Solution

 Tecchnium Hardware wants to create an effective and simple interactive dashboard from which it can easily understand and gather important insights from its business in order to improve performance.


## Tech Stack

* MySQL
* Power BI Desktop
* Power Query Editor
* DAX (Data Analysis Expressions)


## Data Analysis using MySQL

1)Imported data into MySQL Workbench form an already existing MySQL file and loaded the sales database onto MySQL.

![Database Image](https://github.com/user-attachments/assets/6845e692-e187-4e72-a26e-94683e4ff3e8)



2)Analysed the various tables using SQL queries in order to prepare for data cleaning and gathered the following insights.

*a)Identified irrelevant records containing "markets_name" "New York" and "Paris"*

![irrelevant records](https://github.com/user-attachments/assets/9ed9cfb1-7edc-4d0c-9ae6-1ac074e72bf7)

*b) Identified records containing currency value "USD" instead of "INR".*

![irrelevant records](https://github.com/user-attachments/assets/08cf2e11-b776-446e-bc5a-f01e45e14ccb)

 *c) Identified records having "sales_amount <= 0"*

 ![irrelevan records](https://github.com/user-attachments/assets/dd72715b-986e-4f36-8100-c0da66ee2280)

 *d) Identified duplicate currency values.*

 ![irrlevant records](https://github.com/user-attachments/assets/51c5be07-e8ab-488e-89a5-2a6c6a6d021a)
 
 
 ## Data Modelling, Data Cleaning and ETL(Extract, Transform, Load) using Power BI

 1) Connected Power BI Desktop to MySQL using a MySQL connector and loaded the sales database onto Power BI.
 2) Used the star schema to organise the data model.
    <img width="959" alt="image" src="https://github.com/user-attachments/assets/b89f66a4-7eed-48d4-abfe-d025c202510f" />

 
3) Used Power Query Editor to perform ETL(Extract, Transform, Load)

    
*a) Filtered "markets_name" form "sales markets" table to remove records containing "New York" and "Paris"*


*b) Filtered "sales_amount" from "sales transaction" table to remove values less than or equal to 0*


*c) Removed the duplicate currencies from the "sales transactions" table*


*d) Converted USD currency to INR using the following formula:*
`= Table.AddColumn(#"Cleaned up currency", "norm_sales_amt", each if [currency] = "USD#(cr)" then [sales_amount] * 75 else [sales_amount]) `


## Creating the Dashboard 

Performed data visualisation using Power BI to visualise key performance metrics.

## Key Sales Insights
![dashboard](https://github.com/user-attachments/assets/c0f0d3d3-e541-447b-b098-61985ddbd0a5)


## Business insights gained with the help of the dashboard
* Underperforming markets
* Growth opportunities
* Key revenue drivers
* Customer loyalty
* Best Sellers
* Revenue Trend 


## References
https://codebasics.io/resources/sales-insights-data-analysis-project

https://www.youtube.com/watch?v=hhZ62IlTxYs&list=PLeo1K3hjS3uva8pk1FI3iK9kCOKQdz1I9&index=1







 
 

 
     
      
      






