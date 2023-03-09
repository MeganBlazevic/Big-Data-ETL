# Big-Data-ETL

### Background
This module 22 challenge will be working on our ETL skills.  Many Amazon shoppers utilize product reviews to determine what to purchase.  These reviews are housed in extremely large datasets with millions of rows and datasets.  As the data is so large it can be a chalelnge for locaiton machines.  This project has 2 parts that will work with us utilizing the cloud to process the data; and then working to do a data analysis. 

## Part 1
Extract 2 Amazon customer review datasets, transform each dataset into 4 dataframes, and load the dataframes into an RDS instance.

### Extract the Data
Picking two sifferent data sets from our S3 Amazon AWS review files. Read in each of the datasets utilizng the correct headers and sep parameters. Get the number of rows in the dataset. 

### Transform the Data
For each datset use the schema.sql file lcoated in the resources starter code to create the four data frames as follows.
- Create the "review_id_df" dataframe with the appropriate columns and data types
- Create the "products_df" dataframe that drops the duplicates in the "product_id" and "product_title" columns
- Create the "customers_df" datatframe that groups the data by the "customer_id" by the number of times a customer reviewd a product. 
- Create the "vine_df" data frame that has the "review_id", "star_rating", "helpful_vots", "total_votes", and "vine" columns.

### Load the data into an RDS instance
Export each dataframe in the RDS instance to create 4 tables for each dataset

## Part 2 | Optional
Extract 2 Amazon customer review datasets and use either SQL or PySpark to analyze whether reviews form Amazon's Vine program are trustworthy. 

Within Amazon's vine program, those that review the roducts receive free products in exchange for their reviews. Several policites are in place in an attempt to reduce the bias of the reviews.  But - are these reviews trustrowthy?  Part 2, would like us to invinvestigate if the reviews are free of bias; utilzing PySpark or SQL to analyze the datta.

- Using Spark via Colab; extract and transform the data and load into an SQL table on my RDS account. 
- What could be done to reduce the noise in the data? (Ex. filtering for reviews that meet a certian criteria for helpful votes, total votes, etc. )
- Submit a summary of findings and analysis. 

## Important for Submission
- Download the Colab notebook as .ipynb and upload to part-1 folder of the git repository
- Do NOT clear outputs in the file, and detele any passwords and endpoint for RDS.
- If doing part 2 - copy the SQL queies into .swl file sna duplad to part-2 folder.
- Make sure all Amazon AWS is cleared


