## Task 01: Create a New mysql user 

1. On start menu search for MySQLworkbench and click on the result.

1. In the home page of workbench click on the created instance.

1. Delete if there is any content And copy paste the below command.

   ```
   create user 'sqluser'@'%' identified by 'Password.1!!';
   GRANT ALL PRIVILEGES ON * . * TO sqluser@'%';

   ```
1. Close the instance,

1. Click on the add button "+" to set-up new connection.

1. When the new connection screen pops up name the connection as **local database**.

1. Leave the connection type as default.

1. For the user type **sqluser** and click on test connection.

1. It asks for password type **Password.1!!**.

1. Once you get the success message click on **ok**.

## Task 02: Create a new Database

1. In the workbench Home page select the created connection **local database**.

1. In the query section copy paste the below command to create a sample database and table.

   ```
     -- Create a database
     -- DROP DATABASE IF EXISTS quickstartdb;
     CREATE DATABASE quickstartdb;
     USE quickstartdb;
     
     -- Create a table and insert rows
     DROP TABLE IF EXISTS inventory;
     CREATE TABLE inventory (id serial PRIMARY KEY, name VARCHAR(50), quantity INTEGER);
     INSERT INTO inventory (name, quantity) VALUES ('banana', 150);
     INSERT INTO inventory (name, quantity) VALUES ('orange', 154);
     INSERT INTO inventory (name, quantity) VALUES ('apple', 100);
     
     -- Read
     SELECT * FROM inventory;
     
     -- Update
     UPDATE inventory SET quantity = 200 WHERE id = 1;
     SELECT * FROM inventory;
     
     -- Delete
     DELETE FROM inventory WHERE id = 2;
     SELECT * FROM inventory;
     
     ```
    

1. Click on the thunder sign to execute the query and you can see the database with a table has been created.(refresh schema to see the new database)
