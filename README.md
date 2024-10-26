# What is DataBase ?
An Organised collection of data. A method to manipulate and access the data.

Example:

| F Name | L Name | City | Contact |
|:---:|:---:|:---:|:---:|
| AKashdip | Mahapatra | Haldia | 70xxxxxxxx |
| Rahul | Das | London | 7894561237 |

---

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

---

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
- A type of DBMS specifically designed for relational databases.
- Data is stored in tables and can be related based on key values.

| Feature           | DBMS                                 | RDBMS                                     |
|-------------------|--------------------------------------|-------------------------------------------|
| Structure         | Hierarchical or network-based       | Table-based                               |
| Data Integrity    | Limited                             | Enforced through constraints and keys     |
| Example           | XML files, File systems             | MySQL, PostgreSQL, SQL Server             |

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

This structure covers all foundational SQL topics, organized with examples to give you a solid ANSI SQL foundation for your job exam. Good luck!



