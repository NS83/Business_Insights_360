# Business_Insights_360

**Project Overview**

AtliQ Hardware is an electronics company that manufactures consumer goods and operates in various countries. As the company continued to grow rapidly, Excel alone wasn't sufficient to provide comprehensive business insights. While Atliq continued to experience substantial growth, they also incurred a significant loss in Latin America as business decisions were made based on a combination of surveys and intuitions. Meanwhile, AtliQ's competitors continued to experience substantial growth, attributed to their large data analyst team with a robust understanding of the market demographics, consumption patterns, and income levels. The company holds an annual strategic meeting and brings up this issues as one of the key agendas for the year. The stakeholders decide to onboard a data analyst team to facilitate data-driven decision-making within the company. The product owner/ main stakeholder of AtliQ Hardwares provided an Excel file  to the Data Analytics Director with the report features outlining the requiremenwits for five different dashboards. The Data Analytics Director subsequently establishes a Data Analyst team, comprising both a senior and junior data analyst, who then engage in communication with the product owner and start off with the project kick-off meeting.

I worked on this project as part of the Codebasics bootcamp (https://codebasics.io/).

**Tech Stacks**
* Power BI desktop
* Project Charter
* SQL
* Excel
* DAX
* Dax Studio (to optimize report and reduce File size by 25%)

**Knowledge Acquired**
* Undertsand Problem Statement
* Use of Project Charter to het a better understanding of project goals, hopes & fears, risks, & timeline
* Load and connect data with MySQL
* Create date dimension table
* Validate data against benchmark numbers
* Transfrom data in Power Query
* Create calculated columns in Power Query
* Data Modeling to connect to connect dimensions with fact tables (understand star and snowflake schema)
* Create measures using DAX
* Use DAX studio to optimize report and reduce file size
* Design various views as part of the report
* Review mock ups for each view & understanding the key metrics needed to build each view
* Use CALCULATE, RELATEDTABLE,SUMX, DIVIDE, and such functions to create new measures
* Design home page with icons for individual pages and set ups actions to navigate to individual pages
* Create dynamic titles based on applied filters
* Create a toggle bar between two visuals
* Use Bookmarks to choose between visuals
* Choose appropriate graphs for optimal understanding
* Add filters, slicers, key perfromance indicators to each page
* Nitty gritties of designing a dashboard
* Create user acceptance report
* Create a Power BI service account to publish the report
* Implement stakeholder feedback post review
* Set up automatic refresh for MySQL & Excel


**Key Business Concepts**
* Gross Price
* Pre-invoice Deduction
* Net invoice Sales
* Post-invoice Deduction
* Net Sales
* Cost of Goods Sold
* Gross Margin
* Gross Margin %
* Gross Margin/ Unit
* Operational Expense
* Net Profit
* Net Profit %
* Forecast, Accuracy, Net Error, Absolute Error, Forecast Accuracy
* Customer, Consumer
* Platforms: Brick & Mortar, E-Commerce
* Channels: Retail, Direct, & Distributor


**Project Charter Meeting: Questions asked**
* What are the objectives of this project?
* What are the success measures for this project?
* What will be the timeline for this project?
* What are the hopes and fears of the stakeholders for this project?
* How will the data analyst team validate data accuracy in the Power BI dashboard?
* How will the data analyst team avoid feature creep?
* Who are the team members involved in the project?
* What are the points to define this project to be a success?
* What are the risks involved in building this project?


**Data Exploration**

There are two SQL dump files that are provided: gdb041 and gdb056. Both the files were unziped using Winzip after which they were imported into mySQL.
Each file consists of dimension tables and Fact tables. Fact tables consist of transactional data ( things that happened) + foreign keys and Dimension tables consist of entities that participate in the transaction + primary keys (which is like a unique identification code for each dimension record). 

gdb041:
   
* dim_customer:
             
              * 76 Distinct and 20 Unique value for Customers
              * 27 Distinct and 1 Unique value for market
              * 2 Distinct ( Brick & Mortar, E-Commerce) and 0 Unique values for platform
              * 3 Distinct (Retailer, Direct, & Distributor) and 0 Unique values for Channel
              * 209 Distinct and 209 Unique values for Customer Code

* dim_market:

              * 27 Distinct (such as India, FRANCE, Germany) and 27 Unique values for market
              * 7 Distinct (such as ROA, NE, LATAM, NA) and 1 Unique value for sub_zone
              * 4 Distinct(EU, APAC, LATAM, NA) and 0 Unique value for region


* dim_product:

              * 397 Distinct and Unique values for product_code
              * 3 Distinct values for Division (P & A, PC, N & S)
              * 6 Distinct values for segment (such as Notebook, Peripherals, Desktop)
              * 14 Distinct values for categories (such as Personal Laptop, Mouse, Keyboard)
              * 73 Distinct values for product ( such as AQ F16, AQ Smash 1, AQ Gamer 1)
              * 27 Distinct and 1 Unique value for variant (such as Plus 2, Standard, Premium)

  
* fact_forecast_monthly:

              * This table contains forecast quantity along with product and customer code
  
* fact_sales_monthly:

              * This table is similar to the fact_forecast_monthly except that the last column represents the actual
                sold quantity of products instead of the forecast quantity.


gdb056:

* freight_cost:

             * 27 Distinct values for market]
             * This table contains freight_pct and other_cost_pct
  
* gross_price:

             * This table consists of gross price with product code
  
* manufacturing_cost:

             * This table contains manufacturing cost with product code
  
* pre_invoice_deductions:

             * This table contains the pre-invoice discount percent with customer code
  
* post_invoice_deductions:

             * This table contains post invoice Discount percent and other deductions percent with product and customer code



After a thorough evaluation of the dataset, I began by loading the data from MySQL to Power BI. Once the data was loaded, I performed data transformation in 
Power Query followed by Query folding to improve performance.

**Data Modeling**

* Data modeling is crucial in Power BI for several reasons, as it plays a fundamental role in structuring and organizing data to create meaningful visualizations and insights.
* Data modeling allows you to establish relationships (in this case, one to many relation) between these tables, enabling the creation of comprehensive reports by combining information
  from different sources.
* By defining relationship, it is ensured that the data is accurate and consistent across various tables.
* Data modeling allows for the creation of calculated columns and measures, enabling the aggregation and summarization of data. This is essential for generating key performance indicators (KPIs) and other 
  metrics that provide valuable insights.
* Effective data modeling is essential for writing DAX formulas to create custom calculations that can manipulate and analyze data in meaningful ways.



![image](https://github.com/NS83/Business_Insights_360/assets/44031440/4bee400c-1c06-4452-8d75-22c4b9ceb090)


**HOME PAGE**
![image](https://github.com/NS83/Business_Insights_360/assets/44031440/1ed80d01-75f6-4012-bc2e-a9e3e09b9851)


**FINANCE VIEW**![image](https://github.com/NS83/Business_Insights_360/assets/44031440/48c6cd48-f82e-4869-80ca-6ef0132d6c8b)


**SALES VIEW**![image](https://github.com/NS83/Business_Insights_360/assets/44031440/8d4ccef0-e53a-4205-a52b-4463c03cbd70)


**MARKETING VIEW**![image](https://github.com/NS83/Business_Insights_360/assets/44031440/b929459f-a192-4821-9273-b32e74c827b7)


