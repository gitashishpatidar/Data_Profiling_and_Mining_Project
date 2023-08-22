# FetchRewardsAssessment
This repository contains my submission for FetchRewards Assessment

### First: Review Existing Unstructured Data and Diagram a New Structured Relational Data Model
Please refer to the file: First_New_Structured_Data.pdf<br>
For this question, I have eliminated some columns with lots of missing values to keep the ER diagram simple and easy to understand. <br>
The diagram shows all the tables with all the columns and if an instance is a primary key or foreign key and how each table is connected on different cardinality levels with other tables.

### Second: Write a query that directly answers a predetermined question from a business stakeholder
Please refer to the file: Second_predetermined_Queries.pdf<br>
I have written these queries using the DBeaver tool for PostgreSQL to answer the predetermined questions. The schema defined in the first question is used to create the database and answer these questions.<br>

### Third: Evaluate Data Quality Issues in the Data Provided
Please refer to the file: Third_Data_Quality_Check.ipynb<br>
This file contains all the code from data cleaning and preprocessing to analyzing data for quality checks. Each step is clearly mentioned with comments in the file and data quality issues are summarized in markdown cells in the file itself.<br><br>
Some of the major data quality issues which were found against the new relational data model are:
1) Apart from users, users_receipts, and category_code tables, all other tables have lots of missing data.
2) In the category_code table, we've identified instances where certain categories have missing values represented as NaN for their code. Additionally, we've observed cases where a category exhibits both NaN and another value as its code. This situation introduces inconsistency in the data structure.
3) We've come across a scenario where certain users possess receipts associated with their IDs; however, their corresponding data is absent in the users table. This discrepancy not only creates data inconsistency but also violates the fundamental primary key principle in a database, where data for all users should be consistently present in the Users table.

### Fourth: Communicate with Stakeholders
Please refer to the file: Fourth_ Communicate with Stakeholders.pdf<br>
This is an email directed to Ashton(Fictional Product Manager) talking about data quality issues, ways to resolve them, and optimizing our data assets and, scaling & performance concerns.<br>
