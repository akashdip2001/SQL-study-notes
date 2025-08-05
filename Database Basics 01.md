<details>
  <summary style="opacity: 0.85;"><b>Reallity of SQL in the world</b></summary><br>

### 🌐 Major Cloud SQL Database Services in the World

This table highlights key SQL database services from major cloud providers, focusing on MySQL and its direct relational database counterparts.

| Provider        | Service Name                       | Database Type                                     | Key Feature Highlights                                          |
| :-------------- | :--------------------------------- | :------------------------------------------------ | :-------------------------------------------------------------- |
| **Oracle** | **MySQL HeatWave** | MySQL (Fully Managed)                             | OLTP + OLAP in one, Autopilot, Auto-scaling, on OCI.           |
|                 | **MySQL Database Service** | MySQL (Fully Managed)                             | Standard MySQL DBaaS on OCI, high availability.                 |
| **Amazon Web Services (AWS)** | **Amazon RDS for MySQL** | MySQL (Fully Managed)                             | Standard MySQL, easy setup, scaling, Multi-AZ for HA.          |
|                 | **Amazon Aurora (MySQL Compatible)** | Proprietary, MySQL-compatible                     | High performance (5x MySQL), distributed, high availability.  |
|                 | **Amazon RDS Custom for MySQL** | MySQL (Fully Managed with OS/DB access)           | Offers deeper OS and DB access for specific needs.              |
| **Google Cloud Platform (GCP)** | **Cloud SQL for MySQL** | MySQL (Fully Managed)                             | Standard MySQL, global scale, automated backups, patching.     |
|                 | **Cloud Spanner** | Horizontally scalable, relational database        | Global scale, strong consistency, high performance for OLTP.    |
| **Microsoft Azure** | **Azure Database for MySQL** | MySQL (Fully Managed)                             | Flexible Server (modern), Single Server (legacy), high availability. |
|                 | **Azure SQL Database** | SQL Server (Fully Managed)                        | PaaS offering of SQL Server, elastic scale, intelligent features. |
| **IBM Cloud** | **Databases for MySQL** | MySQL (Fully Managed)                             | High availability, automated backups, encryption.               |
| **DigitalOcean**| **Managed Databases for MySQL** | MySQL (Fully Managed)                             | Simple, scalable, developer-friendly, automated backups, failover. |

> 25-06-2025

<img width="1920" height="1080" alt="Screenshot (481)" src="https://github.com/user-attachments/assets/51e0d33d-e39f-4297-b7eb-15064b19f98c" />

-----

**Tree Diagram Concept**

```
                       Cloud SQL Database Services
                                |
        -------------------------------------------------------------
        |           |           |           |           |           |
    Oracle         AWS         GCP         Azure       IBM Cloud   DigitalOcean
      |             |           |           |           |           |
    -MySQL HeatWave   -RDS for MySQL  -Cloud SQL for MySQL  -Azure DB for MySQL  -Databases for MySQL  -Managed DB for MySQL
    -MySQL DB Service -Aurora MySQL   -Cloud Spanner        -Azure SQL DB
                      -RDS Custom MySQL
```

---

### 🌐 Understanding MySQL Services focus on [`Oracle`]() & [`AWS`]()

MySQL is a versatile open-source relational database that is available in various forms: as a standalone software you can install, and as a fully managed service on various cloud platforms.

#### Table 1: Core MySQL Offerings (Oracle's Editions and Services)

These are the primary distributions and services provided by Oracle, the current owner of MySQL.

| Feature             | MySQL Community Edition                                     | MySQL Standard Edition                                     | MySQL Enterprise Edition                                           | MySQL Cluster CGE                                                   | MySQL HeatWave (Part of MySQL Database Service on OCI) |
| :------------------ | :---------------------------------------------------------- | :--------------------------------------------------------- | :----------------------------------------------------------------- | :------------------------------------------------------------------ | :----------------------------------------------------- |
| **Availability** | Free, Open Source (GPL)                                     | Commercial License                                         | Commercial License                                                 | Commercial License                                                  | Fully Managed Service on Oracle Cloud Infrastructure (OCI) |
| **Target User** | Developers, small projects, general use                     | SMBs, general business use                                 | Enterprises, mission-critical applications                         | Telecoms, real-time, high-scalability applications                  | Enterprises, Analytics, Hybrid Workloads on Cloud |
| **Key Features** | Basic database functionality, SQL, Replication, Connectors  | All Community features, plus some advanced features        | All Standard features, plus advanced tools for Security, HA, Mgmt. | In-memory, ACID-compliant, shared-nothing, extreme real-time perf. | OLTP + OLAP (In-Memory Query Accelerator), Autopilot, Auto-scaling |
| **Support** | Community Forums                                            | Oracle Premier Support (limited scope compared to Enterprise) | 24x7 Oracle Premier Support                                        | 24x7 Oracle Premier Support                                         | Oracle Cloud Support (integrated with OCI)             |
| **Included Tools** | MySQL Workbench, Shell                                      | Same as Community, plus some commercial connectors         | MySQL Enterprise Monitor, Firewall, Audit, Backup, etc.            | Specialized Cluster tools                                           | Managed service with built-in monitoring, patching, backups |
| **Use Case** | Web applications, small databases, learning, development    | Business applications requiring more stability and support | Critical enterprise applications, high security/availability needs | Next-gen telco, online gaming, financial trading platforms          | Analytics on live transactional data, mixed workloads  |
| **Deployment** | On-premise, VM, Containers, any cloud (self-managed)        | On-premise, VM, Containers, any cloud (self-managed)       | On-premise, VM, Containers, any cloud (self-managed)               | On-premise, dedicated hardware/VMs                                  | OCI (PaaS/DBaaS)                                       |

![Screenshot (40)](https://github.com/user-attachments/assets/d55e9255-57e5-411e-9033-997fcebad19c)

---

#### Table 2: Amazon Web Services (AWS) Database Services.

AWS offers various database services, with Amazon Aurora being a popular choice that is **MySQL-compatible**. It's important to note that Aurora MySQL is **not** MySQL itself, but a highly optimized, proprietary database developed by AWS that is designed to be wire-compatible with MySQL.

| Feature             | Amazon RDS for MySQL                                       | Amazon Aurora MySQL-Compatible Edition                           | Amazon RDS Custom for MySQL                                | Amazon DocumentDB (MongoDB Compatible) |
| :------------------ | :--------------------------------------------------------- | :--------------------------------------------------------------- | :--------------------------------------------------------- | :------------------------------------- |
| **Database Type** | Managed MySQL Community/Enterprise Edition                 | Proprietary, MySQL-compatible relational database                | Managed MySQL Community/Enterprise Edition (with OS/DB access) | Managed NoSQL Document Database (MongoDB API compatible) |
| **Availability** | Fully Managed Service on AWS                               | Fully Managed Service on AWS                                     | Fully Managed Service on AWS (with deeper control)         | Fully Managed Service on AWS           |
| **Architecture** | Standard MySQL architecture with AWS management            | Distributed, shared-storage architecture for high performance/HA | Standard MySQL with OS and DB access                       | Distributed, JSON document store       |
| **Key Benefits** | Easy setup, scaling, patching, backups, Multi-AZ for HA    | 5x performance of standard MySQL, 6-way replication, fast failover | OS and database access for specific configurations/ISVs    | Scalable, highly available, performant document database |
| **Target User** | General purpose, cost-effective MySQL deployments          | Mission-critical, high-performance, high-scale applications      | Applications with specific OS/DB customization needs       | Developers using MongoDB APIs          |
| **Cost Model** | Pay-as-you-go (instance, storage, I/O)                     | Pay-as-you-go (compute, storage) with separate pricing for I/O   | Pay-as-you-go (instance, storage, I/O, OS/DB access)       | Pay-as-you-go                          |
| **Backup/Restore** | Automated backups, point-in-time recovery, snapshots       | Continuous backup, fast point-in-time recovery, snapshots        | Automated backups, point-in-time recovery, snapshots       | Automated backups, point-in-time recovery |
| **Use Case** | Web/mobile apps, enterprise apps, dev/test                 | Large-scale enterprise applications, high-throughput workloads   | Legacy app modernization, specific compliance needs        | JSON document workloads, mobile apps   |
| **Deployment** | AWS Cloud (PaaS/DBaaS)                                     | AWS Cloud (PaaS/DBaaS)                                           | AWS Cloud (PaaS/DBaaS)                                     | AWS Cloud (PaaS/DBaaS)                 |


---

```
                                    MySQL Ecosystem
                                          |
        ---------------------------------------------------------------------------------
        |                                                                               |
    Core MySQL (Oracle)                                                          Cloud-Managed MySQL Services
        |                                                                               |
  ---------------------------------                       ---------------------------------------------------------------------
  |       |       |       |       |                       |                                   |                               |
Community Standard Enterprise Cluster HeatWave          AWS (Aurora, RDS for MySQL, RDS Custom)  Google Cloud SQL (for MySQL)  Azure Database for MySQL (Flexible/Single Server)
```

---

> ✅ Because of SQL is `Open Source` anyone can modify according to there needs and provide extra features & Security. So it's important to leard SQL as a Computer science student.


</details>

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
10. [use in my Project](#app-sql-explane)
    - [explain line by line](https://github.com/Engineering-college-btech-Project2/Project-2/blob/main/README.md#app-sql-explane)

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

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
│── Flat file System: Notepad in pc
└── Database
```

|  | Books & file System | Flat file System |  | Database |
|---|---|---|---|---|
| Maintenance problam | ❌ | ❌ | | ✅ |
| Security Problam | ❌ | ❌ | | ✅ |
| Required more Man power | ✅ | ⚠️ | | ❌ |
| Costly in maintenance | ✅ | ⚠️ | | ❌ |
| Retrieve | ❌ | ❌ (No indexing) | | ✅ |
| Backup | ❌ | ✅ | | ✅ |
| easy Editing | ❌ | ✅ | | ✅ |
| Remote access | ❌ | ✅ | | ✅ |
| Share & Carry data | ❌ | ✅ | | ✅ |

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

| ✅ [**Skip to Main Topic**](#ANSI-SQL-Study-Notes) ➡️ |
|---|

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

</br>
</br>

<img width="1920" height="1080" alt="Screenshot (481)" src="https://github.com/user-attachments/assets/51e0d33d-e39f-4297-b7eb-15064b19f98c" />

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
    - [RDBMS Terms](#RDBMS-Terms)
    - [RDBMS Relationship](#RDBMS-Relationship)
    - [Schema](#schema)
    - [Key](#key)
    - [ER Model](#er-model)
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

```yaml
DBMS
│
├── RDBMS: (Data store in Row & Column format --> Table)
│
│── No SQL DBMS: Unstructured format data  
│   │──> Mongo DB
│   └──> Redis
│
│── HDBMS: Hierarchical DBMS (Tree)
│   └──> IMS (IBM launched 1st HDBMS Softwer IMS in 1960)
│
│── NDBMS: Netwirk DBMS (data in Graphical Structure) all nodes are diractly connected.
│   └──> IDS (Codasyl,IDS,1964)
│
└── OODBMS: Object Orianted DBMS
```

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

## RDBMS Terms <a name="RDBMS-Terms"></a>
<img align="right" alt="python_logo" width="600" src="https://github.com/user-attachments/assets/f80968aa-7a43-4028-8c44-6552c7185ac4"> 

```yaml
RDBMS Terms
│
│── Entity (Table)
│── Attribute (Column)
│── Records (Row)
│── Degree (No. of Column)
│── Cordinality ( ,, Row)
└── Domain  (Valie of Vplumn)
```
## ✅ RDBMS Relationship <a name="RDBMS-Relationship"></a>
```yaml
RDBMS Relationship
│
│── One to One: 1:1
│── One to many: 1:M
└── Many to Many
```
- **One to One: 1:1** : If each record (01 or 02...) of a table is related only rach racord of another table.<br>
- **One to many: 1:M** : If one Record of a table is enter related to multiple records of another table.

```yaml
+-----------------+     +-----------------+               +------------------------+      +-------------------------------+
│ No.  | Name     |     │ No.  | Place    |               │ Customer ID | Name     |      │ No.  | Customer ID | Orders   |
│ 101  | Akashdip |     │ 101  | Haldia   |               │ 01          | Akashdip |      │ 106  | 01          | i Phon7  |
│ 102  | Suman    |     │ 102  | Asansole |               │ 02          | Suman    |      │ 107  | 01          | Laptop   |
+-----------------+     +-----------------+               +------------------------+      │ 108  | 02          | Phon16   |
                                                                                          +-------------------------------+
in 1:1 --> 01, Akashdip, Haldia                          But in 1:M case a persan can order many items.
```

<img width="1920" height="1080" alt="Screenshot (385)" src="https://github.com/user-attachments/assets/f8f871ac-861f-4759-9ed7-3ec665a92d0c" />
<img width="1920" height="1080" alt="Screenshot (384)" src="https://github.com/user-attachments/assets/79432b94-fb13-4dea-8042-78102a7b2776" />
<img width="1920" height="1080" alt="Screenshot (386)" src="https://github.com/user-attachments/assets/ad7d8583-2b32-48f9-9d37-de88e7bcc1f9" />

<img width="1920" height="1080" alt="Screenshot (389)" src="https://github.com/user-attachments/assets/5770fbbe-cd9e-4d31-ad47-f0eebd56ec73" />
<img width="1920" height="1080" alt="Screenshot (390)" src="https://github.com/user-attachments/assets/a29b4ce1-ba45-4334-8ef2-92df58e44ded" />

## ✅ Schema <a name="schema"></a>

- Schema is a blue-print that defines the structure of database.
- It's includes the table, columns, data-types, relationship & constrains.
- Schema tells how data stored and related.

### see the Schema (Structure of the Table)
```sql
SQL> create table student(name varchar(12),address varchar2(20),phone_no number)
SQL> desc student
```
## ✅ Key <a name="key"></a>

<img width="1920" height="1080" alt="Screenshot (377)" src="https://github.com/user-attachments/assets/49758c00-0a90-4142-9b34-88fb14214260" />

> We need something to differenciate sane entries. That's called `key`

<img width="1920" height="1080" alt="Screenshot (379)" src="https://github.com/user-attachments/assets/4bb83afc-11f1-447e-b76f-9cd141dbd098" />
<img width="1920" height="1080" alt="Screenshot (380)" src="https://github.com/user-attachments/assets/24b3ade1-96d8-4d68-98eb-20ee370220ac" />
<img width="1920" height="1080" alt="Screenshot (381)" src="https://github.com/user-attachments/assets/33ad54d5-3e32-43b2-9c01-8b334436c128" />
<img width="1920" height="1080" alt="Screenshot (382)" src="https://github.com/user-attachments/assets/4f584c89-af8f-45ac-9db8-3a430c9946be" />
<img width="1920" height="1080" alt="Screenshot (383)" src="https://github.com/user-attachments/assets/07e6d81f-eafa-43c0-a2a4-66fab20ade63" />

- Key is the `data item` in RDBMS which exclusively `identify the records` of table.
- **☀️ Primary Key :** it's a key field `uniqly identify eatch racord` of table. ⚠️ Eatch column has a unique value
- **☀️ Candidate Key :** If many column has unique value ⚠️ but onlu one Column is `Primary Key`,✅ So one of anothers is `Condidate Kay`.
- **☀️ Alternate Key :**  If many column has unique value ⚠️ but onlu one Column is `Primary Key`,✅ So all other `eligible` (unique value) columns are `Alternate key`. 
- **☀️ Composite Key :** If two column has no unique value❌ but the combination of this type of two columns are create a unique (marge) column.
- **☀️ Foreign Key :** uniqly identify the records of another table.
- **☀️ Unique Key :** `same` --> use to identify unique records from a table. But it's allow `NULL` but Primary Key not.

The **difference between a primary key and a candidate key** in a relational database is as follows:

### 1. **Candidate Key**

* A **candidate key** is **any column or combination of columns** that can uniquely identify a row in a table.
* There can be **multiple candidate keys** in a table.
* Each candidate key must be **unique** and **not null**.

### 2. **Primary Key**

* A **primary key** is a **specific candidate key** that is **chosen by the database designer** to uniquely identify records in the table.
* There can be **only one primary key** per table.
* It also must be **unique** and **not null**, and is often used as a reference in foreign key relationships.

### Summary Table:

| Feature     | Candidate Key          | Primary Key        |
| ----------- | ---------------------- | ------------------ |
| Uniqueness  | Must be unique         | Must be unique     |
| Null Values | Not allowed            | Not allowed        |
| Quantity    | Can be many in a table | Only one per table |
| Purpose     | Potential identifier   | Chosen identifier  |

**Example:**
In a `Students` table:

* `student_id`, `email`, and `phone_number` could all be candidate keys.
* If `student_id` is chosen as the main identifier, it becomes the **primary key**.

## ✅ ER Model <a name="er-model"></a>

- ER --> Entity relationship model. [Video Link](https://youtu.be/GBjLgU1WZvo)
- also known as Conceptual frameWork, use to describe and design the structure of a database.
  │
  │── The graphical representation of relationship of table is called ER-diagram.
  └── and The model through which use describe the relationship called ER-model.

```yaml
  Relationship
     │
     │── 1:1
     │── 1: M
     └── M:M
```  

<img src="https://github.com/akashdip2001/college-final-year-project/blob/main/img/colour_line.png">

# 3. SQL Basics <a name="sql-basics"></a>

**SQL (Structured Query Language)** is the standard language for interacting with RDBMS. **ANSI SQL** is the standardized version of SQL.

<img width="1920" height="1080" alt="Screenshot (394)" src="https://github.com/user-attachments/assets/b38bf54f-34ec-4e17-93e7-be29a5e61199" />
<img width="1920" height="1080" alt="Screenshot (395)" src="https://github.com/user-attachments/assets/86a9ca88-cf5e-475a-adde-d5d95cc44c10" />

<p align="center">
  <img src="https://github.com/user-attachments/assets/30b244dd-07f4-4f54-b538-55ab6db17bb8" width="45%" />
  <img src="https://github.com/user-attachments/assets/ffa140b8-75ad-4154-aa8f-86cc4e6de351" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/47fe120d-49fd-4718-852b-f2f8b2b49a86" width="45%" />
  <img src="https://github.com/user-attachments/assets/0aa47a8e-baf6-4179-93be-39621ebea955" width="45%" />
</p>

<img width="1920" height="1080" alt="Screenshot (402)" src="https://github.com/user-attachments/assets/a6f72b35-2c87-4cf1-8d81-7c922cc853dc" />

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

---

<img width="1920" height="1080" alt="Screenshot (420)" src="https://github.com/user-attachments/assets/4170fb80-69d6-4dbc-b552-cfff3b505bc3" />

<p align="center">
  <img src="https://github.com/user-attachments/assets/eea24562-026e-4c81-98f7-de86e8d95220" width="46%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/709f4c55-3c37-4333-83c6-7611b73a545d" width="46%" />
</p>

</br>

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/814fce11-64ad-4060-a048-c82ff959e154" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/592ff6c0-f071-4207-8863-ebec53ad9051" width="45%" />
</p>

### Show the Table
```sql
desc employees
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

<img width="1920" height="1080" alt="Screenshot (427)" src="https://github.com/user-attachments/assets/09420349-b6b5-4ad5-8b18-1407dc05096d" />

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/a3d547d2-86ce-4ca6-8070-d41fb995e6d7" width="33%" />
  <img src="https://github.com/user-attachments/assets/f82ef64a-b33c-44b2-8a7e-01c1f886af3d" width="33%" />
  <img src="https://github.com/user-attachments/assets/95175dfe-4985-4a36-a5f2-40359d9a8a5f" width="33%" />
</p>

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/62780a29-426c-48b2-9589-17164d00ffa5" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/7977caa0-8548-47a2-8a66-7372bf456518" width="45%" />
</p>

<details>
  <summary style="opacity: 0.85;"><b>more SQL Clauses</b></summary><br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/ea25df91-7377-4e9d-b91b-b64d3271b8ab" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/ac19b8db-6402-4b32-9538-757e4cfe1fb7" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f719c124-8f44-4c97-97ce-f727bd398ab9" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/57f9d265-577b-42f1-b71c-f7bb0c7cd25a" width="45%" />
</p>

</br>
</br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/395eaedf-cbdc-440f-b3ae-38b98079467e" width="33%" />
  <img src="https://github.com/user-attachments/assets/7bbcc4ce-4a7f-4578-b4e9-0797c491c0c6" width="33%" />
  <img src="https://github.com/user-attachments/assets/a0779e03-22ee-4fd5-9453-8860ecfba2dc" width="33%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e9873b81-4eb2-4d20-adcc-eef695d98200" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/652a0237-2b58-4cc0-824b-c1ece81ef9e1" width="45%" />
</p>

</br>
</br>

</details>

### **INSERT Statement**
```sql
# Command Line Interface:
sql> INSERT INTO employees (employee_id, name, department, salary) 
       VALUES (101, 'Alice', 'HR', 55000);

# Output:
1 row inserted.
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/d7d73295-4b15-4f1f-88c7-8ec10e628bf8" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/a96a9585-218d-41c5-adf4-a5bea4ddac7f" width="45%" />
</p>

### **UPDATE Statement**
```sql
# Command Line Interface:
sql> UPDATE employees SET salary = 60000 WHERE name = 'Alice';

# Output:
1 row updated.
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/b2bd562f-6897-4dc1-a661-28ac57dee083" width="24%" /> &nbsp;
  <img src="https://github.com/user-attachments/assets/179c45c5-c912-48c8-8183-286c9c3e19ad" width="24%" /> &nbsp;
  <img src="https://github.com/user-attachments/assets/2be9438b-df76-4b1a-9827-6dea7d15fa04" width="24%" /> &nbsp;
  <img src="https://github.com/user-attachments/assets/e913d54a-991b-4830-8df0-d89acf738630" width="24%" />
</p>

### **DELETE Statement**
```sql
# Command Line Interface:
sql> DELETE FROM employees WHERE name = 'Alice';

# Output:
1 row deleted.
```

<p align="center">
  <img src="https://github.com/user-attachments/assets/7fef2f7c-0cb0-41c0-9bc1-cdd6921802b9" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/33254822-80b3-4268-8789-d9c14f918b2c" width="45%" />
</p>

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

</br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f01b4842-cd10-4a04-a745-b526f18353eb" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/b200ce3f-fbdc-4a35-8f47-68a4a19620ad" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/aaf11cd0-e6ae-4ab4-b712-26d813d13c4e" width="33%" />
  <img src="https://github.com/user-attachments/assets/7e5e3ec9-10f9-4ee6-8c39-25deefa72ee5" width="33%" />
  <img src="https://github.com/user-attachments/assets/57d33e9b-ece4-4c3c-a979-af3230f17871" width="33%" />
</p>

</br>

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/62780a29-426c-48b2-9589-17164d00ffa5" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/7977caa0-8548-47a2-8a66-7372bf456518" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/ea25df91-7377-4e9d-b91b-b64d3271b8ab" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/ac19b8db-6402-4b32-9538-757e4cfe1fb7" width="45%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/f719c124-8f44-4c97-97ce-f727bd398ab9" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/57f9d265-577b-42f1-b71c-f7bb0c7cd25a" width="45%" />
</p>

</br>
</br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/395eaedf-cbdc-440f-b3ae-38b98079467e" width="33%" />
  <img src="https://github.com/user-attachments/assets/7bbcc4ce-4a7f-4578-b4e9-0797c491c0c6" width="33%" />
  <img src="https://github.com/user-attachments/assets/a0779e03-22ee-4fd5-9453-8860ecfba2dc" width="33%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/e9873b81-4eb2-4d20-adcc-eef695d98200" width="45%" /> &nbsp; &nbsp;
  <img src="https://github.com/user-attachments/assets/652a0237-2b58-4cc0-824b-c1ece81ef9e1" width="45%" />
</p>

</br>
</br>

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

<p align="center">
  <img src="https://github.com/user-attachments/assets/ecc1711e-f356-4484-9eb3-8ec3af7e92e0" width="33%" />
  <img src="https://github.com/user-attachments/assets/f0cf77c1-bee1-46f7-9fb8-9a348a6fd02a" width="33%" />
  <img src="https://github.com/user-attachments/assets/ca53ddba-0137-46f9-87d3-2d4299e6b1d5" width="33%" />
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/44e00226-7890-4e7c-ae10-b9ebc351a8b0" width="33%" />
  <img src="https://github.com/user-attachments/assets/b3878257-2e3d-49b3-8060-c4cd8cb5f0e5" width="33%" />
  <img src="https://github.com/user-attachments/assets/6dae26d4-b60f-4adb-9737-ad14cd03bb2e" width="33%" />
</p>

<details>
  <summary style="opacity: 0.85;"><b>more Advanced query</b></summary><br>

<p align="center">
  <img src="https://github.com/user-attachments/assets/c5f09b41-688c-4dc2-bf7c-58cd90a46760" width="33%" />
  <img src="https://github.com/user-attachments/assets/ffcb7ad0-aed4-4786-aac2-f9a740dd52f2" width="33%" />
  <img src="https://github.com/user-attachments/assets/1c9a80ca-8e63-4056-aa44-710f8211219d" width="33%" />
</p>

</details>
  
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

- [Oracle Exam 1Z0-922: MySQL Implementation Associate Dump](https://github.com/debabrata2050/Oracle-Certificate/blob/main/MySQL%20Implementation%20Associate%20(1Z0-922)/Oracle%201Z0-922%20Exam%20Dump.md)
- Job Exam

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

---

## 🗄️ Database Structure using in my APP for login <a name="app-sql-explane"></a>

my MySQL database includes a `users` table to store user information.

**Example:**

```sql
CREATE TABLE users (
  id INT AUTO_INCREMENT PRIMARY KEY,
  username VARCHAR(50) NOT NULL UNIQUE,
  email VARCHAR(100) NOT NULL UNIQUE,
  password VARCHAR(255) NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

This schema ensures unique usernames and emails, storing hashed passwords securely.

# [Explane line by line](https://github.com/Engineering-college-btech-Project2/Project-2/blob/main/README.md#app-sql-explane)




