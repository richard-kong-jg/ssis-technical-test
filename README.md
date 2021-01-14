# Recruitment Technical Test: Data Engineer

This is a test used during the recruitment process for data engineers at JustGiving.

## Summary
In this exercise you will use SSIS to populate a fact table in the data warehouse. Imagine you are an engineer working on a large data warehouse. This fact table is only one of many that need to be implemented.

The data for the fact tables requires data from the OLTP database as well as an API for currency rate data.

## Prerequisites
* Instance of SQL Server 2014 or newer installed
* Visual Studio with add-ons SSIS (2014 or newer) development
* Both Adventureworks OLTP and DW databases installed on your instance of SQL Server. Databases are available here: https://github.com/microsoft/sql-server-samples/tree/master/samples/databases/adventure-works use the install from script versions.


## Instructions
Your task is to create a new fact table in the AdventureWorks data warehouse that will allow a query to be run that returns `US dollar` orders with the following columns:
* `Total sales amount in New Zealand Dollars`
* `Total sales amount in US Dollars`
* `Total Quantity ordered`
* Grouped by: `Calendar Year`, `Product Colour`

For the purposes of this exercise, assume that the existing fact tables do not exist in the AdventureWorks DW database.

1. Create SSIS package(s) to load this fact table using the AdventureWorks OLTP database as the primary source
2. For `Sales Amount in New Zealand Dollars` use currency rates from https://exchangeratesapi.io/ to convert into New Zealand Dollars
3. Create a git repo and push your solution
4. Put a readme file in the repo that documents:
    1. How to build and run the solution
    2. Describe and explain reasoning behind any assumptions you have made
    3. Explian why you decided to implement things the way you did (optional)
    4. How your solution could be made better
5. Provide us with a link to your git repo


## Notes
1. You will have to look at the AdventureWorks database to work out how to populate these fields. The data in this table is similar as `FactInternetSales` so you can use that as a reference.
2. Refer to the job specification and demonstrate the attributes listed there.