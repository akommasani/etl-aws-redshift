# etl-aws-redshift
This project create a DWH on redshift cluster for analysis fof songs data. 
The project follow star schema
There is one Fact tables as most of the inquiries are related to song play. 
songplays - records in event data associated with song plays i.e. records with page NextSong
songplay_id, start_time, user_id, level, song_id, artist_id, session_id, location, user_agent
and four Dimension Tables:
    users - users in the app
    user_id, first_name, last_name, gender, level
    songs - songs in music database
    song_id, title, artist_id, year, duration
    artists - artists in music database
    artist_id, name, location, lattitude, longitude
    time - timestamps of records in songplays broken down into specific units
    start_time, hour, day, week, month, year, weekday

The create_table.py contains sql scripts to create the staging and final table needed for analysis of songs data

The etl.py is the data pipeline script that calls the SQL queries for loading the data into stage and destination tables. 
sql_queries.py contains all the necessary SQL statements
