# Pipeline for Data Analysis with PySpark
In this proyect where are gone practice the use of PySpark with a DataSet from Keggle. The proyect use **ETL** (Extract, Transform and Load) 
with this one were are going to implement a Pipeline that is going to receive a Dataset specified below and transformed in a desired value to uploaded in our DataBase 

Also this proyect is to test my knowledge, for the use of this tecnologies 
 - Python
 - PySpark
 - PostgreSQl

And the capabilites of the Data Analysis, and the use of DataBases

# Resources 

## DataSet 

To use this proyect you will need the following [DataSet](https://www.kaggle.com/datasets/danielsowah123/retail-sales-dataset?resource=download ), is a Retail Sales Dataset from Kaggle. 

The Dataset contains a pretty good amount of columns for the analysis, but for this case we're going to use only the Column "Country" and "Sales Amount"
this to know the sales per region, also this regions where made up by me, the countrys in the regions are the next ones

- Europe
     - Germany
     - France
     - United Kingdom
- America 
     - Canada
     - United States 
- Ocenia
     - Australia
 
## PySpark

For the use of this code you will need PySpark, is easy to install you will only have to use the following command on your terminal

``` terminal
pip install pyspark
```
And a the SQL dependencie

```
pip install pyspark[sql]
```

If you need more help or information I'll recommend the offical guide of Apache Spark. Just [Click Here](https://spark.apache.org/docs/latest/api/python/getting_started/install.html) consult it 


# Pipeline 

The proyect was implemented following the next diagram of the pipeline for the ETL process 

<img width="1060" height="634" alt="image" src="https://github.com/user-attachments/assets/d324edac-9ad3-4de7-a7e1-4a1183c5fcba" />

# Code Functions

# Run

To run succesfully this code you must have the DataSet Downloanded and Pyspark installed. If the Dataset is not in the same Folder as the Code you must change the variable `file_path` with yours, also you will need to provide your password on the `db_access` variable to connect succesfuly with you DataBase, this for the load of the DataFrame Transformed.

Once you acomplish the requierments mentionted before, you wont have any trouble running it. When the file has finished you will get the files uploaded and two Files called `Global_Report_Retail` and `Europe_Report_Retail` in AVRO format, if you wish to get an CSV format just change this in their respective variables with 'csv' 
