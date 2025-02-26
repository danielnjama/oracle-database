# Oracle Database for Beginners

## Course Overview
This course is designed for beginners who want to learn Oracle Database from scratch. It covers fundamental concepts, SQL queries, database administration, and basic performance tuning.

## Prerequisites
- Basic understanding of databases (optional but helpful)
- Familiarity with SQL syntax (not mandatory)
- Willingness to learn database management concepts

## Course Outline

### **Module 1: Introduction to Oracle Database**
- What is Oracle Database?
- Features and Benefits of Oracle
- Oracle Database Editions
- Installation and Setup (Windows/Linux)
- Connecting to Oracle Database (SQL*Plus, SQL Developer)

### **Module 2: SQL Basics**
- Understanding SQL and PL/SQL
- Data Types in Oracle
- DDL (CREATE, ALTER, DROP)
- DML (INSERT, UPDATE, DELETE)
- DQL (SELECT, WHERE, ORDER BY)
- TCL (COMMIT, ROLLBACK, SAVEPOINT)

### **Module 3: Advanced SQL Queries**
- Joins (INNER, LEFT, RIGHT, FULL)
- Subqueries and Nested Queries
- Aggregate Functions (SUM, AVG, COUNT)
- Views and Indexes
- Sequences and Synonyms

### **Module 4: Database Administration Basics**
- Understanding Users and Roles
- Creating and Managing Users
- Granting and Revoking Privileges
- Tablespaces and Datafiles
- Backup and Restore Basics

### **Module 5: PL/SQL Programming**
- Introduction to PL/SQL
- Anonymous Blocks and Stored Procedures
- Functions and Packages
- Triggers and Cursors

### **Module 6: Performance Tuning Basics**
- Understanding Execution Plans
- Optimizing Queries with Indexes
- Partitioning in Oracle
- Basic Troubleshooting

### **Module 7: Practical Implementation**
- Creating a Sample Database
- Writing SQL Queries for Real-world Scenarios
- Performing Database Backup and Restore
- Administering Users and Security

## Resources
- [Oracle Official Documentation](https://docs.oracle.com/en/database/)
- [Oracle Live SQL](https://livesql.oracle.com/)
- [SQL & PL/SQL Tutorials](https://www.oracle.com/database/technologies/appdev/sql.html)

## Certification & Next Steps
- Oracle Database SQL Certification (1Z0-071)
- Oracle Database Administration Certification (1Z0-082)
- Learning Advanced Oracle Features (RAC, Data Guard, Performance Tuning)

---
**Author:** Dynamic Technologies  
**Website:** [Your Website Link]  
**YouTube Channel:** [Your YouTube Channel Link]  


# Module 1: Introduction to Oracle Database

This module provides an overview of Oracle Database, its features, editions, installation, and connection methods.

---

## **Topics Covered**

### 1. What is Oracle Database?
- Oracle Database is a multi-model database management system developed by Oracle Corporation.
- It is widely used for enterprise-level data management, offering robust features for data storage, retrieval, and manipulation.

### 2. Features and Benefits of Oracle
- **Scalability**: Handles large volumes of data efficiently.
- **Security**: Advanced security features like encryption and access control.
- **High Availability**: Ensures minimal downtime with features like Real Application Clusters (RAC).
- **Performance**: Optimized for high-speed data processing and query execution.
- **Backup and Recovery**: Comprehensive tools for data backup and disaster recovery.

### 3. Oracle Database Editions
- **Enterprise Edition**: Full-featured version for large enterprises.
- **Standard Edition**: Suitable for small to medium-sized businesses.
- **Express Edition (XE)**: Free, lightweight version for learning and development.
- **Personal Edition**: Single-user version for development and testing.

### 4. Installation and Setup (Windows/Linux)
- **Windows**:
  1. Download the Oracle Database installer from the official website.
  2. Run the installer and follow the on-screen instructions.
  3. Configure the database instance during installation.
- **Linux**:
  1. Download the Oracle Database RPM or ZIP file.
  2. Install prerequisite packages (e.g., `oracle-database-preinstall`).
  3. Run the installer and configure the database.

### 5. Connecting to Oracle Database
- **SQL*Plus**:
  - A command-line tool for interacting with Oracle Database.
  - Example: `sqlplus username/password@hostname:port/service_name`
- **SQL Developer**:
  - A graphical tool for database management and development.
  - Download and install SQL Developer, then configure a connection using the database credentials.

---


# Module 2: SQL Basics

This module introduces the fundamentals of SQL and PL/SQL, covering data types, DDL, DML, DQL, and TCL commands in Oracle Database.

---

## **Topics Covered**

### 1. Understanding SQL and PL/SQL
- **SQL (Structured Query Language)**:
  - A standard language for managing and manipulating relational databases.
  - Used for querying, updating, and managing data.
- **PL/SQL (Procedural Language/SQL)**:
  - Oracle's procedural extension to SQL.
  - Allows writing procedural logic like loops, conditions, and functions.

### 2. Data Types in Oracle
- **Character Types**: `CHAR`, `VARCHAR2`, `CLOB`
- **Numeric Types**: `NUMBER`, `INTEGER`, `FLOAT`
- **Date/Time Types**: `DATE`, `TIMESTAMP`, `INTERVAL`
- **LOB Types**: `BLOB`, `BFILE` (for large binary objects)
- **Other Types**: `RAW`, `ROWID`, `XMLType`

### 3. DDL (Data Definition Language)
- **CREATE**: Creates database objects like tables, views, and indexes.
  - Example: `CREATE TABLE employees (id NUMBER, name VARCHAR2(50));`
- **ALTER**: Modifies the structure of existing database objects.
  - Example: `ALTER TABLE employees ADD (salary NUMBER);`
- **DROP**: Deletes database objects.
  - Example: `DROP TABLE employees;`

### 4. DML (Data Manipulation Language)
- **INSERT**: Adds new rows to a table.
  - Example: `INSERT INTO employees (id, name) VALUES (1, 'John Doe');`
- **UPDATE**: Modifies existing rows in a table.
  - Example: `UPDATE employees SET salary = 5000 WHERE id = 1;`
- **DELETE**: Removes rows from a table.
  - Example: `DELETE FROM employees WHERE id = 1;`

### 5. DQL (Data Query Language)
- **SELECT**: Retrieves data from one or more tables.
  - Example: `SELECT * FROM employees;`
- **WHERE**: Filters rows based on a condition.
  - Example: `SELECT * FROM employees WHERE salary > 3000;`
- **ORDER BY**: Sorts the result set.
  - Example: `SELECT * FROM employees ORDER BY name ASC;`

### 6. TCL (Transaction Control Language)
- **COMMIT**: Saves changes made during the current transaction.
  - Example: `COMMIT;`
- **ROLLBACK**: Undoes changes made during the current transaction.
  - Example: `ROLLBACK;`
- **SAVEPOINT**: Sets a point within a transaction to which you can later roll back.
  - Example: `SAVEPOINT sp1;`

---

# Module 3: Advanced SQL Queries

This module dives into advanced SQL concepts, including joins, subqueries, aggregate functions, views, indexes, sequences, and synonyms in Oracle Database.

---

## **Topics Covered**

### 1. Joins
- **INNER JOIN**: Retrieves rows with matching values in both tables.
  - Example: `SELECT employees.name, departments.department_name FROM employees INNER JOIN departments ON employees.department_id = departments.department_id;`
- **LEFT JOIN**: Retrieves all rows from the left table and matching rows from the right table.
  - Example: `SELECT employees.name, departments.department_name FROM employees LEFT JOIN departments ON employees.department_id = departments.department_id;`
- **RIGHT JOIN**: Retrieves all rows from the right table and matching rows from the left table.
  - Example: `SELECT employees.name, departments.department_name FROM employees RIGHT JOIN departments ON employees.department_id = departments.department_id;`
- **FULL JOIN**: Retrieves all rows when there is a match in either the left or right table.
  - Example: `SELECT employees.name, departments.department_name FROM employees FULL JOIN departments ON employees.department_id = departments.department_id;`

### 2. Subqueries and Nested Queries
- **Subquery**: A query nested inside another query.
  - Example: `SELECT name FROM employees WHERE department_id = (SELECT department_id FROM departments WHERE department_name = 'Sales');`
- **Nested Query**: A subquery within another subquery.
  - Example: `SELECT name FROM employees WHERE department_id = (SELECT department_id FROM departments WHERE location_id = (SELECT location_id FROM locations WHERE city = 'New York'));`

### 3. Aggregate Functions
- **SUM**: Calculates the total sum of a numeric column.
  - Example: `SELECT SUM(salary) FROM employees;`
- **AVG**: Calculates the average value of a numeric column.
  - Example: `SELECT AVG(salary) FROM employees;`
- **COUNT**: Counts the number of rows.
  - Example: `SELECT COUNT(*) FROM employees;`
- **GROUP BY**: Groups rows that have the same values into summary rows.
  - Example: `SELECT department_id, AVG(salary) FROM employees GROUP BY department_id;`
- **HAVING**: Filters groups based on a condition.
  - Example: `SELECT department_id, AVG(salary) FROM employees GROUP BY department_id HAVING AVG(salary) > 5000;`

### 4. Views and Indexes
- **Views**: Virtual tables created by a query.
  - Example: `CREATE VIEW employee_view AS SELECT name, salary FROM employees WHERE department_id = 10;`
- **Indexes**: Improves the speed of data retrieval.
  - Example: `CREATE INDEX idx_employee_name ON employees(name);`

### 5. Sequences and Synonyms
- **Sequences**: Generates unique numeric values, often used for primary keys.
  - Example: `CREATE SEQUENCE employee_seq START WITH 1 INCREMENT BY 1;`
- **Synonyms**: Alternative names for database objects.
  - Example: `CREATE SYNONYM emp FOR employees;`

---

# Module 4: Database Administration Basics

This module introduces the fundamentals of database administration in Oracle, covering users, roles, privileges, tablespaces, datafiles, and backup/restore operations.

---

## **Topics Covered**

### 1. Understanding Users and Roles
- **Users**: Accounts that can connect to and interact with the database.
  - Example: `CREATE USER john_doe IDENTIFIED BY password;`
- **Roles**: Collections of privileges that can be assigned to users.
  - Example: `CREATE ROLE manager;`

### 2. Creating and Managing Users
- **Creating Users**:
  - Example: `CREATE USER jane_doe IDENTIFIED BY password;`
- **Modifying Users**:
  - Example: `ALTER USER jane_doe IDENTIFIED BY new_password;`
- **Dropping Users**:
  - Example: `DROP USER jane_doe;`

### 3. Granting and Revoking Privileges
- **Granting Privileges**: Assigning permissions to users or roles.
  - Example: `GRANT SELECT, INSERT ON employees TO manager;`
- **Revoking Privileges**: Removing permissions from users or roles.
  - Example: `REVOKE INSERT ON employees FROM manager;`

### 4. Tablespaces and Datafiles
- **Tablespaces**: Logical storage units that group related database objects.
  - Example: `CREATE TABLESPACE ts_data DATAFILE 'ts_data.dbf' SIZE 100M;`
- **Datafiles**: Physical files on disk that store the data of tablespaces.
  - Example: `ALTER TABLESPACE ts_data ADD DATAFILE 'ts_data2.dbf' SIZE 50M;`

### 5. Backup and Restore Basics
- **Backup**: Creating copies of the database to prevent data loss.
  - Example: `RMAN> BACKUP DATABASE;`
- **Restore**: Recovering the database from a backup in case of failure.
  - Example: `RMAN> RESTORE DATABASE;`

---
# Module 5: PL/SQL Programming

This module introduces PL/SQL (Procedural Language/SQL), Oracle's procedural extension to SQL. It covers anonymous blocks, stored procedures, functions, packages, triggers, and cursors.

---

## **Topics Covered**

### 1. Introduction to PL/SQL
- **What is PL/SQL?**
  - A procedural language that combines SQL with procedural constructs like loops, conditions, and exception handling.
  - Used for writing complex database logic and applications.
- **Advantages of PL/SQL**:
  - Improved performance due to reduced network traffic.
  - Better error handling with exception management.
  - Modular and reusable code.

### 2. Anonymous Blocks and Stored Procedures
- **Anonymous Blocks**:
  - Unnamed PL/SQL blocks that are executed immediately.
  - Example:
    ```sql
    DECLARE
      v_name VARCHAR2(50);
    BEGIN
      SELECT name INTO v_name FROM employees WHERE id = 1;
      DBMS_OUTPUT.PUT_LINE('Employee Name: ' || v_name);
    END;
    ```
- **Stored Procedures**:
  - Named PL/SQL blocks stored in the database for reuse.
  - Example:
    ```sql
    CREATE OR REPLACE PROCEDURE get_employee_name (p_id IN NUMBER, p_name OUT VARCHAR2) IS
    BEGIN
      SELECT name INTO p_name FROM employees WHERE id = p_id;
    END;
    ```

### 3. Functions and Packages
- **Functions**:
  - Named PL/SQL blocks that return a value.
  - Example:
    ```sql
    CREATE OR REPLACE FUNCTION calculate_bonus (p_salary NUMBER) RETURN NUMBER IS
    BEGIN
      RETURN p_salary * 0.1; -- 10% bonus
    END;
    ```
- **Packages**:
  - Groups of related procedures, functions, variables, and cursors.
  - Example:
    ```sql
    CREATE OR REPLACE PACKAGE employee_pkg IS
      PROCEDURE get_employee_name(p_id IN NUMBER, p_name OUT VARCHAR2);
      FUNCTION calculate_bonus(p_salary NUMBER) RETURN NUMBER;
    END employee_pkg;
    ```

### 4. Triggers and Cursors
- **Triggers**:
  - PL/SQL blocks that automatically execute in response to specific database events (e.g., INSERT, UPDATE, DELETE).
  - Example:
    ```sql
    CREATE OR REPLACE TRIGGER before_employee_insert
    BEFORE INSERT ON employees
    FOR EACH ROW
    BEGIN
      :NEW.created_date := SYSDATE;
    END;
    ```
- **Cursors**:
  - Used to process multiple rows returned by a query.
  - Example:
    ```sql
    DECLARE
      CURSOR c_employees IS SELECT name FROM employees;
      v_name employees.name%TYPE;
    BEGIN
      OPEN c_employees;
      LOOP
        FETCH c_employees INTO v_name;
        EXIT WHEN c_employees%NOTFOUND;
        DBMS_OUTPUT.PUT_LINE('Employee Name: ' || v_name);
      END LOOP;
      CLOSE c_employees;
    END;
    ```

---


# Module 6: Performance Tuning Basics

This module introduces the fundamentals of performance tuning in Oracle Database, covering execution plans, query optimization, partitioning, and basic troubleshooting techniques.

---

## **Topics Covered**

### 1. Understanding Execution Plans
- **What is an Execution Plan?**
  - A roadmap that shows how Oracle executes a SQL query.
  - Helps identify performance bottlenecks.
- **How to Generate an Execution Plan**:
  - Use `EXPLAIN PLAN` or tools like SQL Developer.
  - Example:
    ```sql
    EXPLAIN PLAN FOR
    SELECT * FROM employees WHERE department_id = 10;
    SELECT * FROM TABLE(DBMS_XPLAN.DISPLAY);
    ```
- **Key Components**:
  - Full Table Scan, Index Scan, Join Methods, and Cost.

### 2. Optimizing Queries with Indexes
- **What are Indexes?**
  - Database objects that improve the speed of data retrieval.
- **Types of Indexes**:
  - **B-Tree Index**: Default index type for most queries.
    - Example: `CREATE INDEX idx_employee_name ON employees(name);`
  - **Bitmap Index**: Suitable for low-cardinality columns.
    - Example: `CREATE BITMAP INDEX idx_gender ON employees(gender);`
- **Best Practices**:
  - Index columns used in `WHERE`, `JOIN`, and `ORDER BY` clauses.
  - Avoid over-indexing, as it can slow down `INSERT`/`UPDATE` operations.

### 3. Partitioning in Oracle
- **What is Partitioning?**
  - Dividing large tables into smaller, manageable pieces (partitions).
  - Improves query performance and maintenance.
- **Types of Partitioning**:
  - **Range Partitioning**: Based on a range of values (e.g., dates).
    - Example:
      ```sql
      CREATE TABLE sales (
        sale_id NUMBER,
        sale_date DATE
      ) PARTITION BY RANGE (sale_date) (
        PARTITION p1 VALUES LESS THAN (TO_DATE('2023-01-01', 'YYYY-MM-DD')),
        PARTITION p2 VALUES LESS THAN (TO_DATE('2024-01-01', 'YYYY-MM-DD'))
      );
      ```
  - **List Partitioning**: Based on specific values (e.g., regions).
  - **Hash Partitioning**: Distributes data evenly across partitions.

### 4. Basic Troubleshooting
- **Common Performance Issues**:
  - High CPU or I/O usage.
  - Slow-running queries.
  - Lock contention.
- **Tools for Troubleshooting**:
  - **AWR (Automatic Workload Repository)**: Captures performance data.
  - **ADDM (Automatic Database Diagnostic Monitor)**: Analyzes performance issues.
  - **SQL Trace and TKPROF**: Identifies slow SQL statements.
- **Steps for Troubleshooting**:
  1. Identify the problem (e.g., slow query, high resource usage).
  2. Analyze execution plans and statistics.
  3. Optimize queries, indexes, or database configuration.
  4. Monitor and validate improvements.

---

# Module 7: Practical Implementation

This module focuses on hands-on implementation of Oracle Database concepts, including creating a sample database, writing SQL queries for real-world scenarios, performing backup and restore operations, and administering users and security.

---

## **Topics Covered**

### 1. Creating a Sample Database
- **Steps to Create a Sample Database**:
  1. Design the database schema (tables, relationships, and constraints).
  2. Create tables using `CREATE TABLE`.
     - Example:
       ```sql
       CREATE TABLE employees (
         employee_id NUMBER PRIMARY KEY,
         first_name VARCHAR2(50),
         last_name VARCHAR2(50),
         department_id NUMBER,
         hire_date DATE
       );
       ```
  3. Insert sample data using `INSERT`.
     - Example:
       ```sql
       INSERT INTO employees (employee_id, first_name, last_name, department_id, hire_date)
       VALUES (1, 'John', 'Doe', 10, TO_DATE('2023-01-01', 'YYYY-MM-DD'));
       ```
  4. Add constraints (e.g., foreign keys, unique keys).
     - Example:
       ```sql
       ALTER TABLE employees ADD CONSTRAINT fk_department FOREIGN KEY (department_id) REFERENCES departments(department_id);
       ```

### 2. Writing SQL Queries for Real-world Scenarios
- **Example Scenarios**:
  - Retrieve all employees in a specific department.
    - Example:
      ```sql
      SELECT * FROM employees WHERE department_id = 10;
      ```
  - Calculate the average salary by department.
    - Example:
      ```sql
      SELECT department_id, AVG(salary) FROM employees GROUP BY department_id;
      ```
  - Find employees hired in the last year.
    - Example:
      ```sql
      SELECT * FROM employees WHERE hire_date >= ADD_MONTHS(SYSDATE, -12);
      ```
  - Join tables to retrieve employee details with department names.
    - Example:
      ```sql
      SELECT e.first_name, e.last_name, d.department_name
      FROM employees e
      JOIN departments d ON e.department_id = d.department_id;
      ```

### 3. Performing Database Backup and Restore
- **Backup**:
  - Use Oracle Recovery Manager (RMAN) to create backups.
    - Example:
      ```bash
      RMAN> BACKUP DATABASE;
      ```
  - Export data using `expdp` (Data Pump).
    - Example:
      ```bash
      expdp username/password@dbname DIRECTORY=backup_dir DUMPFILE=backup.dmp SCHEMAS=hr;
      ```
- **Restore**:
  - Use RMAN to restore the database.
    - Example:
      ```bash
      RMAN> RESTORE DATABASE;
      ```
  - Import data using `impdp` (Data Pump).
    - Example:
      ```bash
      impdp username/password@dbname DIRECTORY=backup_dir DUMPFILE=backup.dmp SCHEMAS=hr;
      ```

### 4. Administering Users and Security
- **Creating Users**:
  - Example:
    ```sql
    CREATE USER new_user IDENTIFIED BY password;
    ```
- **Granting Privileges**:
  - Example:
    ```sql
    GRANT CONNECT, RESOURCE TO new_user;
    GRANT SELECT ON employees TO new_user;
    ```
- **Revoking Privileges**:
  - Example:
    ```sql
    REVOKE SELECT ON employees FROM new_user;
    ```
- **Managing Roles**:
  - Example:
    ```sql
    CREATE ROLE manager;
    GRANT SELECT, INSERT, UPDATE ON employees TO manager;
    GRANT manager TO new_user;
    ```

---

# Oracle SQL Hands-on 

## 1. Introduction to Oracle SQL
- Overview of SQL and its importance
- Introduction to Oracle Database
- Setting up Oracle SQL Developer or SQL*Plus

## 2. Basic SQL Queries
- **SELECT Statement**
  - Syntax: `SELECT column1, column2 FROM table_name;`
  - Example: `SELECT first_name, last_name FROM employees;`
- **WHERE Clause**
  - Syntax: `SELECT column1, column2 FROM table_name WHERE condition;`
  - Example: `SELECT * FROM employees WHERE salary > 50000;`
- **ORDER BY Clause**
  - Syntax: `SELECT column1, column2 FROM table_name ORDER BY column1 ASC|DESC;`
  - Example: `SELECT first_name, last_name FROM employees ORDER BY last_name ASC;`

## 3. Data Manipulation Language (DML)
- **INSERT Statement**
  - Syntax: `INSERT INTO table_name (column1, column2) VALUES (value1, value2);`
  - Example: `INSERT INTO employees (first_name, last_name) VALUES ('John', 'Doe');`
- **UPDATE Statement**
  - Syntax: `UPDATE table_name SET column1 = value1 WHERE condition;`
  - Example: `UPDATE employees SET salary = 60000 WHERE employee_id = 101;`
- **DELETE Statement**
  - Syntax: `DELETE FROM table_name WHERE condition;`
  - Example: `DELETE FROM employees WHERE employee_id = 102;`

## 4. Data Definition Language (DDL)
- **CREATE TABLE Statement**
  - Syntax: `CREATE TABLE table_name (column1 datatype, column2 datatype, ...);`
  - Example: `CREATE TABLE employees (employee_id NUMBER, first_name VARCHAR2(50), last_name VARCHAR2(50));`
- **ALTER TABLE Statement**
  - Syntax: `ALTER TABLE table_name ADD column_name datatype;`
  - Example: `ALTER TABLE employees ADD email VARCHAR2(100);`
- **DROP TABLE Statement**
  - Syntax: `DROP TABLE table_name;`
  - Example: `DROP TABLE employees;`

## 5. Constraints
- **Primary Key**
  - Syntax: `CREATE TABLE table_name (column1 datatype PRIMARY KEY, column2 datatype);`
  - Example: `CREATE TABLE employees (employee_id NUMBER PRIMARY KEY, first_name VARCHAR2(50));`
- **Foreign Key**
  - Syntax: `CREATE TABLE table_name (column1 datatype, column2 datatype, FOREIGN KEY (column1) REFERENCES other_table(column_name));`
  - Example: `CREATE TABLE orders (order_id NUMBER, employee_id NUMBER, FOREIGN KEY (employee_id) REFERENCES employees(employee_id));`
- **NOT NULL Constraint**
  - Syntax: `CREATE TABLE table_name (column1 datatype NOT NULL, column2 datatype);`
  - Example: `CREATE TABLE employees (employee_id NUMBER NOT NULL, first_name VARCHAR2(50));`
- **UNIQUE Constraint**
  - Syntax: `CREATE TABLE table_name (column1 datatype UNIQUE, column2 datatype);`
  - Example: `CREATE TABLE employees (employee_id NUMBER UNIQUE, first_name VARCHAR2(50));`

## 6. Joins
- **INNER JOIN**
  - Syntax: `SELECT columns FROM table1 INNER JOIN table2 ON table1.column = table2.column;`
  - Example: `SELECT employees.first_name, departments.department_name FROM employees INNER JOIN departments ON employees.department_id = departments.department_id;`
- **LEFT JOIN**
  - Syntax: `SELECT columns FROM table1 LEFT JOIN table2 ON table1.column = table2.column;`
  - Example: `SELECT employees.first_name, departments.department_name FROM employees LEFT JOIN departments ON employees.department_id = departments.department_id;`
- **RIGHT JOIN**
  - Syntax: `SELECT columns FROM table1 RIGHT JOIN table2 ON table1.column = table2.column;`
  - Example: `SELECT employees.first_name, departments.department_name FROM employees RIGHT JOIN departments ON employees.department_id = departments.department_id;`
- **FULL OUTER JOIN**
  - Syntax: `SELECT columns FROM table1 FULL OUTER JOIN table2 ON table1.column = table2.column;`
  - Example: `SELECT employees.first_name, departments.department_name FROM employees FULL OUTER JOIN departments ON employees.department_id = departments.department_id;`

## 7. Aggregare Functions
- **COUNT**
  - Syntax: `SELECT COUNT(column_name) FROM table_name;`
  - Example: `SELECT COUNT(employee_id) FROM employees;`
- **SUM**
  - Syntax: `SELECT SUM(column_name) FROM table_name;`
  - Example: `SELECT SUM(salary) FROM employees;`
- **AVG**
  - Syntax: `SELECT AVG(column_name) FROM table_name;`
  - Example: `SELECT AVG(salary) FROM employees;`
- **MIN**
  - Syntax: `SELECT MIN(column_name) FROM table_name;`
  - Example: `SELECT MIN(salary) FROM employees;`
- **MAX**
  - Syntax: `SELECT MAX(column_name) FROM table_name;`
  - Example: `SELECT MAX(salary) FROM employees;`

## 8. Group By and Having
- **GROUP BY Clause**
  - Syntax: `SELECT column1, COUNT(column2) FROM table_name GROUP BY column1;`
  - Example: `SELECT department_id, COUNT(employee_id) FROM employees GROUP BY department_id;`
- **HAVING Clause**
  - Syntax: `SELECT column1, COUNT(column2) FROM table_name GROUP BY column1 HAVING condition;`
  - Example: `SELECT department_id, COUNT(employee_id) FROM employees GROUP BY department_id HAVING COUNT(employee_id) > 5;`

## 9. Subqueries
- **Single-Row Subquery**
  - Syntax: `SELECT column1 FROM table_name WHERE column2 = (SELECT column2 FROM table_name WHERE condition);`
  - Example: `SELECT first_name FROM employees WHERE salary = (SELECT MAX(salary) FROM employees);`
- **Multiple-Row Subquery**
  - Syntax: `SELECT column1 FROM table_name WHERE column2 IN (SELECT column2 FROM table_name WHERE condition);`
  - Example: `SELECT first_name FROM employees WHERE department_id IN (SELECT department_id FROM departments WHERE location_id = 1700);`

## 10. Views
- **CREATE VIEW**
  - Syntax: `CREATE VIEW view_name AS SELECT column1, column2 FROM table_name WHERE condition;`
  - Example: `CREATE VIEW high_salary_employees AS SELECT first_name, last_name FROM employees WHERE salary > 70000;`
- **DROP VIEW**
  - Syntax: `DROP VIEW view_name;`
  - Example: `DROP VIEW high_salary_employees;`

## 11. Indexes
- **CREATE INDEX**
  - Syntax: `CREATE INDEX index_name ON table_name (column1, column2);`
  - Example: `CREATE INDEX idx_employee_name ON employees (first_name, last_name);`
- **DROP INDEX**
  - Syntax: `DROP INDEX index_name;`
  - Example: `DROP INDEX idx_employee_name;`

## 12. Transactions
- **COMMIT**
  - Syntax: `COMMIT;`
  - Example: `UPDATE employees SET salary = 75000 WHERE employee_id = 101; COMMIT;`
- **ROLLBACK**
  - Syntax: `ROLLBACK;`
  - Example: `UPDATE employees SET salary = 75000 WHERE employee_id = 101; ROLLBACK;`
- **SAVEPOINT**
  - Syntax: `SAVEPOINT savepoint_name;`
  - Example: `SAVEPOINT before_update; UPDATE employees SET salary = 75000 WHERE employee_id = 101; ROLLBACK TO before_update;`

## 13. Advanced SQL
- **Window Functions**
  - Syntax: `SELECT column1, ROW_NUMBER() OVER (ORDER BY column2) FROM table_name;`
  - Example: `SELECT first_name, ROW_NUMBER() OVER (ORDER BY salary DESC) FROM employees;`
- **Common Table Expressions (CTEs)**
  - Syntax: `WITH cte_name AS (SELECT column1 FROM table_name) SELECT * FROM cte_name;`
  - Example: `WITH high_salary AS (SELECT * FROM employees WHERE salary > 70000) SELECT * FROM high_salary;`
- **PIVOT and UNPIVOT**
  - Syntax: `SELECT * FROM (SELECT column1, column2 FROM table_name) PIVOT (aggregate_function(column2) FOR column1 IN (value1, value2));`
  - Example: `SELECT * FROM (SELECT department_id, salary FROM employees) PIVOT (AVG(salary) FOR department_id IN (10, 20, 30));`

## 14. Performance Tuning
- **EXPLAIN PLAN**
  - Syntax: `EXPLAIN PLAN FOR SELECT * FROM table_name;`
  - Example: `EXPLAIN PLAN FOR SELECT * FROM employees WHERE salary > 50000;`
- **Index Optimization**
  - Example: `CREATE INDEX idx_salary ON employees (salary);`
- **Query Refactoring**
  - Example: Refactor subqueries to joins for better performance.

## 15. PL/SQL Basics
- **PL/SQL Block Structure**
  - Syntax: `DECLARE ... BEGIN ... END;`
  - Example: `DECLARE v_name VARCHAR2(50); BEGIN SELECT first_name INTO v_name FROM employees WHERE employee_id = 101; END;`
- **Cursors**
  - Syntax: `DECLARE CURSOR cursor_name IS SELECT column1 FROM table_name;`
  - Example: `DECLARE CURSOR emp_cursor IS SELECT first_name FROM employees;`
- **Stored Procedures**
  - Syntax: `CREATE OR REPLACE PROCEDURE procedure_name IS BEGIN ... END;`
  - Example: `CREATE OR REPLACE PROCEDURE increase_salary IS BEGIN UPDATE employees SET salary = salary * 1.1; END;`
- **Functions**
  - Syntax: `CREATE OR REPLACE FUNCTION function_name RETURN datatype IS BEGIN ... END;`
  - Example: `CREATE OR REPLACE FUNCTION get_employee_name (emp_id NUMBER) RETURN VARCHAR2 IS v_name VARCHAR2(50); BEGIN SELECT first_name INTO v_name FROM employees WHERE employee_id = emp_id; RETURN v_name; END;`

## 16. Security
- **User Management**
  - Syntax: `CREATE USER username IDENTIFIED BY password;`
  - Example: `CREATE USER john_doe IDENTIFIED BY password123;`
- **Granting Privileges**
  - Syntax: `GRANT privilege ON object TO user;`
  - Example: `GRANT SELECT ON employees TO john_doe;`
- **Revoking Privileges**
  - Syntax: `REVOKE privilege ON object FROM user;`
  - Example: `REVOKE SELECT ON employees FROM john_doe;`

## 17. Backup and Recovery
- **Exporting Data**
  - Example: `EXPDP username/password DIRECTORY=dir_name DUMPFILE=file_name.dmp TABLES=table_name;`
- **Importing Data**
  - Example: `IMPDP username/password DIRECTORY=dir_name DUMPFILE=file_name.dmp TABLES=table_name;`



