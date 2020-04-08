### Project Summary
A music streaming startup, Sparkify, has grown their user base and song database even more and want to move their data warehouse to a data lake. Their data resides in S3, in a directory of JSON logs on user activity on the app, as well as a directory with JSON metadata on the songs in their app.
You are tasked with building an ETL pipeline that extracts their data from S3, processes them using Spark, and loads the data back into S3 as a set of dimensional tables.

### Database Schema
To complete the project, create a star schema optimized for queries on song play analysis. This includes the following tables.

## Fact Table
songplays - records in log data associated with song plays i.e. records with page NextSong songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent

## Dimension Tables
users - users in the app user_id, first_name, last_name, gender, level

songs - songs in music database song_id, title, artist_id, year, duration

artists - artists in music database artist_id, name, location, latitude, longitude

time - timestamps of records in songplays broken down into specific units start_time, hour, day, week, month, year, weekday

## Template Files
etl.py reads data from S3, processes that data using Spark, and writes them back to S3

dl.cfg contains AWS credentials

README.md provides discussion on the process and decisions

## Steps to Follow
Load data from S3.

Process the data into analytics tables using Spark.

Load them back into S3.

## ETL Pipeline
Script executes Apache Spark SQL commands to read source data (JSON files) from S3 to memory as Spark DataFrames.

In memory, data is further manipulated to analytics DataFrames.

Analytics DataFrames are stored back to S3 as Spark parquet files.