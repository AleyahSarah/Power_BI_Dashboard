# Sales Insights for Atliq Hardware

## Problem Statement

Atliq Hardware is a company that supplies computer hardware and peripherals to many clients across India. Atliq Hardware has its head office in Delhi and it has many regional offices all over India.

In recent times, Atliq Hardware has been facing a challenge. Their market has been growing rapidly and as a result of this, it has become difficult for the company to gather accurate insights of its business performance. 

Previously, all insights about company performance were gathered verbally over the phone from different regional managers. However, this proved to be ineffective as the insights gathered were not always accurate and reliable. 

The company finds that its overall sales are declining and it is unable to make sense of its numbers due to the huge volumes presented in multiple excel files. Moreover, the company is unable to identify the areas on which it must focus due to the poor quality of insights.

Atliq Hardware wants a solution to this problem that they are facing. It wants to create an effective and simple interactive dashboard from which it can easily understand and gather important insights from its business in order to improve performance.

## Data Analysis using MySQL

1)Imported data into MySQL Workbench form an already existing MySQL file and loaded the sales database onto MySQL.

<img width="158" alt="image" src="https://github.com/user-attachments/assets/6845e692-e187-4e72-a26e-94683e4ff3e8" />


2)Analysed the various tables using SQL queries in order to prepare for data cleaning and gathered the following insights.

      *a) Identified irrelevant records containing markets_name "New York" and "Paris".*

<img width="959" alt="image" src="https://github.com/user-attachments/assets/9ed9cfb1-7edc-4d0c-9ae6-1ac074e72bf7" />

      b) Identified records containing currency value "USD" instead of "INR"

<img width="959" alt="image" src="https://github.com/user-attachments/assets/08cf2e11-b776-446e-bc5a-f01e45e14ccb" />

      c) Identified records having sales_amount <= 0

 <img width="959" alt="image" src="https://github.com/user-attachments/assets/dd72715b-986e-4f36-8100-c0da66ee2280" />
 


 ## Data Modelling, Data Cleaning and ETL(Extract, Transform, Load) using Power BI

 1) Connected Power BI Desktop to MySQL using a MySQL connector and loaded the sales database onto Power BI.
 2) Used the star schema to organise the data model.
    <img width="959" alt="image" src="https://github.com/user-attachments/assets/b89f66a4-7eed-48d4-abfe-d025c202510f" />

 
 3) Used Power Query Editor to perform ETL(Extract, Transform, Load)
          a) Filtered "markets_name" form "sales markets" to remove 

 
 

 
     
      
      






