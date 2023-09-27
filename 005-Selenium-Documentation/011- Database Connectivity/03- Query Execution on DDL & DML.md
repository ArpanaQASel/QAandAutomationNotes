## Query Execution: DDL and DML: ##

---

**DDL (Data Definition Language) Example:**

~~~
CREATE DATABASE ExampleDB;

USE ExampleDB;

CREATE TABLE Users (

ID INT AUTO\_INCREMENT PRIMARY KEY,

Name VARCHAR(50),

Age INT

);
~~~
In this DDL example, we create a database called ExampleDB and a table called Users.

---

**DML (Data Manipulation Language) Example:**

~~~
INSERT INTO Users (Name, Age) VALUES ('Alice', 30);

INSERT INTO Users (Name, Age) VALUES ('Bob', 35);

UPDATE Users SET Age = 40 WHERE Name = 'Alice';

DELETE FROM Users WHERE Name = 'Bob';

~~~

In this DML example, we insert data into the Users table, update a record, and delete a record.

---
