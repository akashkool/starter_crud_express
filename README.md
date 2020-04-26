# CRUD API using Express with PostgreSQL

Start a CRUD API quickly using Node, Express & Postgres.

Serves four requests (get, post, put, delete) from one page with a separate function for each.

**Dependencies**

We use **express** to serve the API, **body-parser** to parse responses, **postgres** for the database, **knex** as the query engine, **dotenv** to protect environment variables, **helmet** to add proper headers, **cors** to prevent/allow XSS, **morgan** as our logger, and **nodemon** as a dev dependency to watch for changes.

All dependencies are included in the cloned project.

**1. Clone the repo**

```
git clone https://github.com/akashkool/starter_crud_express.git
```

**2. CD into the project**

```
cd starter_crud_express
```

**3. Install dependencies**

```
npm install
```

**4. Start Postgres**

```
brew services start postgresql
```

**5. Create a database**

Change the database name to whatever you would like to name the database. Be sure to also change the database name in server.js to whatever you name the database.

```
createdb crud-starter-api
```

**6. Create a database table**

Open psql console or PG Admin and run the following command. Change the table name to whatever you would like to name the table.

```
CREATE TABLE users (
 id serial PRIMARY KEY,
 first VARCHAR(100),
 last VARCHAR(100),
 email text UNIQUE NOT NULL,
 phone VARCHAR(100),
 location VARCHAR(100),
 hobby VARCHAR(100),
 added TIMESTAMP NOT NULL
);
```
**7. Start API & Test via Postman**

Run command npm start to run the API server & test it via Postman.

**8. End points explained**
 ```
  GET     -  /user gives all users.
  POST    -  /user create new users.
  PUT     -  /user update existing users by id.
  Delete  -  /user delete user by id.
````
  
  ```Look into code to understand JSON request```

