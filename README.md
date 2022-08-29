
# Node Movie Database


In this project movie REST API is created and the data is saved persistently to a database.



## This project includes the following topics

- install PostgreSQL relational database
- create database and tables using the SQL Shell (psql)
- use PostgreSQL with Node.js and express
- connect into database using Node.js
- fetch data from the database using Node.js
- create REST api with PostgreSQL database


## Steps taken during this project
1. #### install PostgreSQL relational database. 
  PostgreSQL installation provides some useful tools for database administration. One of these tools is SQL Shell that you can use to execute SQL statements to you database. 

2. #### Create database and table for the movies
    1. Open the SQL Shell (psql) command line tool.
    2. Connect to the postgres database using postgres user.
    3. Type following SQL statement to SQL Shell. That will create a new database called movie.
    
            CREATE DATABASE movie;

    4. Next, we will connect to the movies database by typing following command in the SQL Shell.

            \c movie
    5. Then, we will create movies table to our movie database. 

            CREATE TABLE movies (
            id serial PRIMARY KEY,
            title VARCHAR (200) NOT NULL,
            director VARCHAR (200) NOT NULL, 
            year INTEGER NOT NULL 
            );
    6. Finally, you can type \d command in the SQL Shell to verify that movies table exists.

3. #### Create connection to movie database

4. #### Fetch data using GET
5. #### Add some structure to your project


6. #### Add data using POST
7. #### Implement delete functionality (DELETE)
8. #### Update data using PUT
