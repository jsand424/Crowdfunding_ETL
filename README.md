# Crowdfunding ETL Project

***Team Collaborators***
+ [Khushbu Kothari (Khushi)](https://github.com/dakhushi)
+ [Eric Tran](https://github.com/Tadakatsu213)
+ [Jackson](https://github.com/jsand424/Crowdfunding_ETL/tree/main)

## Instructions
The instructions for this mini project are divided into the following subsections:

- Create the Category and Subcategory DataFrames
- Create the Campaign DataFrame
- Create the Contacts DataFrame
- Create the Crowdfunding Database

### Create the Category and Subcategory DataFrames

1. Extract and transform the crowdfunding.xlsx Excel data to create a category DataFrame that has the following columns:

- A "category_id" column that has entries going sequentially from "cat1" to "catn", where n is the number of unique categories

- A "category" column that contains only the category titles
- The following image shows this category DataFrame:
<img width="190" alt="category_DataFrame" src="https://github.com/user-attachments/assets/3001cd43-24f4-426c-9e88-8fcbeb00d60a">

2. Export the category DataFrame as category.csv and save it to your GitHub repository.

3. Extract and transform the crowdfunding.xlsx Excel data to create a subcategory DataFrame that has the following columns:

- A "subcategory_id" column that has entries going sequentially from "subcat1" to "subcatn", where n is the number of unique subcategories

- A "subcategory" column that contains only the subcategory titles
- The following image shows this subcategory DataFrame:
- <img width="250" alt="subcategory_DataFrame" src="https://github.com/user-attachments/assets/c06131cd-7c83-40e0-85a9-57ff22f0349c">
- Export the subcategory DataFrame as subcategory.csv and save it to your GitHub repository.

### Create the Campaign DataFrame
1. Extract and transform the crowdfunding.xlsx Excel data to create a campaign DataFrame has the following columns:

- The "cf_id" column

- The "contact_id" column

- The "company_name" column

- The "blurb" column, renamed to "description"

- The "goal" column, converted to the float data type

- The "pledged" column, converted to the float data type

- The "outcome" column

- The "backers_count" column

- The "country" column

- The "currency" column

- The "launched_at" column, renamed to "launch_date" and with the UTC times converted to the datetime format

- The "deadline" column, renamed to "end_date" and with the UTC times converted to the datetime format

- The "category_id" column, with unique identification numbers matching those in the "category_id" column of the category DataFrame

- The "subcategory_id" column, with the unique identification numbers matching those in the "subcategory_id" column of the subcategory DataFrame
- The following image shows this campaign DataFrame:
- <img width="1074" alt="campaign_DataFrame" src="https://github.com/user-attachments/assets/ff76468b-c864-40a1-adc2-c2b013a58e98">
2. Export the campaign DataFrame as campaign.csv and save it to your GitHub repository.

### Create the Contacts DataFrame
1. Choose one of the following two options for extracting and transforming the data from the contacts.xlsx Excel data:

- **Option 1:** Use Python dictionary methods.

- **Option 2:** Use regular expressions.

2. If you chose Option 1, complete the following steps:

- Import the contacts.xlsx file into a DataFrame.
- Iterate through the DataFrame, converting each row to a dictionary.
- Iterate through each dictionary, doing the following:
- Extract the dictionary values from the keys by using a Python list comprehension.
- Add the values for each row to a new list.
- Create a new DataFrame that contains the extracted data.
- Split each "name" column value into a first and last name, and place each in a new column.
- Clean and export the DataFrame as contacts.csv and save it to your GitHub repository.
3. If you chose Option 2, complete the following steps:
- Import the contacts.xlsx file into a DataFrame.
- Extract the "contact_id", "name", and "email" columns by using regular expressions.
- Create a new DataFrame with the extracted data.
- Convert the "contact_id" column to the integer type.
- Split each "name" column value into a first and a last name, and place each in a new column.
- Clean and then export the DataFrame as contacts.csv and save it to your GitHub repository.

4. Check that your final DataFrame resembles the one in the following image:
- <img width="415" alt="contact_DataFrame_final" src="https://github.com/user-attachments/assets/9c008314-b398-4e0e-a6df-c36db27561f7">

### Create the Crowdfunding Database
1. Inspect the four CSV files, and then sketch an ERD of the tables by using QuickDBDLinks to an external site..
![ERD-physical model design](https://github.com/user-attachments/assets/39dceef9-f4cb-4ac0-a808-28c8607e70f4)
2. Use the information from the ERD to create a table schema for each CSV file.

Note: Remember to specify the data types, primary keys, foreign keys, and other constraints.

3. Save the database schema as a Postgres file named crowdfunding_db_schema.sql, and save it to your GitHub repository.

4. Create a new Postgres database, named crowdfunding_db.

5. Using the database schema, create the tables in the correct order to handle the foreign keys.

6. Verify the table creation by running a SELECT statement for each table.

7. Import each CSV file into its corresponding SQL table.

8. Verify that each table has the correct data by running a SELECT statement for each.

### References
Data for this dataset was generated by edX Boot Camps LLC, and is intended for educational purposes only.
