# Databricks---GreenYellow-NYC-Taxi-ETL
ETL on NYC Green and Yellow Taxi datasets

New York City has two types of taxies: yellow and green; they are widely recognizable symbols of the city. Taxis painted yellow (medallion taxis) can pick up passengers from anywhere in the five boroughs. Those painted apple green (street hail livery vehicles, commonly known as "boro taxis"), which began to appear in August 2013, are allowed to pick up passengers in Upper Manhattan, the Bronx, Brooklyn, Queens (excluding LaGuardia Airport and John F. Kennedy International Airport), and Staten Island. 

Considering the Volume, Velocity and Veracity aspects of the data, We have decided to build a Data Lake using Databricks Lake House Platform which is going to be a single store for raw intermittent and processed data. 

We will be using mainly 2 datasets - A green taxi dataset, and a Yellow taxi dataset.

In this repository we will perform ETL Operation on the Green and Yellow Taxi datasets. 
We will first upload the datasets in the DBFS. 
In our Notebook we will perform ETL on both the datasets. We will create a temporary view of the raw datasets and then filter the records

Filter the GreenTripView data as per the below filter conditions –
1.	lpep_pickup_datetime and lpep_pickup_datetime should not be same
2.	record will be considered on for year 2019
3.	passenger_count should not be zero
4.	trip_distance should not be zero
5.	fare_amount should not be zero
6.	total_amount should not be zero
7.	PULocationID should not be null
8.	DOLocationID should not be null

Filter the YellowTripView data as per the below filter conditions –
1.	tpep_pickup_datetime and tpep_pickup_datetime should not be same
2.	record will be considered on for year 2019
3.	passenger_count should not be zero
4.	trip_distance should not be zero
5.	fare_amount should not be zero
6.	total_amount should not be zero
7.	PULocationID should not be null
8.	DOLocationID should not be null

After we filter the datasets we will create a DELTA TABLE for both the datasets and store it in a specific location.

