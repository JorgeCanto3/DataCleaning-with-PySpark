# Pipeline for Data Analysis with PySpark
In this project, we implement an **ETL (Extract, Transform, and Load) Data Pipeline** using **PySpark** and a Retail Sales Dataset from **Kaggle**. The pipeline extracts raw transaction records, cleans and transforms the data to calculate regional and country-level sales, loads the processed data into a **PostgreSQL** database, and exports analytical reports in **Avro** (or CSV) format.

This project demonstrates Data Engineering and Data Analysis capabilities using the following technologies:

 - Python
 - PySpark
 - PostgreSQL

And the capabilites of the Data Analysis, and the use of DataBases

# Resources 

## DataSet 

To use this proyect you will need the [Retail Sales Dataset from Kaggle](https://www.kaggle.com/datasets/danielsowah123/retail-sales-dataset?resource=download ), is a Retail Sales Dataset from Kaggle. 

Although the dataset contains multiple columns for transactional analysis, this pipeline focuses primarily on `"Country"` and `"Sales_Amount"` to evaluate sales performance across markets. A custom regional classification was defined as follows:

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

For the use of this code you will need PySpark.You can easily install it via terminal using `pip`:

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

To run succesfully this code you must have the following.

1. If the Dataset is not in the same Folder as the Code you must change the variable `file_path` with yours
2. You must change the credentials with yours. By providing your password on the `db_access` variable, this for the load of the DataFrame Transformed.
3. To execute the script you can do this:

```terminal
 python Pipeline_Gtec.py
```
    
   
Once execution finishes, the cleaned records will be uploaded to your PostgreSQL database, and two output report directories will be generated in Avro format:
 -`Global_Report_Retail`
 -`Europe_Report_Retail`
 
 If you wish to get an CSV format, simply change the `.format("avro")` parameter to 'csv' in their respective export variables.
