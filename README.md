# Business Insights 360<br>
## Project Overview<br>
AtliQ Hardware is growing rapidly in the recent years, and they have decided to implement the data analytics using PowerBi in their company for the first time to surpass their competitors in the market and to make data driven decisions. This project is hoped to give answers to the questions of stakeholder in terms all the aspects like finance, sales, marketing and supply chain.
<br><br>
I worked on this project by following the Codebasics PowerBi Course, Link to the course is here<br><br>

Live Report Link<br><br>

## Tech stacks<br>
* SQL<br>
* PowerBi Desktop<br>
* Excel<br>
* DAX language<br>
* DAX studio (for optimizing the report)<br>
* Project charter file<br>
## PowerBI techniques Learnt<br>
* What are all the questions should be asked before staring the project<br>
* Creating calculated columns<br>
* creating measure using DAX language<br>
* Data modeling<br>
* Using Bookmarks to switch between two visuals<br>
* Page navigation with buttons<br>
* Using divide function to prevent zero division errors<br>
* creating date table using m language<br>
* Dynamic titles based on the applied filters<br>
* Using KPI indicators<br>
* Conditional formatting the values in visuals using icons or background color<br>
* Data validation techniques<br>
* PowerBi services<br>
* Publishing reports to PowerBi services<br>
* Setting up personal gateway to set up the auto refresh of data<br>
* PowerBi App creation<br>
* Collaboration, workspace, access permissions in PowerBi services<br><br>
## GitHub<br>
* Uploading Large size files using GitHub LFS<br>
* Tracking the particular type of file extensions for LFS<br>
## Business related terms<br>
* Gross price<br>
* Pre-invoice deductions<br>
* Post-Invoice deductions<br>
* Net Invoice sale<br>
* Gross Margin<br>
* Net sales<br>
* Net profit<br>
* COGC - cost of goods sold<br>
* YTD - Year to Date<br>
* YTG - Year to Go<br>
* Direct<br>
* Retailer<br>
* Distributors<br>
* Consumer<br>
## Company’s back ground<br>
AltiQ hardware is a company which has grown vastly in the recent years, and opened business all over the globe. It is a company which sells, computer and computer accessories through three mediums/channel
<br><br>
* Retailers<br>
* Direct<br>
* Distributors<br>
Recently the company has faced a unforeseen loss by opening store in America based on the surveys, intuition and some excel analysis and also the company’s competitors has handful of analytics team to perform analysis and make data driven decision. So, the AltiQ hardware has no other option other than building their analytics team for data driven insights and decisions in the future to survive better in the industry.
<br><br>
Project kick off session, where you should get clear of for what and why this project and all other questions you have with regards to the project
<br><br>
## Questions to ask before starting with dashboard<br>
* What is the objective of building this PowerBi dashboard?<br>
* In what terms the success of this project will be measured?<br>
* What will be time dead-line of the project?<br>
* do the stakeholders expecting pre-view before the actual release?<br>
* What are all the hopes stakeholders have out of this project?<br>
* what are all fears the stakeholder have in terms of building this dashboard?<br>
* Who are all will be using this dashboard and for what purpose?<br>
* what are all expectation the stakeholders have, by the completion of this project?<br>
* What can go wrong while building this project?<br>
* what are all the resources/ data needed to build this dashboard?<br>
* is there any inputs from stakeholders in terms of design and views of the dashboard?<br>
* After the project kick off meetings, the data engineering team has given the data as per the request of data analytics team, let’s explore them.<br><br>
## Dataset Understanding.<br>
Understanding what data is available will be more helpful while doing analysis. before jumping on to the analysis get good understanding of what are data available.
<br><br>
Dimension table : It will have the static data like details of customer and products
<br><br>
Fact table : It will have the data about the transactions
<br><br>
* gdb041:<br>
  * dim_customer<br>
    * 27 distinct markets (ex India, USA, spain)<br>
    * 75 distinct customers thorough out the market<br>
    * 2 types of platforms<br>
      * Brick & Motors - Physical/offline store<br>
      * E-commerce - Online Store (Amazon, flipkart)<br>
    * Three channels<br>
      * Retailer<br>
      * Direct<br>
      * Distributors<br>
* dim_market<br>
  * 27 distinct markets (ex India, USA, spain)<br>
  * 7 sub-zones<br>
  * 4 regions<br>
    * APAC<br>
    * EU<br>
    * nan<br>
    * LATAM<br>
* dim_product<br>
  * Divisions<br>
    * P & A<br>
      * Peripherals<br>
      * Accessories<br>
    * PC<br>
      * Notebook<br>
      * Desktop<br>
    * N & S<br>
      * Networking<br>
      * Storage<br>
  * There are 14 different categories, Like Internal HDD, keyboard<br>
  * There are different variants available for the same product<br>
* fact_forecast_monthly<br>
  * This table is used to forecast the customer’s need in advance, which can help in<br>
    * Higher customer satisfaction<br>
    * Reduced cost in warehouses for storage purpose<br>
  * The table is denormalized by data engineering team, as it is a data warehouse which is aimed to be used for analytical work.<br>
  * All the date of the month will be replaced by the start date of the month<br>
  * It will have all the column names and in the end it will have the forecast quantity need of the customer<br>
* fact_sales_monthly<br>
  * This table is more or less is same as fact_forecase_monthly table, but the last column has the value of sold quantity instead of forecast value.<br>
* gdb056<br>
  * freight_cost<br>
    * This table has details of travel cost and other cost for each market with fiscal year<br>
  * gross_price<br>
    * Has the details of gross prices with product code<br>
  * manufacturing_cost<br>
    * Has the details of manufacturing cost with product code with year<br>
  * Pre_invoice_dedutions<br>
    * Has the details of pre invoice deductions percentage for each cutomer with year<br>
  * Post_invoice_deductions<br>
    * Post invoice deductions and other deductions details<br>
## Importing data into PowerBi<br>
As the database is MySQL in this project, we need to import the datasets from Mysql database to PowerBi by providing the Database access credential<br>
## Data Model<br>
Data modeling plays a vital role and is considered as the basement of report. All the visuals will be build upon the data model.<br>
Poor data modeling affects the over all performance of the report.<br>
Following Good practices of data modeling is must. Refer this page to get to know the good practices Blog<br>
In this project, we have followed Snowfall data modeling method.<br>
<br><br><br>

## Dashboard designing<br>
* Based on the mock ups received as requirement, the team will start designing the visuals and create measure as and when required<br><br>

## Home view<br>
In Home view, all the views button will be available. User will land on specific view page by clicking the button<br>
<br>
* Info<br>
* Finance View<br>
* Sales View<br>
* Marketing View<br>
* Supply chain View<br>
* Executive View<br>
* Products<br>
* Support<br>
## Overall Report<br>
Overall Report.gif


## Info Page<br>
Info.gif


## Finance View<br>
Finace.gif


## Sales View<br>
Sales.gif


## Marketing View<br>
Marketing.gif


## Supply chain View<br>
Supply chain.gif


## Executive View<br>
Executive.gif


## Products<br>
Products


