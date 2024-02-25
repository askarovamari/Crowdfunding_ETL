# Crowdfunding ETL Mini Project
For the ETL mini project, we worked as a team to practice building an ETL pipeline using Python, Pandas, using both Python dictionary methods and regular expressions to extract and transform the data. After we transformed the data, we created four CSV files and used these CSV file data to create an ERD and a table schema. Finally, we uploaded the CSV file data into a Postgres database.

## Project Description
The Crowdfunding ETL Mini Project completed the following steps: 

### 1.    Create the Category and Subcategory DataFrames
Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

* A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories
* A "category" column that contains only the category titles

Export the category DataFrame as category.csv and save it to your GitHub repository.

Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

* A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories
* A "subcategory" column that contains only the subcategory titles  
* Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

### 2.    Create the Campaign DataFrame
Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

* The "cf_id" column
* The "contact_id" column
* The "company_name" column
* The "blurb" column, renamed to "description"
* The "goal" column, converted to the float data type
* The "pledged" column, converted to the float data type
* The "outcome" column
* The "backers_count" column
* The "country" column
* The "currency" column
* The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format
* The "deadline" column, renamed to "end_date" and with the UTC times converted to * the datetime format
* The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame
* The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame

Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

### 3.    Create the Contacts DataFrame
Utilized both Python dictionary methods and regular expressions for extracting and transforming the data from the contacts.xlsx Excel data. Followed the below suggested steps for this: 

#### Python dictionary methods extracting and transforming steps: 

Import the contacts.xlsx file into a DataFrame.

Iterate through the DataFrame, converting each row to a dictionary.

Iterate through each dictionary, doing the following:

* Extract the dictionary values from the keys by using a Python list comprehension.
* Add the values for each row to a new list.
* Create a new DataFrame that contains the extracted data.
* Split each "name" column value into a first and last name, and place each in a new column.
* Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.

#### Regular expressions methods extracting and transforming steps: 

Import the contacts.xlsx file into a DataFrame.

Extract the "contact_id", "name", and "email" columns by using regular expressions.

Create a new DataFrame with the extracted data.

Convert the "contact_id" column to the integer type.

Split each "name" column value into a first and a last name, and place each in a new column.

Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.

### 4.    Create the Crowdfunding Database
Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site.

Use the information from the ERD to create a table schema for each CSV file.

Specify the data types, primary keys, foreign keys, and other constraints.

Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

Create a new Postgres database, named crowdfunding_db.

Using the database schema, create the tables in the correct order to handle the foreign keys.

Verify the table creation by running a SELECT statement for each table.

Import each CSV file into its corresponding SQL table.

Verify that each table has the correct data by running a SELECT statement for each.

## Dependencies
The following libraries were used in one or more code files:
pandas, numpy, datetime

## The Dataset
Authors downloaded the provided .csv files including crowdfunding and contacts. 
The authors created additional .csv from the ETL process. These .csv data files can be found in the Resources folder in main. 

## What is included in the Repository
1.    In the main branch, you can view the data extraction and transformation process by opening this file: ETL_Mini_Project_Starter_Code.ipynb. 

2. Creating the DataFrames was broken into two parts: 

**Part 1:** Creating the Category and Subcategory DataFrames and Creating the Campaign DataFrame was completed by Mandy. 

**Part 2:** Creating the Contacts DataFrame was completed by Tim. Tim used both Python dictionary methods and regular expressions for extracting and transforming the data. 

3. Creating the Crowdfunding Database was broken into two parts: 

**Part 1:** Creating the ERD in Quick DBD was completed by Xueyi and Mari. The ERD sketch and the table schema can be found in the main folder. 

**Part 2:** Creating the Postgre Database was completed by Richard.  

## Authors
Mari Awaisi, Ricky Bialick, Mandy Cisler, Tim Haawke, Xueyi, Lu
