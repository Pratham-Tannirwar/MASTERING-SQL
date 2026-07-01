# 📅 Day 03: SELECT Statement & Data Retrieval

## 📖 Introduction

The `SELECT` statement is one of the most important SQL commands. It is used to retrieve data from one or more tables in a database. Whether you need all records, specific columns, or filtered data, the `SELECT` statement is the starting point for almost every SQL query.

---

# 🎯 Learning Objectives

After completing this topic, you will be able to:

* Retrieve all records from a table.
* Retrieve specific columns.
* Rename columns using aliases.
* Perform simple calculations using `SELECT`.
* Understand the basic syntax of data retrieval.

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

# 📊 View Complete Table

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

## Select All Columns

```sql
SELECT * FROM table_name;
```

## Select Specific Columns

```sql
SELECT column1, column2
FROM table_name;
```

## Select with Alias

```sql
SELECT column_name AS alias_name
FROM table_name;
```

---

# 💡 Example 1: Retrieve All Data

### Query

```sql
SELECT * FROM students;
```

### Explanation

Returns every row and every column from the `students` table.

---

# 💡 Example 2: Retrieve Specific Columns

### Query

```sql
SELECT name, city
FROM students;
```

### Output

| Name    | City   |
| ------- | ------ |
| PRATHAM | Pune   |
| Navin   | Pune   |
| ADITI   | Mumbai |
| Amit    | Delhi  |
| GAURI   | Mumbai |
| Rohit   | Pune   |
| KIRTI   | Delhi  |
| Neha    | Mumbai |

### Explanation

Only the `name` and `city` columns are displayed.

---

# 💡 Example 3: Use Column Alias

### Query

```sql
SELECT
name AS Student_Name,
marks AS Score
FROM students;
```

### Output

| Student_Name | Score |
| ------------ | ----- |
| PRATHAM      | 85    |
| Navin        | 90    |
| ADITI        | 95    |
| Amit         | 70    |
| GAURI        | 88    |
| Rohit        | 76    |
| KIRTI        | 92    |
| Neha         | 80    |

### Explanation

`AS` assigns a temporary name to a column for the query result.

---

# 💡 Example 4: Arithmetic Operations

### Query

```sql
SELECT
name,
marks,
marks + 5 AS Updated_Marks
FROM students;
```

### Output

| Name    | Marks | Updated_Marks |
| ------- | ----- | ------------- |
| PRATHAM | 85    | 90            |
| Navin   | 90    | 95            |
| ADITI   | 95    | 100           |
| Amit    | 70    | 75            |
| GAURI   | 88    | 93            |
| Rohit   | 76    | 81            |
| KIRTI   | 92    | 97            |
| Neha    | 80    | 85            |

### Explanation

SQL can perform arithmetic operations directly in the `SELECT` statement.

---

# 📌 Important Notes

* `SELECT` retrieves data from a table.
* `*` selects all columns.
* Specify column names to retrieve only required data.
* Use `AS` to create temporary column names.
* SQL keywords are case-insensitive.

---

# ⚠ Common Errors

## Error 1

### Wrong

```sql
SELECT FROM students;
```

### Correct

```sql
SELECT * FROM students;
```

### Reason

At least one column or `*` must be specified.

---

## Error 2

### Wrong

```sql
SELECT names FROM students;
```

### Correct

```sql
SELECT name FROM students;
```

### Reason

The column name must exactly match the table definition.

---

## Error 3

### Wrong

```sql
SELECT * students;
```

### Correct

```sql
SELECT * FROM students;
```

### Reason

The `FROM` keyword is mandatory.

---

# 🌍 Real-World Applications

* Student information systems
* Banking applications
* Hospital databases
* Employee management systems
* E-commerce websites
* Data analysis and reporting

---

# 🎤 Interview Questions

### Q1. What is the purpose of the `SELECT` statement?

**Answer:**

It retrieves data from one or more tables in a database.

---

### Q2. What does `SELECT *` mean?

**Answer:**

It retrieves all columns from the specified table.

---

### Q3. What is a column alias?

**Answer:**

A temporary name given to a column using the `AS` keyword.

---

### Q4. Can SQL perform calculations inside `SELECT`?

**Answer:**

Yes. SQL supports arithmetic operations such as `+`, `-`, `*`, and `/` within the `SELECT` statement.

---

### Q5. Is `AS` mandatory while giving aliases?

**Answer:**

No. The `AS` keyword is optional in most SQL databases, but using it improves readability.

---

# 📚 Commands Covered

```sql
SELECT

FROM

*

AS
```

---

# ⚙ SQL Query Execution Order

```text
1. FROM
2. SELECT
3. Display Result
```

---

# 🧠 Best Practices

* Retrieve only the columns you need instead of using `SELECT *`.
* Use meaningful aliases for better readability.
* Keep SQL keywords in uppercase.
* Write queries with proper indentation.
* Avoid unnecessary data retrieval to improve performance.

---

# 📝 Practice Questions

1. Display all records from the `students` table.
2. Display only the `name` and `course` columns.
3. Rename the `marks` column as `Score`.
4. Display student names and marks increased by 10.
5. Display only the `city` column.

---

# 📖 Summary

* Learned the `SELECT` statement.
* Retrieved all records using `SELECT *`.
* Retrieved specific columns.
* Used column aliases with `AS`.
* Performed arithmetic operations in `SELECT`.
* Understood best practices for data retrieval.

---

## ⏭ Next Topic

**Day 04:** WHERE Clause & Filtering Data
