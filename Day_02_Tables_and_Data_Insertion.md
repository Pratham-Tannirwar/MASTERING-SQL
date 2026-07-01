# 📅 Day 02: Tables and Data Insertion

## 📖 Introduction

Tables are the foundation of every relational database. They organize data into rows and columns, making it easy to store, retrieve, and manage information. Before working with SQL queries, it's important to understand how to create tables and insert records into them.

---

# 🎯 Learning Objectives

After completing this topic, you will be able to:

* Create tables using `CREATE TABLE`
* Define appropriate data types
* Apply constraints like `PRIMARY KEY`
* Insert single and multiple records
* Understand the importance of table design

---

# 🛠 Database Setup Used

## Create Database

```sql
CREATE DATABASE student_db;
```

## Use Database

```sql
USE student_db;
```

## Create Table

```sql
CREATE TABLE students(
    id INT PRIMARY KEY,
    name VARCHAR(50),
    age INT,
    city VARCHAR(50),
    course VARCHAR(50),
    marks INT
);
```

---

## Insert Multiple Records

```sql
INSERT INTO students(id,name,age,city,course,marks)
VALUES
(101,'PRATHAM',21,'Pune','BCA',85),
(102,'Navin',22,'Pune','BCA',90),
(103,'ADITI',21,'Mumbai','BTech',95),
(104,'Amit',23,'Delhi','BCA',70),
(105,'GAURI',22,'Mumbai','BCom',88),
(106,'Rohit',20,'Pune','BTech',76),
(107,'KIRTI',21,'Delhi','BCA',92),
(108,'Neha',22,'Mumbai','BCom',80);
```

---

## View Data

```sql
SELECT * FROM students;
```

### Output

| ID  | Name    | Age | City   | Course | Marks |
| --- | ------- | --- | ------ | ------ | ----- |
| 101 | PRATHAM | 21  | Pune   | BCA    | 85    |
| 102 | Navin   | 22  | Pune   | BCA    | 90    |
| 103 | ADITI   | 21  | Mumbai | BTech  | 95    |
| 104 | Amit    | 23  | Delhi  | BCA    | 70    |
| 105 | GAURI   | 22  | Mumbai | BCom   | 88    |
| 106 | Rohit   | 20  | Pune   | BTech  | 76    |
| 107 | KIRTI   | 21  | Delhi  | BCA    | 92    |
| 108 | Neha    | 22  | Mumbai | BCom   | 80    |

---

# 📝 Syntax

## Create Table

```sql
CREATE TABLE table_name(
    column_name datatype constraint,
    column_name datatype constraint
);
```

## Insert Single Record

```sql
INSERT INTO table_name(column1,column2,...)
VALUES(value1,value2,...);
```

## Insert Multiple Records

```sql
INSERT INTO table_name(column1,column2,...)
VALUES
(value1,value2,...),
(value1,value2,...),
(value1,value2,...);
```

---

# 💡 Example 1

### Query

```sql
CREATE TABLE employees(
    emp_id INT PRIMARY KEY,
    emp_name VARCHAR(50),
    salary INT
);
```

### Explanation

Creates a new table named `employees` with three columns.

---

# 💡 Example 2

### Query

```sql
INSERT INTO employees(emp_id,emp_name,salary)
VALUES(1,'Rahul',50000);
```

### Output

```
1 row inserted successfully.
```

### Explanation

Inserts a single record into the `employees` table.

---

# 💡 Example 3

### Query

```sql
INSERT INTO employees(emp_id,emp_name,salary)
VALUES
(2,'Sneha',60000),
(3,'Aman',55000),
(4,'Priya',70000);
```

### Output

```
3 rows inserted successfully.
```

### Explanation

Multiple rows can be inserted using a single `INSERT INTO` statement.

---

# 📌 Important Notes

* Every table should have a Primary Key.
* Choose appropriate data types for each column.
* Column names should be meaningful.
* String values must be enclosed in single quotes (`' '`).
* Numeric values do not require quotes.
* Maintain the same order of columns and values.

---

# ⚠ Common Errors

## Error 1

### Wrong

```sql
INSERT students VALUES(1,'Rahul',50000);
```

### Correct

```sql
INSERT INTO students
VALUES(1,'Rahul',50000);
```

### Reason

The `INTO` keyword is required in standard SQL.

---

## Error 2

### Wrong

```sql
INSERT INTO students(id,name)
VALUES('One','Rahul');
```

### Correct

```sql
INSERT INTO students(id,name)
VALUES(1,'Rahul');
```

### Reason

The `id` column has an integer data type.

---

## Error 3

### Wrong

```sql
INSERT INTO students
VALUES(101,'Rahul');
```

### Correct

```sql
INSERT INTO students(id,name)
VALUES(101,'Rahul');
```

### Reason

Provide values for all columns or explicitly specify the target columns.

---

# 🌍 Real-World Applications

* Student Management Systems
* Banking Applications
* Hospital Records
* Employee Management
* Online Shopping Platforms
* Inventory Management Systems

---

# 🎤 Interview Questions

### Q1. What is a table in SQL?

**Answer:**

A table is a collection of related data organized into rows and columns.

---

### Q2. What is the purpose of the `PRIMARY KEY`?

**Answer:**

It uniquely identifies each record and prevents duplicate values.

---

### Q3. What is the difference between inserting one row and multiple rows?

**Answer:**

A single-row insert adds one record, whereas a multi-row insert adds several records in one SQL statement, improving efficiency.

---

### Q4. Can we insert data without mentioning column names?

**Answer:**

Yes, but only if values are provided in the exact order of the table's columns.

---

### Q5. Which SQL command is used to add new records?

**Answer:**

`INSERT INTO`

---

# 📚 Commands Covered

```sql
CREATE TABLE

PRIMARY KEY

VARCHAR

INT

INSERT INTO

VALUES

SELECT *
```

---

# ⚙ Execution Flow

```text
1. CREATE DATABASE
2. USE DATABASE
3. CREATE TABLE
4. INSERT RECORDS
5. SELECT DATA
```

---

# 🧠 Best Practices

* Always use meaningful table names.
* Define a Primary Key whenever possible.
* Use appropriate data types.
* Insert multiple records in one query for better performance.
* Keep SQL keywords in uppercase for readability.

---

# 📝 Practice Questions

1. Create a table named `courses`.
2. Add five records to the `courses` table.
3. Create an `employees` table with four columns.
4. Insert three employee records.
5. Display all records using `SELECT *`.

---

# 📖 Summary

* Learned how to create tables.
* Understood SQL data types.
* Used `PRIMARY KEY`.
* Inserted single and multiple records.
* Retrieved records using `SELECT`.
* Learned best practices for table creation and data insertion.

---

## ⏭ Next Topic

**Day 03:** SQL Data Types and Constraints
