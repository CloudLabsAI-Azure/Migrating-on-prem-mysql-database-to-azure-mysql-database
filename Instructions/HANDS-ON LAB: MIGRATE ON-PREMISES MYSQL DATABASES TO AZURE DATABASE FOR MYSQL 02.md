## Task 1: Create a Database using MySQL workbench

1. In the desktop select start menu

1. Search for MySQL workbench.

1.  Click on the Default instance created.

   ![Workbench](./media/workbench.png)

1. Once the editor opens up copy paste the below query to create a database and a table  

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
1. Click on the execute button.

1. verify whether the database is created by clicking on schema on the left.(refresh it)

  >**Note:** Don't close the page as the steps are continued in the next exercise.

## Proceed to next exercise.

