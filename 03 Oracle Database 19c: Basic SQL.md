## 📘 Oracle Database 19c: Basic SQL — Study Notes

---

### [Contents](#contents)

* [Introduction](#introduction)
* [1. Client Tools](#1-client-tools)

  * [1.1 SQL\*Plus](#11-sqlplus)
  * [1.2 SQLcl](#12-sqlcl)
  * [1.3 SQL Developer](#13-sql-developer)
* [2. SELECT Statements](#2-select-statements)

  * [2.1 Data Types Overview](#21-data-types-overview)
  * [2.2 SELECT Statement Clauses](#22-select-statement-clauses)
  * [2.3 Expressions in SELECT and WHERE](#23-expressions-in-select-and-where)
  * [2.4 Column Aliases](#24-column-aliases)
  * [2.5 Subqueries](#25-subqueries)
  * [2.6 Quiz](#26-quiz)

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

📄 [SQLcl User Guide](https://docs.oracle.com/en/database/oracle/sql-developer-command-line/22.1/sclug/index.html)

---

### 1.3 SQL Developer

A graphical interface for managing Oracle databases.

📝 **Use Case**: Ideal for beginners, GUI-based table editing, data modeling.

#### 🔧 Download:

* [SQL Developer Download](https://www.oracle.com/database/sqldeveloper/)

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

Let me know if you’re ready for:

* 🔜 Section 3: **Data Dictionary**
* I’ll include DESCRIBE, DDL usage, and relevant examples.

Shall I continue?
