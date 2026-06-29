# 📅 Day X: SQL Fundamentals

> **Topic:** Fundamentals
> **Difficulty:** 🟢 Beginner
> **Prerequisites:** None

---

# 📖 Introduction

Briefly explain what this topic is, why it is important, and where it is used in real-world database applications.

Example:

> SQL (Structured Query Language) is the standard language used to communicate with relational databases. Before learning advanced queries, it is essential to understand the fundamentals of databases, tables, rows, columns, and SQL syntax.

---

# 🎯 Learning Objectives

After completing this topic, you will be able to:

* Understand the concept of databases.
* Differentiate between DBMS and RDBMS.
* Create a database.
* Create tables.
* Insert records.
* Retrieve stored data.
* Understand basic SQL syntax.

---

# 🛠 Database Setup

## Create Database

```sql
CREATE DATABASE student_db;
```

---

## Select Database

```sql
USE student_db;
```

---

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

## Insert Sample Data

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

# 📊 View Table

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

```sql
SQL Command

SELECT column_name
FROM table_name
WHERE condition;
```

### Syntax Breakdown

* **SELECT** → Specifies the columns to retrieve.
* **FROM** → Specifies the table.
* **WHERE** → Filters rows based on a condition.

---

# 💡 Example 1

### Problem

Display all students.

### Query

```sql
SELECT * FROM students;
```

### Output

Complete student table.

### Explanation

`*` selects all columns from the table.

---

# 💡 Example 2

### Problem

Display only student names.

### Query

```sql
SELECT name
FROM students;
```

### Output

```
PRATHAM
Navin
ADITI
Amit
...
```

### Explanation

Only the `name` column is displayed.

---

# 💡 Example 3

### Problem

Display names and marks.

### Query

```sql
SELECT name, marks
FROM students;
```

### Output

```
PRATHAM 85
Navin   90
ADITI   95
...
```

### Explanation

Multiple columns can be selected by separating them with commas.

---

# 📌 Key Concepts

* Database stores related information.
* Table stores records.
* Row represents one record.
* Column represents one attribute.
* SQL is not case-sensitive.
* Every SQL statement ends with a semicolon (`;`).

---

# ⚠ Common Errors

## Error 1

### Wrong

```sql
SELEC * FROM students;
```

### Correct

```sql
SELECT * FROM students;
```

### Reason

`SELECT` keyword is misspelled.

---

## Error 2

### Wrong

```sql
SELECT FROM students;
```

### Correct

```sql
SELECT *
FROM students;
```

### Reason

At least one column or `*` must be specified.

---

## Error 3

### Wrong

```sql
USE studentdb;
```

### Correct

```sql
USE student_db;
```

### Reason

Database name must match exactly.

---

# 💼 Real-World Applications

* Student Management System
* Banking System
* Hospital Database
* E-commerce Applications
* Inventory Management
* Employee Management System

---

# 🎤 Interview Questions

### Q1. What is SQL?

**Answer:**

SQL (Structured Query Language) is the standard language used to create, manipulate, and retrieve data from relational databases.

---

### Q2. What is the difference between DBMS and RDBMS?

**Answer:**

DBMS stores data without relationships, whereas RDBMS stores related data using tables and supports relationships using keys.

---

### Q3. What is a table?

**Answer:**

A table is a collection of rows and columns used to organize data inside a database.

---

### Q4. Is SQL case-sensitive?

**Answer:**

SQL keywords are generally not case-sensitive, but string values can be depending on the database collation.

---

### Q5. Why is a Primary Key important?

**Answer:**

A Primary Key uniquely identifies each row and prevents duplicate records.

---

# 🛠 Commands Covered

```sql
CREATE DATABASE

USE

CREATE TABLE

INSERT INTO

VALUES

SELECT

FROM
```

---

# ⚙ SQL Query Execution Flow

```
Write Query
      ↓
SQL Parser
      ↓
Optimizer
      ↓
Execution Engine
      ↓
Retrieve Data
      ↓
Display Result
```

---

# 🧠 Best Practices

* Use meaningful table names.
* Use meaningful column names.
* Always define a Primary Key.
* Write SQL keywords in uppercase.
* End every statement with a semicolon.
* Keep your queries readable using indentation.

---

# 📚 Practice Questions

1. Create a database named `college_db`.
2. Create a table named `employees`.
3. Insert five employee records.
4. Display all employee details.
5. Display only employee names.
6. Display employee names and salaries.

---

# 📖 Summary

✅ Learned about SQL Fundamentals

✅ Created a database

✅ Created a table

✅ Inserted records

✅ Retrieved data using SELECT

✅ Understood SQL syntax

✅ Practiced basic SQL queries

---

## ⏭ Next Topic

**Day X+1:** SQL Syntax & Data Types
