# Iintroduction Contents

1. [What is Data ?](#What-is-Data)
2. [What is DataBase ?](#What-is-DataBase)
3. [Data store technique](#Data-store-technique)
4. [Database Types](#Database-Types)
5. [SQL vs MySQL](#SQL-vs-MySQL)
6. [Download SQL](#Download)
7. [ANSI SQL Study Notes](#ANSI-SQL-Study-Notes) ✅
8. [**practical**](#practical) 
9. [**EXAM**](#EXAM) ✅✅


# What is Data

Data is a collection of raw facts. 
#### Example: 
Number, text, etc.

# What is DataBase
An Organised collection of structured data, that is stored access & manipulate electronically to manage efficiently called DataBase.

Example:

| F Name | L Name | City | Contact |
|:---:|:---:|:---:|:---:|
| AKashdip | Mahapatra | Haldia | 70xxxxxxxx |
| Rahul | Das | London | 7894561237 |

---

# Data store technique
```yaml
Data store technique
│
├── Books & file System
│── Flat file System
└── Database
```
<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# Database Types

| **Database Type**             | **Characteristics**                                                                                   | **Examples**                                    |
|--------------------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| | |
| **Relational Databases (RDBMS)** | Use tables (rows and columns), enforce ACID properties, support SQL for querying data.               | MySQL, PostgreSQL, Oracle, SQL Server, SQLite    |
| | |
| **NoSQL Databases**           | Schema-less, handle unstructured or semi-structured data, ideal for distributed systems.             | MongoDB, Cassandra, DynamoDB, Redis, Couchbase   |
| | |
| - **Key-Value Stores**        | Data stored as key-value pairs, highly performant for simple read/write operations.                  | Redis, DynamoDB, Riak, Memcached                 |
| | |
| - **Document Stores**         | Store data in JSON-like documents, flexible and often used in web apps.                             | MongoDB, Couchbase, Firebase Firestore           |
| | |
| - **Column-Family Stores**    | Data organized in columns, efficient for analytical and large-scale data applications.              | Cassandra, HBase, Google Bigtable                |
| | |
| - **Graph Databases**         | Optimized for handling and querying data with complex relationships (e.g., social networks).        | Neo4j, Amazon Neptune, ArangoDB, OrientDB       |
| | |
| **Object-Oriented Databases (OODBMS)** | Store data as objects, similar to objects in programming languages like Java or C#.               | db4o, ObjectDB, Versant Object Database          |
| | |
| **Time-Series Databases (TSDB)** | Optimized for time-stamped data (e.g., metrics, logs, and IoT data).                               | InfluxDB, Prometheus, TimescaleDB                |
| | |
| **Graph Databases**           | Store data in nodes and edges, ideal for applications involving connections and networks.           | Neo4j, Amazon Neptune, ArangoDB                  |
| | |
| **Columnar Databases**        | Store data in columns rather than rows, optimized for analytics and data warehousing.               | Apache HBase, Amazon Redshift, Google Bigtable   |
| | |
| **In-Memory Databases**       | Data stored in-memory for fast access, suitable for real-time applications.                         | Redis, Memcached, SAP HANA                       |
| | |
| **NewSQL Databases**          | Combine SQL with NoSQL scalability, maintaining ACID compliance for distributed systems.            | CockroachDB, Google Spanner, VoltDB              |
| | |
| **Embedded Databases**        | Lightweight databases embedded within applications, often file-based.                              | SQLite, LevelDB, Berkeley DB                     |
| | |
| **Multimodel Databases**      | Support multiple data models (e.g., document, graph, key-value) within a single system.            | ArangoDB, OrientDB, Couchbase                    |

---

# SQL vs MySQL

| **SQL** | **MySQL** |
| --- | --- |
| Structured Query Language, used to talk (access & Changes) to our DB | DBMS which uses SQL to talk with DB |

---

# Download
## ✈️ [Link for Windows](https://dev.mysql.com/downloads/installer/)
## ✈️ [for Linux](https://drive.google.com/file/d/1coREmAmIW34bkyvbZPbR71dONkX0Z8Qv/view?usp=drivesdk)
</br>
<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/user-attachments/assets/00faaac0-1b47-482a-a777-f80e2cc339f8" alt="python projects" style="width: 45%; height: auto;"/>
  <img src="https://github.com/user-attachments/assets/ebd6157f-fd11-4273-b007-cc5ddce31486" alt="pythonprojects" style="width: 45%; height: auto;"/>
</div>

---
</br>

### GUI & CLI
<img align="right" alt="DBMS" width="550" src="https://github.com/user-attachments/assets/02928922-231e-4441-bacc-9f7592b4bda0">

#### You can use SQL with `Workbanch` or `CLI mode` (case sensitive)
```sql
SHOW DATABASES;
```
Output
```go
+--------------------+
| Database           |
+--------------------+
| information_schema |
| mysql              |
| performance_schema |
| sakila             |
| sys                |
| world              |
+--------------------+
```
---

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# ANSI SQL Study Notes
### Table of Contents
1. [Introduction to Databases](#introduction-to-databases)
2. [DBMS vs. RDBMS](#dbms-vs-rdbms)
3. [SQL Basics](#sql-basics)
4. [Data Definition Language (DDL)](#ddl)
5. [Data Manipulation Language (DML)](#dml)
6. [Data Control Language (DCL)](#dcl)
7. [Transaction Control Language (TCL)](#tcl)
8. [Constraints and Their Types](#constraints)
9. [SQL Operators](#sql-operators)
10. [SQL Functions](#sql-functions)
11. [SQL Clauses](#sql-clauses)
12. [Joins and Their Types](#joins)
13. [Subqueries](#subqueries)
14. [Views](#views)
15. [Indexes](#indexes)
16. [**practical**](#practical)
17. [**EXAM**](#EXAM)

---
[<img align="right" alt="DBMS" width="400" src="https://github.com/user-attachments/assets/1d5e3c49-1a80-4f03-8585-247338cd45ab">](https://youtu.be/Hy3qbMAoEJk)

## 1. Introduction to Databases <a name="introduction-to-databases"></a>

A **database** is an organized collection of data that can be accessed, managed, and updated. It is often used to store large volumes of information for easy retrieval, analysis, and manipulation.

**Example:** 
Imagine a company’s employee database, which stores information like employee names, IDs, departments, and salaries.

---

## 2. DBMS vs. RDBMS <a name="dbms-vs-rdbms"></a>

**DBMS (Database Management System):**
- Software for creating, retrieving, updating, and managing data in databases.
- Supports a variety of database models like hierarchical, network, and object-oriented models.

**RDBMS (Relational Database Management System):**

- Store imformation in `Table` form
- A type of DBMS specifically designed for relational databases.
- Data is stored in tables and can be related based on key values.

| Feature                        | DBMS (Database Management System)                                     | RDBMS (Relational Database Management System)                      |
|--------------------------------|----------------------------------------------------------------------|-------------------------------------------------------------------|
| | |
| **Data Structure**             | Data can be organized in hierarchical, network, or object-oriented formats. | Data is always organized in tables (rows and columns).            |
| | |
| **Relationships**              | Generally does not support relationships between data elements.     | Supports relationships through primary and foreign keys.          |
| | |
| **Data Integrity**             | Limited enforcement of data integrity constraints.                  | Enforces data integrity using ACID (Atomicity, Consistency, Isolation, Durability) properties. |
| | |
| **Data Redundancy**            | Higher likelihood of data redundancy due to lack of relational structures. | Reduced redundancy due to normalization in relational tables.     |
| | |
| **Examples**                   | Hierarchical DBMS, Network DBMS, Object-Oriented DBMS               | MySQL, PostgreSQL, Oracle, Microsoft SQL Server                   |
| | |
| **Example Syntax (Insert)**    | `ADD NODE 'Employee' UNDER 'Department'`                             | `INSERT INTO Employees (EmployeeID, Name) VALUES ('E001', 'Alice');` |
| | |
| **Example Syntax (Retrieve)**  | `FIND NODE 'Employee' UNDER 'Department: Sales'`                    | `SELECT Name FROM Employees WHERE DepartmentID = 1;`              |
| | |
| **Scalability**                | Suitable for small to medium-sized applications.                    | Designed to handle larger applications and complex data needs.    |
| | |
| **Multi-user Access**          | Limited support for multi-user access.                              | Strong support for multi-user access and concurrency control.     |

---

Let's break down the difference between **DBMS** and **RDBMS** by showing a concrete example with clear structures to illustrate how data might be organized in each.

### ✅. DBMS Example (Hierarchical DBMS)
In a **Hierarchical DBMS**, data is stored in a tree-like structure, similar to a folder system, where each piece of data (called a **node**) is connected in a parent-child relationship.

#### Scenario:
Imagine we have data for **Departments** and **Employees** where each department has employees.

#### Structure:
```yaml
Department (root node)
│
├── Department: Sales
│   ├── Employee: Alice
│   └── Employee: Bob
│
└── Department: HR
    ├── Employee: Carol
    └── Employee: Dave
```

#### Example Syntax (Hierarchical DBMS):
1. **To add a new employee under a department (e.g., adding Eve in Sales):**
   ```sql
   ADD NODE 'Employee' UNDER 'Department: Sales' SET Attributes(Name="Eve", ID="E002")
   ```

2. **To retrieve all employees in a department (e.g., Sales):**
   ```sql
   FIND NODE 'Employee' UNDER 'Department: Sales'
   ```

In this DBMS, there are no **tables**. Data is organized in a tree, and you access nodes by navigating through the hierarchy.

---

### ✅. RDBMS Example (Relational DBMS)
In an **RDBMS**, data is stored in tables with rows and columns, where tables can relate to each other through keys (e.g., primary keys and foreign keys).

#### Scenario:
We'll use the same **Departments** and **Employees** data, but here they are stored in tables that relate to each other.

#### Structure:
- **Departments Table**
  | DepartmentID | DepartmentName |
  |--------------|----------------|
  | 1            | Sales          |
  | 2            | HR             |

- **Employees Table**
  | EmployeeID | Name  | DepartmentID |
  |------------|-------|--------------|
  | E001       | Alice | 1            |
  | E002       | Bob   | 1            |
  | E003       | Carol | 2            |
  | E004       | Dave  | 2            |

Here, the **DepartmentID** in the **Employees Table** acts as a foreign key that links to the **Departments Table**.

#### Example Syntax (RDBMS):
1. **To add a new employee to the Sales department:**
   ```sql
   INSERT INTO Employees (EmployeeID, Name, DepartmentID) VALUES ('E005', 'Eve', 1);
   ```

2. **To retrieve all employees in the Sales department:**
   ```sql
   SELECT Name FROM Employees WHERE DepartmentID = 1;
   ```

In an **RDBMS**, data is stored in a **tabular form** with relationships between tables, unlike DBMS, where data could be stored hierarchically or in other non-tabular structures.

---

## 3. SQL Basics <a name="sql-basics"></a>

**SQL (Structured Query Language)** is the standard language for interacting with RDBMS. **ANSI SQL** is the standardized version of SQL.

### Basic Syntax
```sql
-- Select all columns from a table
SELECT * FROM table_name;

-- Insert a new row into a table
INSERT INTO table_name (column1, column2) VALUES (value1, value2);

-- Update a row in a table
UPDATE table_name SET column1 = value1 WHERE condition;

-- Delete rows from a table
DELETE FROM table_name WHERE condition;
```

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

## 4. Data Definition Language (DDL) <a name="ddl"></a>

DDL commands are used to define and modify the structure of database objects.

- **CREATE**: Creates tables, views, or other objects.
- **ALTER**: Modifies existing structures.
- **DROP**: Deletes tables, views, or other objects.

### ✈️ Syntax

### **CREATE Table**
```sql
sql> CREATE TABLE employees (
       employee_id INT PRIMARY KEY,
       name VARCHAR(50),
       department VARCHAR(50),
       salary DECIMAL(10, 2)
     );

# Output:
Table 'employees' created successfully.
```

### **ALTER Table**

`The ALTER Command allow us to altering the structure of object like- add a new Column, drop or Rename a Column, add Constraint etc.`

```sql
# 1. Add a New Column
ALTER TABLE employees ADD age INT;

# 2. Rename an Existing Column
ALTER TABLE employees RENAME COLUMN age TO years_of_experience;

# 3. Modify an Existing Column
ALTER TABLE employees MODIFY years_of_experience DECIMAL(3, 1);

# 4. Rename the Table
ALTER TABLE employees RENAME TO staff;

# 5. Add a Constraint
ALTER TABLE employees ADD CONSTRAINT chk_salary CHECK (salary > 0);

# 6. Drop a Column
ALTER TABLE employees DROP COLUMN years_of_experience;

# 7. Drop a Constraint
ALTER TABLE employees DROP CONSTRAINT chk_salary;
```

### **DROP Table**
```sql
sql> DROP TABLE employees;

# Output:
Table 'employees' dropped successfully.
```

---

## 5. Data Manipulation Language (DML) <a name="dml"></a>

DML commands are used to manipulate data in tables.

- **SELECT**: Retrieves data from a table.
- **INSERT**: Adds new data to a table.
- **UPDATE**: Modifies existing data in a table.
- **DELETE**: Removes data from a table.

### Syntax

```sql
-- Select data from a table
SELECT name, department FROM employees;

-- Insert data into a table
INSERT INTO employees (employee_id, name, department, salary) VALUES (101, 'Alice', 'HR', 55000);

-- Update data in a table
UPDATE employees SET salary = 60000 WHERE name = 'Alice';

-- Delete data from a table
DELETE FROM employees WHERE name = 'Alice';
```

### Explane 
### **SELECT Statement**
```sql
# Command Line Interface:
sql> SELECT name, department FROM employees;

# Output:
| name    | department |
|---------|------------|
| Alice   | HR         |
| Bob     | Finance    |
| Charlie | IT         |
```

### **INSERT Statement**
```sql
# Command Line Interface:
sql> INSERT INTO employees (employee_id, name, department, salary) 
       VALUES (101, 'Alice', 'HR', 55000);

# Output:
1 row inserted.
```

### **UPDATE Statement**
```sql
# Command Line Interface:
sql> UPDATE employees SET salary = 60000 WHERE name = 'Alice';

# Output:
1 row updated.
```

### **DELETE Statement**
```sql
# Command Line Interface:
sql> DELETE FROM employees WHERE name = 'Alice';

# Output:
1 row deleted.
```

---

## 6. Data Control Language (DCL) <a name="dcl"></a>

DCL commands manage permissions and access controls.

- **GRANT**: Grants user permissions on database objects.
- **REVOKE**: Removes user permissions.

### Example Syntax and Output

```sql
-- Grant SELECT permission to a user
GRANT SELECT ON employees TO user_name;

-- Revoke SELECT permission from a user
REVOKE SELECT ON employees FROM user_name;
```

---

## 7. Transaction Control Language (TCL) <a name="tcl"></a>

TCL commands control database transactions.

- **COMMIT**: Saves changes made in the current transaction.
- **ROLLBACK**: Reverts changes made in the current transaction.
- **SAVEPOINT**: Sets a point in a transaction to which you can rollback.

### Example Syntax and Output

```sql
-- Start a transaction
BEGIN TRANSACTION;

-- Update statement
UPDATE employees SET salary = salary + 500 WHERE department = 'HR';

-- Commit the transaction
COMMIT;

-- Rollback if needed
ROLLBACK;
```

---

## 8. Constraints and Their Types <a name="constraints"></a>

Constraints enforce data integrity by defining rules for columns.

- **PRIMARY KEY**: Uniquely identifies each row in a table.
- **FOREIGN KEY**: References a primary key in another table.
- **UNIQUE**: Ensures unique values in a column.
- **NOT NULL**: Prevents null values.
- **CHECK**: Enforces a condition on values.

### Example Syntax and Output

```sql
-- Create a table with constraints
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    product_id INT NOT NULL,
    quantity INT CHECK (quantity > 0),
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);
```

---

## 9. SQL Operators <a name="sql-operators"></a>

Operators in SQL are used for calculations and comparisons.

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`
- **Comparison Operators**: `=`, `<`, `>`, `<=`, `>=`, `<>`
- **Logical Operators**: `AND`, `OR`, `NOT`

### ✅ Syntax 

```sql
-- Arithmetic operators
SELECT salary * 1.1 AS increased_salary FROM employees;

-- Comparison operators
SELECT * FROM employees WHERE salary > 50000;

-- Logical operators
SELECT * FROM employees WHERE department = 'HR' AND salary > 50000;
```

### ✈️ Explane 
### **Arithmetic Operators**
```sql
# Command Line Interface:
sql> SELECT salary * 1.1 AS increased_salary FROM employees;

# Output:
| increased_salary |
|------------------|
| 60500.00         |
| 66000.00         |
| 71500.00         |
```

### **Comparison Operators**
```sql
# Command Line Interface:
sql> SELECT * FROM employees WHERE salary > 50000;

# Output:
| employee_id | name  | department | salary |
|-------------|-------|------------|--------|
| 102         | Bob   | Finance    | 55000  |
| 103         | Carol | IT         | 60000  |
```

---

## 10. SQL Functions <a name="sql-functions"></a>

SQL functions perform operations on data.

- **Aggregate Functions**: Operate on multiple rows (e.g., `COUNT`, `SUM`, `AVG`, `MIN`, `MAX`).
- **String Functions**: Manipulate string values (e.g., `UPPER`, `LOWER`, `CONCAT`).
- **Date Functions**: Work with date values (e.g., `NOW`, `DATEADD`).

### ✅ Syntax

```sql
-- Aggregate function
SELECT COUNT(*) AS total_employees FROM employees;

-- String function
SELECT UPPER(name) AS uppercase_name FROM employees;

-- Date function
SELECT NOW() AS current_date_time;
```

### ✈️ Explane
### **Aggregate Functions**
```sql
# Command Line Interface:
sql> SELECT COUNT(*) AS total_employees FROM employees;

# Output:
| total_employees |
|-----------------|
| 5               |
```

### **String Functions**
```sql
# Command Line Interface:
sql> SELECT UPPER(name) AS uppercase_name FROM employees;

# Output:
| uppercase_name |
|----------------|
| ALICE          |
| BOB            |
| CHARLIE        |
```

---

## 11. SQL Clauses <a name="sql-clauses"></a>

SQL clauses refine query results.

- **WHERE**: Filters results based on a condition.
- **GROUP BY**: Groups results by one or more columns.
- **ORDER BY**: Sorts the result set.
- **HAVING**: Filters groups.
- **LIMIT**: Limits the number of results returned.

### ✅ Syntax

```sql
-- WHERE clause
SELECT * FROM employees WHERE department = 'Finance';

-- GROUP BY clause
SELECT department, COUNT(*) FROM employees GROUP BY department;

-- ORDER BY clause
SELECT * FROM employees ORDER BY salary DESC;

-- HAVING clause
SELECT department, AVG(salary) FROM employees GROUP BY department HAVING AVG(salary) > 50000;

-- LIMIT clause
SELECT * FROM employees LIMIT 5;
```

### ✈️ Explane
### **WHERE Clause**
```sql
# Command Line Interface:
sql> SELECT * FROM employees WHERE department = 'Finance';

# Output:
| employee_id | name | department | salary |
|-------------|------|------------|--------|
| 102         | Bob  | Finance    | 55000  |
```

### **GROUP BY Clause**
```sql
# Command Line Interface:
sql> SELECT department, COUNT(*) FROM employees GROUP BY department;

# Output:
| department | count |
|------------|-------|
| HR         | 2     |
| IT         | 1     |
| Finance    | 1     |
```

### **ORDER BY Clause**
```sql
# Command Line Interface:
sql> SELECT * FROM employees ORDER BY salary DESC;

# Output:
| employee_id | name    | department | salary |
|-------------|---------|------------|--------|
| 103         | Charlie | IT         | 60000  |
| 102         | Bob     | Finance    | 55000  |
| 101         | Alice   | HR         | 50000  |
```

---

## 12. Joins and Their Types <a name="joins"></a>

Joins combine rows from two or more tables.

- **INNER JOIN**: Returns rows with matching values in both tables.
- **LEFT JOIN**: Returns all rows from the left table and matched rows from the right.
- **RIGHT JOIN**: Returns all rows from the right table and matched rows from the left.
- **FULL JOIN**: Returns rows with a match in either table.

### ✅ Syntax 

```sql
-- Inner join example
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;

-- Left join example
SELECT employees.name, departments.department_name
FROM employees
LEFT JOIN departments ON employees.department_id = departments.department_id;
```

### ✈️ Explane
### **INNER JOIN**
```sql
# Command Line Interface:
sql> SELECT employees.name, departments.department_name
       FROM employees
       INNER JOIN departments ON employees.department_id = departments.department_id;

# Output:
| name   | department_name |
|--------|-----------------|
| Alice  | HR             |
| Bob    | Finance        |
```

### **LEFT JOIN**
```sql
# Command Line Interface:
sql> SELECT employees.name, departments.department_name
       FROM employees
       LEFT JOIN departments ON employees.department_id = departments.department_id;

# Output:
| name   | department_name |
|--------|-----------------|
| Alice  | HR             |
| Bob    | Finance        |
| Carol  | NULL           |
```

---

## 13. Subqueries <a name="subqueries"></a>

Subqueries are queries embedded within other queries to return a result used in the outer query.

### Example Syntax and Output

```sql
-- Subquery example to find employees with above-average salary
sql> SELECT name FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);

# Output:
| name    |
|---------|
| Bob     |
| Charlie |
```

---

## 14. Views <a name="views"></a>

A view is a virtual table based on a query result. Views provide security by limiting user access to specific data.

### ✅ Syntax

```sql
-- Create a view
CREATE VIEW high_salary_employees AS
SELECT * FROM employees WHERE salary > 60000;

-- Select from view
SELECT * FROM high_salary_employees;
```

### ✈️ Explane
```sql
# Command Line Interface:
sql> CREATE VIEW high_salary_employees AS
       SELECT * FROM employees WHERE salary > 60000;

# Output:
View 'high_salary_employees' created successfully.

sql> SELECT * FROM high_salary_employees;

# Output:
| employee_id | name    | department | salary |
|-------------|---------|------------|--------|
| 104         | David   | IT         | 75000  |
```

---

## 12. Indexes

### **Create an Index**
```sql
# Command Line Interface:
sql> CREATE INDEX idx_salary ON employees (salary);

# Output:
Index 'idx_salary' created on 'employees' table.

sql> SELECT name FROM employees WHERE salary > 50000;

# Output (using index for faster retrieval):
| name    |
|---------|
| Bob     |
| Charlie |
```

---

## 15. Indexes <a name="indexes"></a>

Indexes improve the speed of data retrieval operations on a database table. However, they can slow down data modification.

### Example Syntax and Output

```sql
-- Create an index on the salary column
CREATE INDEX idx_salary ON employees (salary);

-- Use index in a query
SELECT name FROM employees WHERE salary > 50000;
```

---

### Practice Questions
1. Write a query to find the highest-paid employee in each department.
2. Create a query to list all employees hired after 2015.
3. Write a query to list products with no sales.

This structure covers all foundational SQL topics, organized with examples to give you a solid ANSI SQL foundation for job exam.

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# practical
### [pdf Notes](https://drive.google.com/file/d/1coREmAmIW34bkyvbZPbR71dONkX0Z8Qv/view?usp=drivesdk)
# 1) Creat Databases 

```go
✅ 1) GUI option ----> CREATE SCHEMA `schema_01` ;
✅ 2) GUI Command ---> CREATE DATABASE first_db
✅ 3) CLI Command ---> CREATE DATABASE first01_db;
```
| GUI option | GUI Command |
| --- | --- |
| `CREATE SCHEMA `schema_01` ;` | `CREATE DATABASE first_db` |

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/user-attachments/assets/427ca07d-9348-4354-a02b-3736ea929383" alt="python projects" style="width: 45%; height: auto;"/>
  <img src="https://github.com/user-attachments/assets/6d059a42-cb50-4e3c-9d18-ee34e96e974d" alt="pythonprojects" style="width: 45%; height: auto;"/>
</div>

---
# 2) Chouse a Database (or Enter or Use a DB) using CLI & check

```sql
USE first_db;
select database();
```

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/user-attachments/assets/665e8edc-4e57-4289-aa72-d93cb9dbba1c" alt="python projects" style="width: 45%; height: auto;"/>
  <img src="https://github.com/user-attachments/assets/c9cc5f7e-ba0e-47b6-bb82-b85ac116a999" alt="pythonprojects" style="width: 45%; height: auto;"/>
</div>

# 3) Delete Database
```sql
 DROP DATABASE first2_db;
```
![Screenshot (45)](https://github.com/user-attachments/assets/0a9c7281-dfc6-47d8-b9b0-009dbb134da7)

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# EXAM

# 1) Problam 01
![SQL_01](https://github.com/user-attachments/assets/75228002-093a-4ab9-86fb-2255c29ae215)
### QUERY ✅
```sql
SELECT
  Account_Type_ID,
  COUNT(*) AS Account_Count
FROM
  Account
GROUP BY
  Account_Type_ID;
```

---
# 2) Problam 02

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/user-attachments/assets/1c94cff0-40e4-4242-a0ea-6bb459598d3c" alt="python projects" style="width: 50%; height: auto;"/>
  <img src="https://github.com/user-attachments/assets/ad066fbd-3ee8-4014-b59b-829378466e12" alt="pythonprojects" style="width: 40%; height: auto;"/>
</div>

### QUERY ⚠️

```sql
SELECT 
    Account_Type_ID, 
    COUNT(*) AS Account_Count
FROM 
    account
GROUP BY 
    Account_Type_ID;

```




