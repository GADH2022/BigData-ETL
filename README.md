# BigData-ETL
For this project I put my ETL skills to the test. 
Many of Amazon's shoppers depend on product reviews to make a purchase. 
Amazon makes these datasets publicly available. They are quite large and can exceed the capacity of local machines.
One dataset alone contains over 1.5 million rows; with over 40 datasets, data analysis can be very demanding on the average local computer.
My first goal will be to perform the ETL process completely in the cloud and upload a DataFrame to an RDS instance. 
The second goal will be to use PySpark or SQL to perform a statistical analysis of selected data.

Part 1:
Extract two Amazon customer review datasets, transform each dataset into four DataFrames, and load the DataFrames into an RDS instance.
1.Extracted data - Two Amazon customer review datasets into Spark DataFrames. One was for Watches and one was for Toys.
2.Transformed data - Created four dataframes from each dataset based off the information extracted:
"review_id_df" DataFrame with appropriate columns and datatypes
![review](https://user-images.githubusercontent.com/111449865/223537835-b783f318-8d1c-478b-8da5-41ec0cad5668.png)

"products_df" DataFrame that drops the duplicates on the "product_id" and "product_title" columns
![products](https://user-images.githubusercontent.com/111449865/223537306-eeaa2da7-9496-48cd-a2fe-3db61f6a6953.png)

"customers_df" DataFrame that groups the data on the "customer_id" by the number of times a customer reviewed a product
![customers](https://user-images.githubusercontent.com/111449865/223537359-c997877b-0721-40ad-9ca0-84746db364ed.png)

"vine_df" DataFrame that has the "review_id", "star_rating", "helpful_votes", "total_votes", and "vine" columns
![vine](https://user-images.githubusercontent.com/111449865/223537417-9dde6cc5-2af9-4180-b5b1-3d35d3801b69.png)

3.Load data - Exported each DataFrame into the RDS instance to create four tables for each dataset.
![ToSql](https://user-images.githubusercontent.com/111449865/223537484-8bc6e983-43d1-4739-9d92-dee52b47b5e6.png)

Tools used:
Google Colab, AWS, Spark, postgresql, java, hadoop

