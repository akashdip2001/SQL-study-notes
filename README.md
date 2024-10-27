# What is DataBase ?
An Organised collection of data. A method to manipulate and access the data.

Example:

| F Name | L Name | City | Contact |
|:---:|:---:|:---:|:---:|
| AKashdip | Mahapatra | Haldia | 70xxxxxxxx |
| Rahul | Das | London | 7894561237 |

---

### Table of Contents
1. [Database Types](#Database-Types)
2. [SQL vs MySQL](#SQL-vs-MySQL)
3. [Download SQL](#Download)
4. [ANSI SQL Study Notes](#ANSI-SQL-Study-Notes)
5. [**practical**](#practical)

---
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
## ✈️ [Link](https://dev.mysql.com/downloads/installer/)

<div style="display: flex; justify-content: space-around;">
  <img src="https://github.com/user-attachments/assets/00faaac0-1b47-482a-a777-f80e2cc339f8" alt="python projects" style="width: 45%; height: auto;"/>
  <img src="https://github.com/user-attachments/assets/ebd6157f-fd11-4273-b007-cc5ddce31486" alt="pythonprojects" style="width: 45%; height: auto;"/>
</div>

---
</br>

### GUI & CLI
<img align="right" alt="DBMS" width="750" src="https://github.com/user-attachments/assets/02928922-231e-4441-bacc-9f7592b4bda0">

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
4. [Data Definition Language (DDL) Commands](#ddl-commands)
5. [Data Manipulation Language (DML) Commands](#dml-commands)
6. [Data Control Language (DCL) Commands](#dcl-commands)
7. [Transaction Control Language (TCL) Commands](#tcl-commands)
8. [Constraints in SQL](#constraints-in-sql)
9. [SQL Clauses](#sql-clauses)
10. [Advanced SQL Topics](#advanced-sql-topics)
11. [**practical**](#practical)

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

---

## 4. Data Definition Language (DDL) Commands <a name="ddl-commands"></a>

DDL commands define and manage the structure of a database. Common DDL commands include:

- **CREATE**: To create a new table or database.
- **ALTER**: To modify existing tables.
- **DROP**: To delete tables or databases.

### Examples

```sql
-- Create a table
CREATE TABLE employees (
    employee_id INT PRIMARY KEY,
    name VARCHAR(50),
    department VARCHAR(50)
);

-- Alter table to add a new column
ALTER TABLE employees ADD salary DECIMAL(10, 2);

-- Drop a table
DROP TABLE employees;
```

---

## 5. Data Manipulation Language (DML) Commands <a name="dml-commands"></a>

DML commands manipulate data within tables. Common DML commands include:

- **SELECT**: To retrieve data from a table.
- **INSERT**: To add new data to a table.
- **UPDATE**: To modify existing data.
- **DELETE**: To remove data.

### Examples

```sql
-- Select specific columns
SELECT name, department FROM employees;

-- Insert new data
INSERT INTO employees (employee_id, name, department) VALUES (101, 'Alice', 'HR');

-- Update existing data
UPDATE employees SET department = 'Finance' WHERE name = 'Alice';

-- Delete data
DELETE FROM employees WHERE name = 'Alice';
```

---

## 6. Data Control Language (DCL) Commands <a name="dcl-commands"></a>

DCL commands control access to data within the database.

- **GRANT**: To give user permissions.
- **REVOKE**: To remove user permissions.

### Examples

```sql
-- Grant access
GRANT SELECT ON employees TO user_name;

-- Revoke access
REVOKE SELECT ON employees FROM user_name;
```

---

## 7. Transaction Control Language (TCL) Commands <a name="tcl-commands"></a>

TCL commands handle database transactions to ensure data integrity.

- **COMMIT**: To save changes permanently.
- **ROLLBACK**: To undo changes made within a transaction.
- **SAVEPOINT**: To set a point in a transaction to which you can rollback.

### Examples

```sql
-- Start a transaction
BEGIN TRANSACTION;

-- Update data
UPDATE employees SET salary = salary + 500 WHERE department = 'HR';

-- Commit the transaction
COMMIT;

-- Rollback if needed
ROLLBACK;
```

---

## 8. Constraints in SQL <a name="constraints-in-sql"></a>

Constraints ensure data integrity in a database by enforcing rules on columns.

- **PRIMARY KEY**: Uniquely identifies each row.
- **FOREIGN KEY**: References a primary key in another table.
- **UNIQUE**: Ensures all values are unique.
- **NOT NULL**: Ensures a column cannot be NULL.
- **CHECK**: Validates values in a column based on a condition.

### Example
```sql
CREATE TABLE orders (
    order_id INT PRIMARY KEY,
    product_id INT,
    quantity INT CHECK (quantity > 0),
    FOREIGN KEY (product_id) REFERENCES products(product_id)
);
```

---

## 9. SQL Clauses <a name="sql-clauses"></a>

Clauses are keywords in SQL that perform specific tasks.

- **WHERE**: Filters results based on a condition.
- **GROUP BY**: Groups rows sharing a property.
- **ORDER BY**: Sorts result set.
- **HAVING**: Filters groups based on a condition.
- **LIMIT**: Limits the number of returned rows.

### Examples

```sql
-- Filter with WHERE
SELECT * FROM employees WHERE department = 'Finance';

-- Group with GROUP BY
SELECT department, COUNT(*) FROM employees GROUP BY department;

-- Sort with ORDER BY
SELECT * FROM employees ORDER BY name ASC;

-- Filter groups with HAVING
SELECT department, AVG(salary) FROM employees GROUP BY department HAVING AVG(salary) > 50000;

-- Limit result
SELECT * FROM employees LIMIT 5;
```

---

## 10. Advanced SQL Topics <a name="advanced-sql-topics"></a>

### a. Joins
SQL joins combine rows from two or more tables.

- **INNER JOIN**: Returns records with matching values.
- **LEFT JOIN**: Returns all records from the left table and matched records from the right table.
- **RIGHT JOIN**: Returns all records from the right table and matched records from the left table.
- **FULL JOIN**: Returns records when there’s a match in either table.

```sql
-- Inner join example
SELECT employees.name, departments.department_name
FROM employees
INNER JOIN departments ON employees.department_id = departments.department_id;
```

### b. Subqueries
A query within another query.

```sql
-- Example of subquery
SELECT name FROM employees WHERE salary > (SELECT AVG(salary) FROM employees);
```

### c. Views
A **view** is a virtual table based on the result set of an SQL query.

```sql
-- Create a view
CREATE VIEW high_salary_employees AS
SELECT * FROM employees WHERE salary > 60000;
```

### d. Indexes
Indexes improve the speed of data retrieval.

```sql
-- Create an index on the salary column
CREATE INDEX idx_salary ON employees (salary);
```

---

### Practice Questions
1. Write a query to find the highest-paid employee in each department.
2. Create a query to list all employees hired after 2015.
3. Write a query to list products with no sales.

This structure covers all foundational SQL topics, organized with examples to give you a solid ANSI SQL foundation for job exam.

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# practical

