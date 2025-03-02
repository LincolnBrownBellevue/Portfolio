## Apache Spark Data Flow

## Project Purpose

The purpose of this project is to demonstrate familiarity with the Spark ecosystem and ingesting data. 
The components used in this project include:
<ul>
    <li>Apache NiFi</li>
    <li>HDFS</li>
    <li>Hive</li>
    <li>Apache Spark</li>
    <li>Hbase</li>

## Dataset:

Advertising Spend vs Sales Data
https://www.kaggle.com/datasets/brsahan/advertising-spend-vs-sales


## Pipeline Overview

The data will be ingested as an HTTP request using an InvokeHTTP processor in NiFi. From there, the data will be sent to a PutHDFS processor also in my NiFi Flow. After the data has been stored in HDFS, I will create a table schema in Hive and then ingest the data into the table. After the table has been populated with data, I will use PySpark to access the Hive table and retrieve the records, storing them in a dataframe that will be converted into a vector to create a Linear Regression model. After the LR model has been created, trained, and evaluated, I will store the model’s performance metrics in HBase.



