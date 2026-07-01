# 📅 Day X: DELETE and DROP Statement

## 📖 Introduction

SQL provides different commands to remove data and database objects. The `DELETE` statement removes records from a table, whereas the `DROP` statement permanently removes an entire database object such as a table or database.

Understanding the difference between these commands is essential because `DELETE` removes only data, while `DROP` removes both the data and the table structure.

---

# 🎯 Learning Objectives

After completing this topic, you will be able to:

* Delete specific records from a table.
* Delete all records from a table.
* Drop a table.
* Drop a database.
* Understand the differences between DELETE and DROP.

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
INSERT INTO students
VALUES
(101,'PRATHAM',21,'Pune','BCA',85),
(102,'Navin',22,'Pune','BCA',90),
(103,'ADITI',21,'Mumbai','BTech',95),
(104,'Amit',23,'Delhi','BCA',70),
(105,'GAURI',22,'Mumbai','BCom',88);
```

---

# 📝 Syntax

## DELETE Specific Records

```sql
DELETE FROM table_name
WHERE condition;
```

## DELETE All Records

```sql
DELETE FROM table_name;
```

## DROP TABLE

```sql
DROP TABLE table_name;
```

## DROP DATABASE

```sql
DROP DATABASE database_name;
```

---

# 💡 Example 1: Delete One Record

### Query

```sql
DELETE FROM students
WHERE id = 105;
```

### Explanation

Deletes only the record whose `id` is **105**.

---

# 💡 Example 2: Delete Multiple Records

### Query

```sql
DELETE FROM students
WHERE city = 'Pune';
```

### Explanation

Deletes all students who belong to Pune.

---

# 💡 Example 3: Delete All Records

### Query

```sql
DELETE FROM students;
```

### Explanation

Deletes every record from the table but keeps the table structure.

---

# 💡 Example 4: Drop Table

### Query

```sql
DROP TABLE students;
```

### Explanation

Deletes the entire `students` table including its structure and all stored data.

---

# 💡 Example 5: Drop Database

### Query

```sql
DROP DATABASE student_db;
```

### Explanation

Deletes the complete database permanently.

---

# 📌 Difference Between DELETE and DROP

| DELETE                   | DROP                                 |
| ------------------------ | ------------------------------------ |
| Removes records only     | Removes the entire table or database |
| Table structure remains  | Table structure is deleted           |
| Can use WHERE clause     | WHERE clause is not allowed          |
| Can delete selected rows | Deletes everything                   |
| DML Command              | DDL Command                          |

---

# 📌 Important Notes

* Always use `WHERE` with `DELETE` unless you intend to remove all records.
* `DELETE` keeps the table structure.
* `DROP` permanently removes the table or database.
* `DROP` cannot be rolled back in many database systems once committed.
* Be careful while executing `DROP` commands.

---

# ⚠ Common Errors

## Error 1

### Wrong

```sql
DELETE students
WHERE id = 1;
```

### Correct

```sql
DELETE FROM students
WHERE id = 1;
```

### Reason

The `FROM` keyword is mandatory.

---

## Error 2

### Wrong

```sql
DROP students;
```

### Correct

```sql
DROP TABLE students;
```

### Reason

The object type (`TABLE`) must be specified.

---

## Error 3

### Wrong

```sql
DELETE FROM students;
```

*(When only one record should be deleted.)*

### Correct

```sql
DELETE FROM students
WHERE id = 101;
```

### Reason

Without a `WHERE` clause, every record is deleted.

---

# 🌍 Real-World Applications

* Remove inactive users.
* Delete cancelled orders.
* Delete old log records.
* Remove temporary tables.
* Delete test databases after development.

---

# 🎤 Interview Questions

### Q1. What is the difference between DELETE and DROP?

**Answer:**

`DELETE` removes records from a table while keeping the table structure. `DROP` removes the entire table or database, including its structure and data.

---

### Q2. Can DELETE be used without a WHERE clause?

**Answer:**

Yes. It deletes all rows from the table but leaves the table structure intact.

---

### Q3. Can DROP remove only one row?

**Answer:**

No. `DROP` removes the complete table or database.

---

### Q4. Which command is faster: DELETE or DROP?

**Answer:**

`DROP` is generally faster because it removes the entire object instead of deleting rows one by one.

---

### Q5. Which command supports the WHERE clause?

**Answer:**

Only the `DELETE` statement supports the `WHERE` clause.

---

# 📚 Commands Covered

```sql
DELETE

DROP TABLE

DROP DATABASE

WHERE
```

---

# ⚙ SQL Execution Order

```text
1. Identify Table
2. Apply WHERE Condition (DELETE only)
3. Delete Rows OR Drop Object
4. Commit Changes
```

---

# 🧠 Best Practices

* Always verify your `WHERE` condition before running `DELETE`.
* Take a backup before using `DROP`.
* Use `DELETE` when you need to preserve the table structure.
* Use `DROP` only when the table or database is no longer needed.

---

# 📝 Practice Questions

1. Delete the student whose ID is `104`.
2. Delete all students from `Mumbai`.
3. Delete every record from the `students` table.
4. Drop the `students` table.
5. Drop the `student_db` database.

---

# 📖 Summary

* Learned the `DELETE` statement.
* Deleted single and multiple records.
* Deleted all records from a table.
* Learned the `DROP TABLE` statement.
* Learned the `DROP DATABASE` statement.
* Understood the difference between `DELETE` and `DROP`.

---

## ⏭ Next Topic

**Day X+1:** NOT NULL
