# 📅 Day 04: WHERE Clause & Filtering Data

## 📖 Introduction

The `WHERE` clause is used to filter records from a table based on one or more conditions. Instead of retrieving every row, it allows you to fetch only the data that matches specific criteria. It is one of the most frequently used clauses in SQL and forms the basis of writing efficient queries.

---

# 🎯 Learning Objectives

After completing this topic, you will be able to:

* Filter records using the `WHERE` clause.
* Use comparison operators in SQL.
* Combine multiple conditions using logical operators.
* Apply filtering to retrieve meaningful data.
* Write efficient SQL queries.

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

## Basic WHERE Clause

```sql
SELECT column_name
FROM table_name
WHERE condition;
```

## Comparison Operators

| Operator | Description              |
| -------- | ------------------------ |
| =        | Equal to                 |
| != or <> | Not equal to             |
| >        | Greater than             |
| <        | Less than                |
| >=       | Greater than or equal to |
| <=       | Less than or equal to    |

---

# 💡 Example 1: Students from Pune

### Query

```sql
SELECT *
FROM students
WHERE city = 'Pune';
```

### Output

| ID  | Name    | City |
| --- | ------- | ---- |
| 101 | PRATHAM | Pune |
| 102 | Navin   | Pune |
| 106 | Rohit   | Pune |

### Explanation

Returns only those students whose city is **Pune**.

---

# 💡 Example 2: Students Scoring More Than 85

### Query

```sql
SELECT name, marks
FROM students
WHERE marks > 85;
```

### Output

| Name  | Marks |
| ----- | ----- |
| Navin | 90    |
| ADITI | 95    |
| GAURI | 88    |
| KIRTI | 92    |

### Explanation

Displays students whose marks are greater than **85**.

---

# 💡 Example 3: Students Age 21

### Query

```sql
SELECT name, age
FROM students
WHERE age = 21;
```

### Output

| Name    | Age |
| ------- | --- |
| PRATHAM | 21  |
| ADITI   | 21  |
| KIRTI   | 21  |

### Explanation

Only students with age **21** are displayed.

---

# 💡 Example 4: Using AND Operator

### Query

```sql
SELECT *
FROM students
WHERE city = 'Mumbai'
AND marks > 85;
```

### Output

| Name  | City   | Marks |
| ----- | ------ | ----- |
| ADITI | Mumbai | 95    |
| GAURI | Mumbai | 88    |

### Explanation

Both conditions must be true.

---

# 💡 Example 5: Using OR Operator

### Query

```sql
SELECT *
FROM students
WHERE city = 'Delhi'
OR city = 'Mumbai';
```

### Output

Students belonging to either **Delhi** or **Mumbai**.

### Explanation

At least one condition must be true.

---

# 💡 Example 6: Using NOT Operator

### Query

```sql
SELECT *
FROM students
WHERE NOT city = 'Pune';
```

### Output

Displays all students except those from Pune.

### Explanation

`NOT` reverses the condition.

---

# 📌 Important Notes

* `WHERE` filters rows based on conditions.
* String values should be enclosed in single quotes.
* Numeric values do not require quotes.
* Multiple conditions can be combined using `AND`, `OR`, and `NOT`.
* Filtering improves query efficiency by returning only the required data.

---

# ⚠ Common Errors

## Error 1

### Wrong

```sql
SELECT * FROM students
WHERE city = Pune;
```

### Correct

```sql
SELECT * FROM students
WHERE city = 'Pune';
```

### Reason

String values must be enclosed in single quotes.

---

## Error 2

### Wrong

```sql
SELECT *
WHERE marks > 80;
```

### Correct

```sql
SELECT *
FROM students
WHERE marks > 80;
```

### Reason

The `FROM` clause is mandatory.

---

## Error 3

### Wrong

```sql
SELECT *
FROM students
WHERE marks => 80;
```

### Correct

```sql
SELECT *
FROM students
WHERE marks >= 80;
```

### Reason

The correct comparison operator is `>=`.

---

# 🌍 Real-World Applications

* Find students with high marks.
* Display employees from a specific department.
* Retrieve customers from a particular city.
* Filter products by price range.
* Search hospital patients by age or disease.

---

# 🎤 Interview Questions

### Q1. What is the purpose of the `WHERE` clause?

**Answer:**

The `WHERE` clause filters records based on specified conditions.

---

### Q2. Which operators are commonly used with `WHERE`?

**Answer:**

`=`, `!=`, `<>`, `>`, `<`, `>=`, `<=`, `AND`, `OR`, and `NOT`.

---

### Q3. What is the difference between `AND` and `OR`?

**Answer:**

* `AND` returns rows only if all conditions are true.
* `OR` returns rows if at least one condition is true.

---

### Q4. Why are string values enclosed in single quotes?

**Answer:**

SQL treats text values as strings only when enclosed in single quotes.

---

### Q5. Can multiple conditions be used in a `WHERE` clause?

**Answer:**

Yes. Multiple conditions can be combined using logical operators such as `AND`, `OR`, and `NOT`.

---

# 📚 Commands Covered

```sql
WHERE

=

>

<

>=

<=

AND

OR

NOT
```

---

# ⚙ SQL Query Execution Order

```text
1. FROM
2. WHERE
3. SELECT
4. Display Result
```

---

# 🧠 Best Practices

* Retrieve only the required records.
* Use meaningful conditions.
* Prefer `AND` over multiple nested queries when applicable.
* Use proper indentation for readability.
* Avoid unnecessary filtering on large datasets without indexes.

---

# 📝 Practice Questions

1. Display students from Mumbai.
2. Display students whose marks are greater than 80.
3. Display students whose age is less than 22.
4. Display students from Pune with marks greater than 80.
5. Display students who are not from Delhi.
6. Display students from either Pune or Mumbai.

---

# 📖 Summary

* Learned the `WHERE` clause.
* Used comparison operators.
* Combined conditions using `AND`, `OR`, and `NOT`.
* Retrieved filtered records efficiently.
* Understood common mistakes and best practices.

---

## ⏭ Next Topic

**Day 05:** Modify Data from a Table
