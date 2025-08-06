## 📘 Oracle Database 19c: Basic SQL — Study Notes

---
---

### 📚 [Contents](#contents)

---

#### 🎬 [Introduction](#-introduction)

* [Why Oracle Database 19c?](#why-oracle-database-19c)
* [What You Should Know](#what-you-should-know)

---

#### 🛠️ [1. Client Tools](#-1-client-tools)

* [1.1 SQL\*Plus](#11-sqlplus)
* [1.2 SQLcl](#12-sqlcl)
* [1.3 SQL Developer](#13-sql-developer)
* [Client Tools Quiz](#client-tools-quiz)

---

#### 📊 [2. SELECT Statements](#-2-select-statements)

* [2.1 Data Types Overview](#21-data-types-overview)
* [2.2 SELECT Statement Clauses](#22-select-statement-clauses)
* [2.3 Expressions in SELECT and WHERE](#23-expressions-in-select-and-where)
* [2.4 Column Aliases](#24-column-aliases)
* [2.5 Subqueries in SELECT](#25-subqueries-in-select)
* [SELECT Chapter Quiz](#select-chapter-quiz)

---

#### 📘 [3. Data Dictionary](#-3-data-dictionary)

* [3.1 DESCRIBE in SQL\*Plus](#31-describe-in-sqlplus)
* [3.2 Using DDL Command in SQLcl](#32-using-ddl-command-in-sqlcl)
* [Data Dictionary Quiz](#data-dictionary-quiz)

---

#### 🧵 [4. String Manipulation](#-4-string-manipulation)

* [4.1 Literals](#41-literals)
* [4.2 Concatenation](#42-concatenation)
* [4.3 Alternative Quoting](#43-alternative-quoting)
* [String Manipulation Quiz](#string-manipulation-quiz)

---

#### 🔍 [5. Filtering Rows](#-5-filtering-rows)

* [5.1 WHERE Clause Syntax](#51-where-clause-syntax)
* [5.2 Subqueries in WHERE Clause](#52-subqueries-in-where-clause)
* [5.3 Table Joins and Filtering](#53-table-joins-and-filtering)
* [Filtering Quiz](#filtering-quiz)

---

#### ↕️ [6. Sorting Rows](#-6-sorting-rows)

* [6.1 ORDER BY Clause](#61-order-by-clause)
* [6.2 Collation Rules](#62-collation-rules)
* [Sorting Quiz](#sorting-quiz)

---

#### 🧮 [7. Single-Row Functions](#-7-single-row-functions)

* [7.1 Numeric Functions](#71-numeric-functions)
* [7.2 Character Functions (Return Character)](#72-character-functions-return-character)
* [7.3 Character Functions (Return Numeric)](#73-character-functions-return-numeric)
* [7.4 Datetime Functions](#74-datetime-functions)
* [7.5 Conversion Functions](#75-conversion-functions)
* [7.6 General Functions](#76-general-functions)
* [7.7 Listing Functions in SQL Developer](#77-listing-functions-in-sql-developer)
* [Single-Row Functions Quiz](#single-row-functions-quiz)

---

#### 🧢 [8. Aggregation and Multiple-Row Functions](#-8-aggregation-and-multiple-row-functions)

* [8.1 GROUP BY Clause](#81-group-by-clause)
* [8.2 HAVING Clause](#82-having-clause)
* [8.3 Using DISTINCT](#83-using-distinct)
* [Aggregation Quiz](#aggregation-quiz)

---

#### 🔗 [9. Joining Tables](#-9-joining-tables)

* [9.1 ANSI vs Oracle Join Syntax](#91-ansi-vs-oracle-join-syntax)
* [9.2 INNER JOIN](#92-inner-join)
* [9.3 LEFT (OUTER) JOIN](#93-left-outer-join)
* [9.4 RIGHT (OUTER) JOIN](#94-right-outer-join)
* [9.5 FULL (OUTER) JOIN](#95-full-outer-join)
* [9.6 NATURAL JOIN](#96-natural-join)
* [9.7 CROSS JOIN](#97-cross-join)
* [Joins Quiz](#joins-quiz)

---

#### 📚 [10. Using the Oracle Data Dictionary](#-10-using-the-oracle-data-dictionary)

* [10.1 Understanding the Data Dictionary](#101-understanding-the-data-dictionary)
* [10.2 Querying the Data Dictionary](#102-querying-the-data-dictionary)
* [Data Dictionary Quiz](#data-dictionary-quiz)

---

#### 📥 [11. DML: INSERT, UPDATE, DELETE](#-11-dml-insert-update-delete)

* [11.1 INSERT Single Row](#111-insert-single-row)
* [11.2 INSERT Multiple Rows](#112-insert-multiple-rows)
* [11.3 UPDATE Rows](#113-update-rows)
* [11.4 DELETE Rows](#114-delete-rows)
* [DML Quiz](#dml-quiz)

---

#### 🏗️ [12. DDL: Creating Objects](#-12-ddl-creating-objects)

* [12.1 Creating Tables](#121-creating-tables)
* [12.2 Creating Indexes](#122-creating-indexes)
* [12.3 Oracle Specific Tables](#123-oracle-specific-tables)
* [DDL Quiz](#ddl-quiz)

---

#### 🧹 [13. Dropping Objects](#-13-dropping-objects)

* [13.1 Dropping Tables](#131-dropping-tables)
* [13.2 Dropping Indexes](#132-dropping-indexes)
* [13.3 Drop Oracle Specific Tables](#133-drop-oracle-specific-tables)
* [Drop Quiz](#drop-quiz)

---

#### 🎓 [Conclusion & Next Steps](#-conclusion--next-steps)

* [Wrap-up](#wrap-up)
* [Further Learning Resources](#further-learning-resources)

---
---

## Introduction

### 🎥 Learning Oracle Database SQL: Why 19c?

Oracle 19c is a Long-Term Support version, stable and enterprise-ready for database solutions. It supports advanced features like:

* JSON
* PDB (Pluggable DB)
* Auto indexing

▶️ *Video Duration: 1m 7s*

---

## 1. Client Tools

Oracle SQL tools let you interact with the database in different ways. Choose based on your environment and comfort level.

---

### 1.1 SQL\*Plus

A command-line interface bundled with Oracle.

📝 **Use Case**: Lightweight, fast for scripting and automation.

#### 🔧 Installation:

* Comes with Oracle client or full DB install.
* [Oracle Instant Client SQL\*Plus](https://www.oracle.com/database/sqldeveloper/technologies/sqlplus-downloads.html)

#### 💻 Example:

```sql
-- Open terminal
sqlplus username/password@localhost:1521/xe

-- Run SQL
SELECT * FROM employees;

-- Exit
EXIT;
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/2819d8ac-7750-4c86-8e6f-0d83ce0b5346" width="24%" /> 
  <img src="https://github.com/user-attachments/assets/957dde10-c4f7-4050-914e-4012c6e0620f" width="24%" /> 
  <img src="https://github.com/user-attachments/assets/0d220d3e-8d73-4d84-bc53-821272d3364f" width="24%" />
  <img src="https://github.com/user-attachments/assets/13d8b0c6-6208-467d-95e5-6bda1c0b3758" width="24%" />
</p>

📄 [SQL\*Plus Command Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqpug/index.html)

---

### 1.2 SQLcl

A modern command-line tool by Oracle, supports scripting and advanced features.

📝 **Use Case**: Scripting, data export, better than SQL\*Plus in formatting and usability.

#### 🔧 Download:

* [SQLcl Download (Oracle Official)](https://www.oracle.com/database/sqldeveloper/technologies/sqlcl/download/)

#### 💻 Example:

```bash
sql your_user/your_pass@localhost:1521/XEPDB1

-- Or use connect command inside SQLcl:
connect hr/hr@localhost:1521/XEPDB1

-- Run SQL
SELECT first_name, last_name FROM employees;

-- Format table output
set sqlformat ansiconsole

-- Exit
exit;
```

<img width="1920" height="1080" alt="Screenshot (546)" src="https://github.com/user-attachments/assets/b52d7187-04d5-4ddb-995f-1bc169452714" />

📄 [SQLcl User Guide](https://docs.oracle.com/en/database/oracle/sql-developer-command-line/22.1/sclug/index.html)

---

### 1.3 SQL Developer

A graphical interface for managing Oracle databases.

📝 **Use Case**: Ideal for beginners, GUI-based table editing, data modeling.

#### 🔧 Download:

* [SQL Developer Download `Full page`](https://www.oracle.com/database/sqldeveloper/) or [Diract Dpwnload pg](https://www.oracle.com/in/database/sqldeveloper/technologies/download/)

<p align="center">
  <img src="https://github.com/user-attachments/assets/c664f9a3-031e-4c76-8b6e-32c660852a13" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/5e59048e-9576-435f-8b74-5faa3d7211fa" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/7d6f02ba-5641-4dcd-8789-fa6dd1eb9eb3" width="33%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e3c975c2-1870-492d-9b06-0b9fbda4e094" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/70217086-7f5d-4222-bb0a-3f8a9be09e03" width="33%" /> 
  <img src="https://github.com/user-attachments/assets/f90a6a41-f549-42cc-a7dc-1520e2ce17b0" width="33%" />
</p>

#### 💻 Connect Steps:

1. Open SQL Developer.
2. Create a new connection:

   * Username: `hr`
   * Password: `hr`
   * Host: `localhost`
   * SID: `xe` or Service Name: `XEPDB1`
3. Click "Test" → Then "Connect".

#### 💻 Run a SQL query:

```sql
SELECT department_id, department_name FROM departments;
```

📄 [SQL Developer Documentation](https://docs.oracle.com/en/database/oracle/sql-developer/)

---

## 2. SELECT Statements

### 2.1 Data Types Overview

Oracle supports a wide range of data types:

* `VARCHAR2(size)` – variable-length string
* `NUMBER(p,s)` – numeric with precision
* `DATE`, `TIMESTAMP` – date/time
* `CLOB`, `BLOB` – for large objects

#### 💻 Example:

```sql
CREATE TABLE sample (
  name VARCHAR2(50),
  salary NUMBER(8,2),
  hire_date DATE
);
```

📄 [Oracle Data Types Guide](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Data-Types.html)

<details>
  <summary style="opacity: 0.85;"><b>more</b></summary><br>

Great — thanks for confirming! Based on the uploaded images, here’s the **updated and expanded version** of:

---

## 🔹 2.1.0 Data Types Overview

Oracle Database provides several **built-in data types** to define the nature of data stored in a table's columns. Understanding these is fundamental for database design, data integrity, and performance.

---

### 🔸 What is a Data Type?

A **data type** defines:

* The **kind of value** a column can hold (e.g., numbers, text, dates).
* The **operations** that can be performed on that data.
* The **storage format** and space requirements.

Choosing the right data type:

* ✅ Improves **query performance**
* ✅ Ensures **data consistency**
* ✅ Saves **storage space**

---

### 🔸 Main Categories of Data Types

Oracle classifies data types into several broad categories:

| Category       | Description                             |
| -------------- | --------------------------------------- |
| **Character**  | Textual data (names, addresses, etc.)   |
| **Numeric**    | Integers, decimals, and floating points |
| **Date/Time**  | Temporal data like dates and timestamps |
| **LOBs**       | Large objects like images, files, etc.  |
| **RAW/BINARY** | Binary data for internal use            |

---

### 🔹 2.1.1. Character Data Types

| Type           | Description                                    | Example                   |
| -------------- | ---------------------------------------------- | ------------------------- |
| `CHAR(n)`      | Fixed-length string (right-padded with spaces) | `'A'` → `'A '` if `n = 2` |
| `VARCHAR2(n)`  | Variable-length string, up to `n` bytes/chars  | `'Hello'`                 |
| `NCHAR(n)`     | Fixed-length Unicode characters                | `'ह'`                     |
| `NVARCHAR2(n)` | Variable-length Unicode string                 | `'日本語'`                   |

📌 **CHAR vs VARCHAR2**

* `CHAR` always reserves `n` characters (even if unused).
* `VARCHAR2` stores exactly what you input — more efficient for variable-length text.

🔗 [Oracle Docs - Character Data Types](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Data-Types.html#GUID-52E4A9AB-EC5F-49C7-BCCF-83E9AF35F1B7)

---

### 🔹 2.1.2. Numeric Data Types

| Type           | Description                           | Example                  |
| -------------- | ------------------------------------- | ------------------------ |
| `NUMBER(p, s)` | Precision `p`, scale `s` for decimals | `NUMBER(5,2)` → `123.45` |
| `INTEGER`      | Whole numbers (alias of `NUMBER`)     | `10`, `-2`               |
| `FLOAT`        | Approximate values, scientific use    | `3.1415E+00`             |

📌 Oracle allows extremely large numbers with up to 38 digits of precision.

✅ Example:

```sql
CREATE TABLE employees (
  id NUMBER(5),
  salary NUMBER(8,2)
);
```

🔗 [Oracle Docs - Numeric Types](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Data-Types.html#GUID-509EDC70-91F0-45A5-8C01-F5B131C3A86E)

---

### 🔹 2.1.3. Date and Time Types

| Type                       | Description                           | Example                        |
| -------------------------- | ------------------------------------- | ------------------------------ |
| `DATE`                     | Date and time (to the second)         | `'06-AUG-25 13:10:55'`         |
| `TIMESTAMP`                | DATE + fractional seconds             | `'2025-08-06 13:10:55.123'`    |
| `TIMESTAMP WITH TIME ZONE` | Includes time zone info               | `'2025-08-06 13:10:55 +05:30'` |
| `INTERVAL`                 | Time differences (e.g., days, months) | `INTERVAL '2-3' YEAR TO MONTH` |

✅ Example:

```sql
SELECT SYSDATE FROM DUAL;  -- Returns current date and time
```

🔗 [Oracle Docs - Datetime Types](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Data-Types.html#GUID-607372E2-8C9F-4AE4-B6D3-8E83CEB8C97D)

---

### 🔹 2.1.4. Large Objects (LOBs)

Used for storing **large text, images, audio, or binary files**.

| Type    | Description                     | Example Use Case          |
| ------- | ------------------------------- | ------------------------- |
| `CLOB`  | Character large object (text)   | Storing blog articles     |
| `NCLOB` | Unicode large text              | Multilingual content      |
| `BLOB`  | Binary data                     | Storing images, PDFs      |
| `BFILE` | External file in OS file system | Read-only access to files |

✅ Example:

```sql
CREATE TABLE documents (
  doc_id NUMBER,
  doc_content CLOB
);
```

🔗 [Oracle Docs - LOBs](https://docs.oracle.com/en/database/oracle/oracle-database/19/adlob/)

---

### 🔹 2.1.5. RAW and LONG Data Types

These are used **rarely**, usually for backward compatibility or specialized systems.

| Type       | Description                         | Use Case           |
| ---------- | ----------------------------------- | ------------------ |
| `RAW(n)`   | Stores binary or non-character data | Internal keys      |
| `LONG`     | Deprecated. Stores large text.      | Use `CLOB` instead |
| `LONG RAW` | Stores large binary data            | Use `BLOB` instead |

---

### 🔸 Data Types Best Practices

| Tip                              | Explanation                  |
| -------------------------------- | ---------------------------- |
| Use `VARCHAR2` instead of `CHAR` | Saves space                  |
| Use `CLOB` for long text         | `VARCHAR2` max is 4000 bytes |
| Prefer `TIMESTAMP` over `DATE`   | More precision               |
| Don’t use `LONG` / `LONG RAW`    | Deprecated                   |

</details>

---

### 2.2 SELECT Statement Clauses

Basic structure:

```sql
SELECT column1, column2
FROM table_name
WHERE condition
ORDER BY column1;
```

#### 💻 Example:

```sql
SELECT first_name, salary
FROM employees
WHERE department_id = 90
ORDER BY salary DESC;
```

📄 [SELECT Statement Syntax](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/SELECT.html)

---

### 2.3 Expressions in SELECT and WHERE

You can use arithmetic, logical, or string expressions.

#### 💻 Example:

```sql
SELECT first_name, salary, salary * 12 AS annual_salary
FROM employees
WHERE salary > 1000;
```

---

### 2.4 Column Aliases

You can rename columns in output using `AS`.

#### 💻 Example:

```sql
SELECT first_name AS "First Name", salary AS "Monthly Pay"
FROM employees;
```

---

### 2.5 Subqueries

Subqueries = queries inside queries.

#### 💻 Example:

```sql
SELECT first_name, salary
FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```

---

### 2.6 Quiz

*(Just a reminder: 15 questions — test your understanding!)*

---

## 3. Data Dictionary

Oracle maintains a set of **metadata views** that store information about database objects like tables, views, columns, users, etc.

---

### 3.1 Using `DESCRIBE` in SQL\*Plus

The `DESCRIBE` command shows the structure of a table.

#### 💻 Example:

```sql
-- Describe a table
DESC employees;
```

This displays:

* Column names
* Data types
* Nullable info

📄 [DESCRIBE Command Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqpug/Using-SQL-Plus.html#GUID-C9F2178B-E52A-44B2-8492-81BAEBE45216)

---

### 3.2 Using DDL Commands in SQLcl

DDL = Data Definition Language
Used to define or alter the structure of database objects.

#### 💻 Example 1: Creating a table

```sql
CREATE TABLE departments (
  dept_id NUMBER PRIMARY KEY,
  dept_name VARCHAR2(50)
);
```

#### 💻 Example 2: Altering a table

```sql
ALTER TABLE departments ADD location VARCHAR2(100);
```

#### 💻 Example 3: Viewing object DDL

In SQLcl, you can use:

```sql
DDL departments;
```

🔗 [DDL in SQLcl Docs](https://docs.oracle.com/en/database/oracle/sql-developer-command-line/20.2/sclug/using-sqlcl.html#GUID-B40EC5CE-31C1-4414-8819-CFECF4C59EFB)

---

### 3.3 Common Data Dictionary Views

These views are read-only and let you query the database structure.

| View               | Description                               |
| ------------------ | ----------------------------------------- |
| `USER_TABLES`      | Tables owned by the current user          |
| `ALL_TABLES`       | Tables accessible to the current user     |
| `DBA_TABLES`       | All tables in the database (admin access) |
| `USER_TAB_COLUMNS` | Column info for user’s tables             |

#### 💻 Examples:

```sql
-- List all your tables
SELECT table_name FROM user_tables;

-- See columns of a specific table
SELECT column_name, data_type
FROM user_tab_columns
WHERE table_name = 'EMPLOYEES';
```

📄 [Oracle Data Dictionary Overview](https://docs.oracle.com/en/database/oracle/oracle-database/19/refrn/data-dictionary.html)

---

✅ **Section Complete!**
This section teaches how to:

* Check table structure
* Use DDL commands
* Explore metadata views

---

## 4. String Manipulation

Working with strings is essential in SQL — Oracle provides many functions for formatting, concatenating, and handling quotes in strings.

---

### 4.1 Literals

**Literals** are fixed values like text or numbers used in SQL queries.

#### 💻 Example:

```sql
SELECT 'Hello, Oracle!' AS greeting FROM dual;
```

* `dual` is a special one-row table used for testing expressions in Oracle.
* Strings are enclosed in single quotes `'...'`.

---

### 4.2 Concatenation

To join strings together, use the `||` operator.

#### 💻 Example:

```sql
SELECT first_name || ' ' || last_name AS full_name
FROM employees;
```

* You can also concatenate with literals:

```sql
SELECT 'Employee: ' || first_name FROM employees;
```

---

### 4.3 Alternative Quoting

To handle quotes inside strings, Oracle provides **q-quote syntax**:

#### 💻 Syntax:

```sql
q'[your string here]'
```

#### 💻 Example:

```sql
SELECT q'[This is John's pen]' AS note FROM dual;
```

* No need to escape `'` inside the string
* Delimiters can be any matching pair: `[ ]`, `{ }`, `( )`, `< >`

📄 [Oracle Alternative Quoting](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Literals.html)

---

### 4.4 Common String Functions

| Function                  | Description                | Example                                |
| ------------------------- | -------------------------- | -------------------------------------- |
| `UPPER(str)`              | Converts to uppercase      | `UPPER('abc') → 'ABC'`                 |
| `LOWER(str)`              | Converts to lowercase      | `LOWER('ABC') → 'abc'`                 |
| `INITCAP(str)`            | Capitalizes each word      | `INITCAP('oracle sql') → 'Oracle Sql'` |
| `LENGTH(str)`             | Returns length of string   | `LENGTH('Oracle') → 6`                 |
| `SUBSTR(str, start, len)` | Substring                  | `SUBSTR('OracleSQL', 1, 6) → 'Oracle'` |
| `INSTR(str, substr)`      | Find position of substring | `INSTR('Oracle', 'a') → 3`             |

#### 💻 Example:

```sql
SELECT UPPER(first_name), LENGTH(first_name)
FROM employees;
```

---

### 4.5 Quiz

🧠 *9 Questions — Practice string functions, quotes, and expressions.*

---

✅ **Section Complete!**

You've now covered:

* Handling literals and quotes
* Concatenating strings
* Using string functions like `UPPER`, `SUBSTR`, `INSTR`

---

## 5. Filtering Rows

In SQL, filtering is done using the `WHERE` clause. You can also apply conditions in joins and subqueries to refine your results.

---

### 5.1 WHERE Clause Syntax

The `WHERE` clause is used to filter rows that meet specific conditions.

#### 💻 Syntax:

```sql
SELECT column1, column2
FROM table_name
WHERE condition;
```

#### 💻 Example:

```sql
SELECT first_name, salary
FROM employees
WHERE salary > 5000;
```

You can use:

* Comparison: `=`, `!=`, `<`, `>`, `<=`, `>=`
* Logical: `AND`, `OR`, `NOT`
* Range: `BETWEEN`, `IN`, `LIKE`, `IS NULL`

#### 💻 Example with multiple conditions:

```sql
SELECT first_name, department_id
FROM employees
WHERE department_id IN (50, 80)
  AND salary BETWEEN 4000 AND 8000;
```

📄 [WHERE Clause Docs](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Conditions.html)

---

### 5.2 Subqueries in the WHERE Clause

A **subquery** inside the `WHERE` lets you compare values from another result set.

#### 💻 Example:

```sql
SELECT first_name, salary
FROM employees
WHERE salary > (
  SELECT AVG(salary) FROM employees
);
```

* This query shows employees earning **above average** salary.

---

### 5.3 Filtering in JOINs

When using `JOIN`, conditions can be applied:

* In the `ON` clause
* In the `WHERE` clause (for extra filters)

#### 💻 Example: Filtering joined tables

```sql
SELECT e.first_name, d.department_name
FROM employees e
JOIN departments d ON e.department_id = d.department_id
WHERE d.location_id = 1700;
```

* This filters only those departments in a specific location.

📄 [Oracle JOIN Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Queries-and-Subqueries.html)

---

### 5.4 NULL Filtering

To check for `NULL` values:

#### 💻 Example:

```sql
SELECT employee_id, commission_pct
FROM employees
WHERE commission_pct IS NULL;
```

---

### 5.5 Quiz

🧠 *9 questions — Practice filtering using WHERE, AND/OR, subqueries, and joins.*

---

✅ **Section Complete!**
You've learned how to:

* Use `WHERE` with multiple conditions
* Compare results using subqueries
* Filter joined rows
* Work with `NULL` values

---

## 6. Sorting Rows

After retrieving data with a `SELECT` query, you can sort it using the `ORDER BY` clause. Oracle also supports sorting using **collation rules** for language-sensitive operations.

---

### 6.1 ORDER BY Clause

The `ORDER BY` clause is used to sort query results in ascending (default) or descending order.

#### 💻 Syntax:

```sql
SELECT column1, column2
FROM table_name
ORDER BY column1 [ASC|DESC];
```

#### 💻 Example 1: Sort by salary (lowest to highest)

```sql
SELECT first_name, salary
FROM employees
ORDER BY salary;
```

#### 💻 Example 2: Sort by department and then salary (highest first)

```sql
SELECT first_name, department_id, salary
FROM employees
ORDER BY department_id, salary DESC;
```

You can also use **column position**:

```sql
-- Sort by second column, descending
SELECT first_name, salary FROM employees ORDER BY 2 DESC;
```

---

### 6.2 Sorting by Expressions

You can sort using calculated fields or functions.

#### 💻 Example:

```sql
SELECT first_name, salary, salary * 12 AS annual_salary
FROM employees
ORDER BY annual_salary DESC;
```

---

### 6.3 Collation Rules (Advanced)

Oracle 12c and above supports **collation** — rules that define how characters are compared/sorted (especially for languages with accents, etc.)

#### 💻 Example:

```sql
SELECT first_name
FROM employees
ORDER BY first_name COLLATE BINARY_CI;  -- Case-insensitive sort
```

📝 Collation types:

* `BINARY`: case-sensitive (default)
* `BINARY_CI`: case-insensitive
* `BINARY_AI`: accent-insensitive

📄 [Oracle Collation Documentation](https://docs.oracle.com/en/database/oracle/oracle-database/19/nlspg/introduction-to-collation.html)

---

### 6.4 Quiz

🧠 *6 Questions — Practice sorting, using ORDER BY, and understanding collation.*

---

✅ **Section Complete!**
You now know how to:

* Sort query results using `ORDER BY`
* Use ascending/descending order
* Sort using expressions and multiple columns
* Apply collation rules for custom sorting logic

---

## 7. Single-Row Functions

Single-row functions return one result per row. They are commonly used to:

* Modify data
* Perform calculations
* Format output

Functions are categorized by **type**:

* Numeric
* Character
* Date
* Conversion
* General

You can use them in `SELECT`, `WHERE`, `ORDER BY`, etc.

---

### 7.1 Numeric Functions

#### 🔹 Common Numeric Functions:

| Function      | Description                                |
| ------------- | ------------------------------------------ |
| `ROUND(n, d)` | Rounds number `n` to `d` decimal places    |
| `TRUNC(n, d)` | Truncates number `n` to `d` decimal places |
| `MOD(m, n)`   | Returns remainder of `m/n`                 |

#### 💻 Example:

```sql
SELECT salary, ROUND(salary, -3), MOD(salary, 1000)
FROM employees;
```

---

### 7.2 Character Functions (returning **character**)

These functions work on strings and return string output.

| Function                      | Description                     |
| ----------------------------- | ------------------------------- |
| `LOWER(str)`                  | Converts to lowercase           |
| `UPPER(str)`                  | Converts to uppercase           |
| `INITCAP(str)`                | First letter uppercase          |
| `LTRIM(str)` / `RTRIM(str)`   | Trim characters from left/right |
| `SUBSTR(str, start, len)`     | Extract substring               |
| `REPLACE(str, find, replace)` | Replace text                    |

#### 💻 Example:

```sql
SELECT first_name, UPPER(first_name), SUBSTR(first_name, 1, 2)
FROM employees;
```

---

### 7.3 Character Functions (returning **numeric**)

| Function             | Description                   |
| -------------------- | ----------------------------- |
| `LENGTH(str)`        | Returns number of characters  |
| `INSTR(str, substr)` | Returns position of substring |

#### 💻 Example:

```sql
SELECT email, LENGTH(email), INSTR(email, '@')
FROM employees;
```

---

### 7.4 Datetime Functions

| Function                   | Description                           |
| -------------------------- | ------------------------------------- |
| `SYSDATE`                  | Current system date/time              |
| `CURRENT_DATE`             | Current date (user session time zone) |
| `ADD_MONTHS(date, n)`      | Add months                            |
| `MONTHS_BETWEEN(d1, d2)`   | # of months between two dates         |
| `NEXT_DAY(date, 'MONDAY')` | Next given weekday                    |
| `LAST_DAY(date)`           | Last day of the month                 |

#### 💻 Example:

```sql
SELECT hire_date, ADD_MONTHS(hire_date, 6), LAST_DAY(hire_date)
FROM employees;
```

---

### 7.5 Conversion Functions

Used to convert between data types.

| Function                | Description                   |
| ----------------------- | ----------------------------- |
| `TO_CHAR(expr, format)` | Convert date/number to string |
| `TO_DATE(str, format)`  | Convert string to date        |
| `TO_NUMBER(str)`        | Convert string to number      |

#### 💻 Example:

```sql
SELECT TO_CHAR(SYSDATE, 'DD-Mon-YYYY') AS today,
       TO_DATE('2025-12-01', 'YYYY-MM-DD') AS converted_date
FROM dual;
```

📄 [Oracle Conversion Functions](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/SQL-Functions.html#GUID-67A1F9E8-8E07-4D75-9E64-98C1F5D760C1)

---

### 7.6 General Functions

| Function                      | Description                               |
| ----------------------------- | ----------------------------------------- |
| `NVL(expr1, expr2)`           | Replace `NULL` with expr2                 |
| `NVL2(expr1, expr2, expr3)`   | If expr1 not NULL return expr2 else expr3 |
| `NULLIF(expr1, expr2)`        | Returns NULL if both equal                |
| `COALESCE(expr1, expr2, ...)` | First non-NULL value                      |

#### 💻 Example:

```sql
SELECT first_name, commission_pct, NVL(commission_pct, 0)
FROM employees;
```

---

### 7.7 List Functions with SQL Developer

If you're using SQL Developer:

**📍 Steps:**

* Go to `View` → `DBMS Output`
* Use:

```sql
SELECT object_name
FROM all_objects
WHERE object_type = 'FUNCTION';
```

You can also explore:

* `ALL_FUNCTIONS`
* `USER_FUNCTIONS`

---

### 7.8 Quiz

🧠 *21 Questions — Practice all types of single-row functions in SELECT, WHERE, and expressions.*

---

✅ **Section Complete!**
You now understand:

* How to use built-in single-row functions in SQL
* Use cases for string, number, date, and conversion operations

---

## 8. Aggregation and Multiple-Row Functions

Unlike single-row functions, **aggregation (group) functions** operate on *sets of rows* and return a *single result* per group.

Common aggregate functions:

* `SUM`, `AVG`, `COUNT`, `MAX`, `MIN`

---

### 8.1 `GROUP BY` Clause

Used to group rows sharing a value in one or more columns.

#### 💻 Example:

```sql
SELECT department_id, COUNT(*) AS emp_count, AVG(salary)
FROM employees
GROUP BY department_id;
```

* Groups employees by department
* Returns count and average salary per department

---

### 8.2 `HAVING` Clause

Works like a `WHERE` clause but filters **after grouping**.

#### 💻 Example:

```sql
SELECT department_id, AVG(salary)
FROM employees
GROUP BY department_id
HAVING AVG(salary) > 5000;
```

* Filters only departments with average salary above 5000

> ⚠️ You **can’t** use `WHERE` to filter grouped results. Use `HAVING` instead.

---

### 8.3 Using `DISTINCT` in Aggregation

`DISTINCT` helps avoid duplicate values.

#### 💻 Example:

```sql
SELECT COUNT(DISTINCT department_id) AS total_departments
FROM employees;
```

* Counts only unique departments

You can also use `DISTINCT` inside `SUM`, `AVG`, etc.

---

### 🔧 Common Aggregate Functions

| Function     | Description             |
| ------------ | ----------------------- |
| `COUNT(*)`   | Counts all rows         |
| `COUNT(col)` | Counts non-null rows    |
| `SUM(col)`   | Adds all numeric values |
| `AVG(col)`   | Average of values       |
| `MIN(col)`   | Smallest value          |
| `MAX(col)`   | Largest value           |

---

### 📘 Oracle Documentation

* 📄 [Aggregate Functions — Oracle 19c SQL Reference](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/SQL-Functions.html#GUID-3F3BAF1D-6E14-4FBE-817A-ADDF5F9F2E6B)

---

### 8.4 Quiz

🧠 *9 Questions — Practice GROUP BY, HAVING, and DISTINCT together with aggregation.*

---

✅ **Section Complete!**
You now understand how to:

* Aggregate data using `COUNT`, `SUM`, etc.
* Group results with `GROUP BY`
* Filter group results using `HAVING`

---

## 9. Joining Tables

In real-world databases, data is stored in **multiple related tables**. To retrieve meaningful data, we **join** them.

> 🔗 **JOIN** = Combine rows from two or more tables based on a related column (usually a foreign key).

---

### 9.1 ANSI JOIN vs Oracle JOIN Syntax

There are two styles of writing joins:

#### ✅ ANSI Syntax (Preferred)

```sql
SELECT e.first_name, d.department_name
FROM employees e
JOIN departments d
ON e.department_id = d.department_id;
```

#### ⚠️ Oracle Legacy Syntax

```sql
SELECT e.first_name, d.department_name
FROM employees e, departments d
WHERE e.department_id = d.department_id;
```

> ANSI syntax is **clearer and standard**. Use it in interviews and modern code.

---

### 9.2 `INNER JOIN`

Returns rows **only when a match exists** in both tables.

#### 💻 Example:

```sql
SELECT e.first_name, d.department_name
FROM employees e
INNER JOIN departments d
ON e.department_id = d.department_id;
```

---

### 9.3 `LEFT (OUTER) JOIN`

Returns **all rows from the left** table, even if there’s no match in the right table. Unmatched right-side values return `NULL`.

#### 💻 Example:

```sql
SELECT e.first_name, d.department_name
FROM employees e
LEFT OUTER JOIN departments d
ON e.department_id = d.department_id;
```

---

### 9.4 `RIGHT (OUTER) JOIN`

Returns **all rows from the right** table, even if there’s no match in the left table.

#### 💻 Example:

```sql
SELECT e.first_name, d.department_name
FROM employees e
RIGHT OUTER JOIN departments d
ON e.department_id = d.department_id;
```

---

### 9.5 `FULL (OUTER) JOIN`

Returns **all rows when there is a match in one of the tables**, otherwise returns `NULL`.

#### 💻 Example:

```sql
SELECT e.first_name, d.department_name
FROM employees e
FULL OUTER JOIN departments d
ON e.department_id = d.department_id;
```

---

### 9.6 `NATURAL JOIN`

Automatically joins tables by **columns with the same name**.
⚠️ Use with caution — not recommended unless you fully understand the schema.

#### 💻 Example:

```sql
SELECT *
FROM employees
NATURAL JOIN departments;
```

> Joins on all columns that have the same name and compatible datatypes.

---

### 9.7 `CROSS JOIN`

Creates **Cartesian product** — every row from the first table is joined with every row from the second table.

#### 💻 Example:

```sql
SELECT e.first_name, d.department_name
FROM employees e
CROSS JOIN departments d;
```

> 🚨 Very dangerous on large tables. Only use when needed.

---

### 🧪 Tips for Working with Joins

* Always use **aliases** for table names (e.g., `e`, `d`)
* Use `INNER JOIN` for most tasks
* Be cautious with `FULL` and `CROSS JOIN`
* Use **ER diagrams** or documentation to understand relationships

---

### 📘 Useful Links

* 📄 [Oracle SQL JOIN Syntax (19c Docs)](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/Queries.html#GUID-11750D2B-6DAB-49D5-8C14-AD5A6C3B2A69)
* 🧰 [W3Schools SQL Joins Visual Guide](https://www.w3schools.com/sql/sql_join.asp)

---

### 9.8 Quiz

🧠 *21 Questions — Solidify your knowledge of JOINs with inner, outer, and cross queries.*

---

✅ **Section Complete!**
You’ve now learned to:

* Join tables using ANSI-style SQL
* Retrieve data from multiple sources

---

## 10. Using the Oracle Data Dictionary

The **Oracle Data Dictionary** is a **set of read-only tables and views** that provide information about the database, its objects, users, privileges, and more.

> 🧠 Think of it as **Oracle’s internal database about the database**.

---

### 10.1 Understanding the Data Dictionary

Oracle maintains metadata in tables such as:

| View Prefix | Meaning                                    |
| ----------- | ------------------------------------------ |
| `USER_`     | Info about **your** objects                |
| `ALL_`      | Info about **accessible** objects          |
| `DBA_`      | Info about **all** objects (need DBA role) |

#### 💻 Example:

```sql
-- See your own tables
SELECT table_name FROM user_tables;

-- See all accessible tables
SELECT table_name FROM all_tables;

-- See all tables in the database (DBA only)
SELECT table_name FROM dba_tables;
```

---

### 10.2 Querying the Data Dictionary

Let’s say you want to view all the **columns** of a table:

```sql
SELECT column_name, data_type, data_length
FROM user_tab_columns
WHERE table_name = 'EMPLOYEES';
```

📌 *Note*: Always use uppercase table names in these queries because Oracle stores metadata in uppercase.

---

### 🔍 Commonly Used Data Dictionary Views

| View               | Purpose                      |
| ------------------ | ---------------------------- |
| `USER_TABLES`      | Your tables                  |
| `USER_TAB_COLUMNS` | Columns in your tables       |
| `USER_CONSTRAINTS` | Constraints (PK, FK, etc.)   |
| `USER_INDEXES`     | Indexes                      |
| `USER_VIEWS`       | Views                        |
| `USER_SEQUENCES`   | Sequences                    |
| `USER_SYNONYMS`    | Synonyms                     |
| `USER_OBJECTS`     | All types of objects you own |

---

### 🛠 Bonus: Find Tables You Created Today

```sql
SELECT table_name, created
FROM user_objects
WHERE object_type = 'TABLE'
AND created > SYSDATE - 1;
```

---

### 📘 Useful Links

* 📚 [Oracle Data Dictionary Documentation (19c)](https://docs.oracle.com/en/database/oracle/oracle-database/19/refrn/data-dictionary-views.html)
* 🔍 [Oracle Live SQL: Explore Metadata](https://livesql.oracle.com/)
* 🛠 [USER\_ vs ALL\_ vs DBA\_ – StackOverflow Explainer](https://stackoverflow.com/a/29832871)

---

### 10.3 Quiz

🧠 *6 questions to test your metadata skills.*

---

✅ **Section Complete!**
Now you can:

* Understand and query metadata using Oracle’s dictionary
* Explore tables, columns, constraints, and more

---

## 11. DML: INSERT / UPDATE / DELETE

DML lets you **manipulate existing data** inside Oracle tables. This includes:

* `INSERT`: Add new rows
* `UPDATE`: Modify existing rows
* `DELETE`: Remove rows

Let’s go one-by-one with examples 👇

---

### 11.1 Inserting Single Rows

```sql
-- Insert one row into a table
INSERT INTO employees (employee_id, first_name, last_name, salary)
VALUES (1001, 'John', 'Doe', 50000);
```

📝 Make sure the column order in `INSERT` matches the values.

---

### 11.2 Inserting Multiple Rows

Oracle 19c supports inserting multiple rows with one `INSERT ALL` statement:

```sql
INSERT ALL
  INTO employees (employee_id, first_name, last_name, salary)
  VALUES (1002, 'Alice', 'Smith', 60000)
  
  INTO employees (employee_id, first_name, last_name, salary)
  VALUES (1003, 'Bob', 'Johnson', 55000)
SELECT * FROM dual;
```

🧠 `dual` is a dummy table used for queries that don't rely on real data.

---

### 11.3 Updating Rows

```sql
-- Give a salary hike to employee 1001
UPDATE employees
SET salary = salary + 5000
WHERE employee_id = 1001;
```

📌 Always use a `WHERE` clause in `UPDATE` to avoid updating all rows accidentally.

---

### 11.4 Deleting Rows

```sql
-- Delete employee with ID 1002
DELETE FROM employees
WHERE employee_id = 1002;
```

⚠️ **Without WHERE**, all rows in the table will be deleted!

---

### 💡 Bonus: UPDATE Using Subquery

```sql
-- Set salary based on data from another table
UPDATE employees e
SET salary = (SELECT salary FROM temp_employees t WHERE t.id = e.employee_id)
WHERE EXISTS (SELECT 1 FROM temp_employees t WHERE t.id = e.employee_id);
```

---

### 📘 Documentation & Resources

* 📚 [INSERT Statement (Oracle Docs)](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/INSERT.html)
* 📚 [UPDATE Statement (Oracle Docs)](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/UPDATE.html)
* 📚 [DELETE Statement (Oracle Docs)](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/DELETE.html)
* 🧪 [Try DML on Live SQL](https://livesql.oracle.com)

---

### 🧪 Chapter Quiz

Test your DML skills with **12 questions**.

---

✅ **Section Complete!**
You’ve now mastered inserting, updating, and deleting data in Oracle like a pro!

---

## 12. DDL: Creating Objects

DDL is used to **define, create, or modify database schema objects** such as tables, indexes, and constraints.

Let’s break down the major components with examples 👇

---

### 12.1 Creating Tables

```sql
-- Create a simple table
CREATE TABLE employees (
  employee_id   NUMBER PRIMARY KEY,
  first_name    VARCHAR2(50),
  last_name     VARCHAR2(50),
  salary        NUMBER,
  hire_date     DATE DEFAULT SYSDATE
);
```

🔹 `VARCHAR2` is preferred over `VARCHAR` in Oracle.
🔹 `SYSDATE` returns the current system date and time.

---

### 12.2 Creating Indexes

Indexes improve query performance, especially for large datasets.

```sql
-- Create an index on last_name for faster lookups
CREATE INDEX idx_lastname ON employees (last_name);
```

🧠 Oracle automatically creates indexes for `PRIMARY KEY` and `UNIQUE` constraints.

---

### 12.3 Create Oracle-Specific Tables

Oracle offers advanced features like **object types**, **partitioned tables**, and **temporary tables**. Here’s a basic example:

```sql
-- Create a Global Temporary Table (data persists for session/transaction)
CREATE GLOBAL TEMPORARY TABLE temp_employees (
  id           NUMBER,
  name         VARCHAR2(100)
) ON COMMIT PRESERVE ROWS;
```

💡 Use this for storing intermediate or session-based data.

---

### 🔗 Documentation & Resources

* 📚 [CREATE TABLE – Oracle Docs](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/CREATE-TABLE.html)
* 📚 [CREATE INDEX – Oracle Docs](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/CREATE-INDEX.html)
* 📚 [Oracle Temporary Tables](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/CREATE-GLOBAL-TEMPORARY-TABLE.html)

---

### ✅ Real-Life Tip

📌 When designing a table:

* Use appropriate **data types** and **constraints**
* Plan **indexes** for performance
* Document your structure in a schema diagram

---

### 🧪 Chapter Quiz

Challenge yourself with **6 questions** on DDL!

---

✅ **Section Complete!**
You now know how to **create and structure** your Oracle database using DDL!

---

## 13. Dropping Objects

Dropping objects means **permanently removing** them from the database. It’s a **destructive operation**, so use it with caution.

---

### 13.1 Dropping Tables

```sql
-- Delete the entire table structure and its data
DROP TABLE employees;
```

🔸 This removes the table *and all of its data*.
🔸 Any indexes or constraints defined on the table are also removed.

```sql
-- Drop a table only if it exists (to avoid errors)
BEGIN
   EXECUTE IMMEDIATE 'DROP TABLE employees';
EXCEPTION
   WHEN OTHERS THEN
      NULL; -- silently handle if table doesn't exist
END;
```

---

### 13.2 Dropping Indexes

```sql
-- Drop a previously created index
DROP INDEX idx_lastname;
```

💡 You can’t drop indexes that were automatically created by constraints like `PRIMARY KEY`. You must drop the constraint first.

---

### 13.3 Dropping Oracle-Specific Tables

```sql
-- Drop a Global Temporary Table
DROP TABLE temp_employees;
```

🚫 Dropping any table means **no undo** – so double-check!

---

### 🔗 Documentation & Resources

* 📚 [DROP TABLE – Oracle Docs](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/DROP-TABLE.html)
* 📚 [DROP INDEX – Oracle Docs](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/DROP-INDEX.html)

---

### 🧪 Chapter Quiz

📝 Test your understanding with **5 questions** on DROP commands.

---

✅ **Section Complete!**
You now know how to **safely delete tables, indexes, and other objects** from your Oracle database.

---

## 🎓 Conclusion

### ✅ Next Steps

Congratulations on completing the **Oracle Database 19c: Basic SQL** course! 🎉

Now that you’ve built a solid foundation, here’s what you can do next:

---

### 🔄 Review Key Topics

* **Practice SELECT queries** with filtering, sorting, joins, and functions
* **Explore DML** with `INSERT`, `UPDATE`, and `DELETE`
* **Experiment with DDL** by creating and dropping tables
* **Use the Data Dictionary** to understand your schema
* **Master Joins** – especially INNER, OUTER, and CROSS joins
* **Sharpen SQL skills** using platforms like:

  * [LeetCode – SQL Challenges](https://leetcode.com/problemset/database/)
  * [HackerRank – SQL Practice](https://www.hackerrank.com/domains/tutorials/10-days-of-sql)
  * [Oracle Live SQL (Playground)](https://livesql.oracle.com/)

---

### 📘 Advanced Topics You Can Explore Next

* Views, Synonyms, and Sequences
* Index optimization and performance tuning
* PL/SQL (Procedural Language SQL)
* Transactions and locking
* Triggers and stored procedures
* Oracle Architecture and Internals

---

### 🔗 Useful Resources

* 📘 [Oracle SQL Language Reference 19c](https://docs.oracle.com/en/database/oracle/oracle-database/19/sqlrf/index.html)
* 📥 [Download Oracle Database 19c](https://www.oracle.com/database/technologies/oracle19c-windows-downloads.html)
* 🧰 [Oracle SQL Developer (IDE)](https://www.oracle.com/tools/downloads/sqldev-downloads.html)
* 🎥 [Oracle Learning YouTube – Official SQL Playlist](https://www.youtube.com/playlist?list=PLnMKNibPkDnEEUdnWkM7fP5OACkMQumAG)

---

### 👣 Final Tips

* 💡 SQL isn’t just syntax — **it’s problem-solving** with data.
* 🛠️ Keep practicing on **real datasets** or using **online playgrounds**.
* 🧠 Don’t memorize — **understand why and how** each SQL clause works.
* 🔁 Revisit these notes regularly to stay sharp!


