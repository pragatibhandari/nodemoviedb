
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
1. #### Install PostgreSQL relational database. 
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
3. #### Create Node.js express project
    1. Create a new folder called nodemoviedb and change directory.

            mkdir nodemoviedb
            cd nodemoviedb

    2. Initialize Node.js app

            npm init
    3. Install express and body-parser.

            npm install express body-parser

    4. Add start and dev (nodemon) scripts to the package.json file. Then, your package.json file should look like the code below.

            {
            "name": "nodemoviedb",
            "version": "1.0.0",
            "description": "",
            "main": "index.js",
            "scripts": {
                "dev": "nodemon index.js",
                "start": "node index.js",
                "test": "echo \"Error: no test specified\" && exit 1"
                },
            "author": "",
            "license": "ISC",
            "dependencies": {
                "body-parser": "^1.19.0",
                "express": "^4.17.1"
                }
            }

    5. Next, we will install Node postgres library

    npm install pg
And then your package.json file should look like below.

 
    {
    "name": "nodemoviedb",
    "version": "1.0.0",
    "description": "",
     "main": "index.js",
    "scripts": {
        "dev": "nodemon index.js",
        "start": "node index.js",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "author": "",
    "license": "ISC",
    "dependencies": {
        "body-parser": "^1.19.0",
        "express": "^4.17.1",
        "pg": "^8.1.0"
    }
    }
Finally, create index.js file in the root of nodemovied folder and copy followinf code into the file.

    const express = require('express');
    const bodyParser = require('body-parser');

    const app = express();
    app.use(bodyParser.json());

    const port = 3000;

    app.listen(port, () => {
    console.log(`Server is running on port ${port}.`);
    });
Now, you can start the web server using the npm run dev command.    

4. #### Create connection to movie database

5. #### Fetch data using GET
6. #### Add some structure to your project
7. #### Add data using POST
8. #### Implement delete functionality (DELETE)
9. #### Update data using PUT
