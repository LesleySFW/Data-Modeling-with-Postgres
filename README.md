# Data-Modeling-with-Postgres

### Project Summary

This project builds a data model using postgresql. In the model a music database called sparkifydb which demonstrates a STAR schema is developed and ingested with data from two datasets, song_data and log_data. ETL is performed on both files to process and collect the required data. Prior to this, SQL queries were written to create the needed tables and insert into the table. The ETL was first performed in jupyter notebook etl.ipynb to develop the tables before completing and loading whole dataset in etl.py. The five tables created for the sparkifydb includes 

* **_Songs Table_:**
   This table records details of the songs such as the title, songId, artistId, year and duration. 

* **_Artists Table_:**
   In this table, the records of artists are stored. Artists records such as name, location, longitude and latitude are included in the table

* **_Times Table_:**
   This table comprises the timestamp (ts) in the log_file data. The records are converted to datetime and used to create records such as hour, day, month,and year for the table. 

* **_Users Table_:**
   The users records such as first name, last name, gender, and level are recorded in this table. 

* **_Songplays Table_:**
   Consists of records with page "NextSong". 

### How to run the Scripts

To create the sparkifydb and the tables, run the create_tables.py file. This script imports the sql_queries script responsible for all the queries required to create and insert records into the database. Next, either run the etl.ipynb notebook to notice how each function work or run the etl.py script to add all the data into the database. 

#### Summary of the files

* **_data_:**
    Contains both the log_data and song_data in JSON format
* _**create_tables.py:**_
    Creates the database and tables, drops the database and tables if exists
* **_etl.ipynb_:**
    Notebook for developing the schema, contains functions for etl processing.
* **_etl.py_:**:
    Script for processing and extracting all the data into the various tables in the sparkifydb database
* **_sql_queries.py_:**
    Contains all the queries required for building the schema
* **_test.ipynb_:**
    Checks for constraints such as primary key, not null and data type of the tables created.  
