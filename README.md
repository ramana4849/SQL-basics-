# SQL-basics-
# SQL(structured query language)

## INTRODUCTION

SQL is Structured Query Language, which is a programming language for storing, manipulating and retrieving data stored in a relational database.

SQL is the standard language for Relational Database System. All the Relational Database Management Systems (RDMS) like MySQL, MS Access, Oracle, Sybase, Informix, Postgres and SQL Server use SQL as their standard database language.

## SQL Process
When a SQL command is executed in any RDBMS, the system determines the best way to carry out your command and SQL engine figures out how to interpret the task.

Components like Query Dispatcher, Optimization Engines, Classic Query Engine, SQL Query Engine etc are involved in this process.

Note: A classic query engine handles all the non-SQL queries, but a SQL query engine won't handle logical files.

## common SQL commands
SQL Commands
The standard SQL commands to interact with relational databases are CREATE, SELECT, INSERT, UPDATE, DELETE and DROP. These commands can be classified into the following groups based on their nature,

### 1.DDL - Data Definition Language
DDL is short name of Data Definition Language, which deals with database schemas and descriptions, of how the data should reside in the database.

- CREATE-create a new table, view for a table or other object in the database
- ALTER - modifies an existing database object, such as a table
- DROP - deletes an entire table, a view of a table or other objects in the database
- TRUNCATE - remove all records from a table, including all spaces allocated for the records are removed
- COMMENT - add comments to the data dictionary
- RENAME - rename an object
 
### 2.DML - Data Manipulation Language
DML is short name of Data Manipulation Language which deals with data manipulation and includes most common SQL statements such SELECT, INSERT, UPDATE, DELETE etc, and it is used to store, modify, retrieve, delete and update data in a database.

  - SELECT - retrieves records from one or more tables
  - INSERT - creates a record
  - UPDATE - modifies records
  - DELETE - deletes records
  - MERGE - UPSERT operation (insert or update)
  - CALL - call a PL/SQL or Java subprogram
  - EXPLAIN PLAN - interpretation of the data access path
  - LOCK TABLE - concurrency control
 
### 3.DCL - Data Control Language
DCL is short name of Data Control Language which includes commands such as GRANT and mostly concerned with rights, permissions and other controls of the database system.

  - GRANT (Grant privilige(s) to user)
  - REVOKE (Remove granted privilige(s) from a user)
 
### 4.TCL - Transaction Control Language
TCL is short name of Transaction Control Language which deals with a transaction within a database.

  - COMMIT - commits a transaction
  - ROLLBACK - rollback a transaction in case of any error occurs
  - SAVEPOINT - to rollback the transaction making points within groups
  - SET TRANSACTION - specify characteristics of the transaction

## SQL Command Help
 - **ALTER TABLE**:
 
   ALTER TABLE lets you add columns to a table in a database.

   #### ALTER TABLE table_name ADD column_name datatype;

 

  - **AND**

    AND is an operator that combines two conditions. Both conditions must be true for the row to be included in the result set.

    #### SELECT column_name(s) FROM table_name WHERE column_1 = value_1 AND column_2 = value_2;

 

 - **AS**

   AS is a keyword in SQL that allows you to rename a column or table using an alias.

   #### SELECT column_name AS 'Alias' FROM table_name;

 

 - **AVG()**

   AVG() is an aggregate function that returns the average value for a numeric column.

   #### SELECT AVG(column_name) FROM table_name;

 

- **BETWEEN**

   The BETWEEN operator is used to filter the result set within a certain range. The values can be numbers, text or dates.

  #### SELECT column_name(s) FROM table_name WHERE column_name BETWEEN value_1 AND value_2; 

 

 

- **CASE**

  CASE statements are used to create different outputs (usually in the SELECT statement). It is SQL's way of handling if-then logic.

  #### SELECT column_name, CASE WHEN condition THEN 'Result_1' WHEN condition THEN 'Result_2' ELSE 'Result_3' END FROM table_name;

- **COUNT()**

  COUNT() is a function that takes the name of a column as an argument and counts the number of rows where the column is not NULL.

  #### SELECT COUNT(column_name) FROM table_name;

 

- **CREATE TABLE**

  CREATE TABLE creates a new table in the database. It allows you to specify the name of the table and the name of each column in the table.

  #### CREATE TABLE table_name ( column_1 datatype, column_2 datatype,column_3 datatype );
 

- **DELETE**
  
  DELETE statements are used to remove rows from a table.

  #### DELETE FROM table_name WHERE some_column = some_value;

 

- **GROUP BY**

  GROUP BY is a clause in SQL that is only used with aggregate functions. It is used in collaboration with the SELECT statement to arrange identical data into groups.

  #### SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name;
 

- **HAVING**

  HAVING was added to SQL because the WHERE keyword could not be used with aggregate functions.

  #### SELECT column_name, COUNT(*) FROM table_name GROUP BY column_name HAVING COUNT(*) > value;
 

- **INNER JOIN**

  An inner join will combine rows from different tables if the join condition is true.

  #### SELECT column_name(s) FROM table_1 JOIN table_2 ON table_1.column_name = table_2.column_name;
 

- **INSERT**

   INSERT statements are used to add a new row to a table.

  #### INSERT INTO table_name (column_1, column_2, column_3) VALUES (value_1, 'value_2', value_3);

 

- **IS NULL / IS NOT NULL**

  IS NULL and IS NOT NULL are operators used with the WHERE clause to test for empty values.

  #### SELECT column_name(s) FROM table_name WHERE column_name IS NULL;
 

- **LIKE**

  LIKE is a special operator used with the WHERE clause to search for a specific pattern in a column.

  #### SELECT column_name(s) FROM table_name WHERE column_name LIKE pattern;

 

- **LIMIT**
  
  LIMIT is a clause that lets you specify the maximum number of rows the result set will have.

  #### SELECT column_name(s) FROM table_name LIMIT number;

 

- **MAX()**

  MAX() is a function that takes the name of a column as an argument and returns the largest value in that column.

  #### SELECT MAX(column_name) FROM table_name;

 

- **MIN()**

  MIN() is a function that takes the name of a column as an argument and returns the smallest value in that column.

  #### SELECT MIN(column_name) FROM table_name;

 

- **OR**

   OR is an operator that filters the result set to only include rows where either condition is true.

  #### SELECT column_name FROM table_name WHERE column_name = value_1 OR column_name = value_2;

 

- **ORDER BY**

  ORDER BY is a clause that indicates you want to sort the result set by a particular column either alphabetically or numerically.

  #### SELECT column_name FROM table_name ORDER BY column_name ASC | DESC;

 

- **OUTER JOIN**

  An outer join will combine rows from different tables even if the join condition is not met. Every row in the left table is returned in the result set, and if the join condition is not met, then NULL values are used to fill in the columns from the right table.

  #### SELECT column_name(s) FROM table_1 LEFT JOIN table_2 ON   table_1.column_name=table_2.column_name;
 

- **ROUND()**

   ROUND() is a function that takes a column name and an integer as an argument. It rounds the values in the column to the number of decimal places specified by the integer.

  #### SELECT ROUND(column_name, integer) FROM table_name;

 

- **SELECT**

  SELECT statements are used to fetch data from a database. Every query will begin with SELECT.

  #### SELECT column_name FROM table_name;

 

- **SELECT DISTINCT**

  SELECT DISTINCT specifies that the statement is going to be a query that returns unique values in the specified column(s).

  #### SELECT DISTINCT column_name FROM table_name;

 

- **SUM**

  SUM() is a function that takes the name of a column as an argument and returns the sum of all the values in that column.

  #### SELECT SUM(column_name) FROM table_name;

 

- **UPDATE**

  UPDATE statements allow you to edit rows in a table.

  #### UPDATE table_name SET some_column=some_value WHERE some_column = some_value;

 

- **WHERE**

   WHERE is a clause that indicates you want to filter the result set to include only rows where the following condition is true.

   #### SELECT column_name(s) FROM table_name WHERE column_name operator value;

 




