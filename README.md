## ETL Project Description

This project builds on Project 1 by performing ETL on two CSV files that contain air pollution data from 8 cities between the years 2017 and 2020.


<b>Tools: PostgreSQL, PGAdmin, Jupyter Notebook, Python, Pandas.</b>

### Extract 
Loaded 2 csv files from the Resources folder using pd.read_csv.

### Transform
Removed unnecessary columns and renamed Count column on each dataframe, Count_o3 and Count_pm25. I then merged these two df's using a left merge on the Date, Country, and City columns in each, resulting in one df with the counts of o3 and pm25 for each day in each city.

### Load 
Created a schema, using quotes for capitalized column names. Using pg admin, created the database etl_projct2 and within it, the table called merge_counts. I then loaded the data into the database using new_df.to_sql. Finally, I used pd.read_sql_query to confirm that the data was successfully loaded into the database. In addition, I stored a screenshot of the database in the Outputs folder.

![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/pgadin-screenshoot.png)

Jupyter Notebook:

![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/jn1.png)
![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/jn2.png)
![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/jn3.png)
![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/jn4.png)
![Image](https://github.com/markwsutton/ETL-using-Python-SQL/blob/master/Outputs/jn5.png)
