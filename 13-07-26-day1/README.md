Here is a `README.md` file for your **Students Database**.

````md
# Students Database

## Overview
This project contains a sample **Students** table with student details such as department, city, marks, and attendance. It is useful for practicing SQL queries including filtering, sorting, grouping, aggregate functions, joins, subqueries, and window functions.

---

## Table Name
`Students`

---

## Table Structure

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| student_id | INT | Unique ID of the student (Primary Key) |
| student_name | VARCHAR(50) | Student Name |
| department | VARCHAR(20) | Department of the student |
| city | VARCHAR(30) | City of the student |
| marks | DECIMAL(5,2) | Marks obtained by the student |
| attendance | INT | Attendance percentage |

---

## Create Table

```sql
CREATE TABLE Students (
    student_id INT PRIMARY KEY,
    student_name VARCHAR(50),
    department VARCHAR(20),
    city VARCHAR(30),
    marks DECIMAL(5,2),
    attendance INT
);
```

---

## Insert Data

```sql
INSERT INTO Students
(student_id, student_name, department, city, marks, attendance)
VALUES
(101,'Rahul','CS','Hyderabad',178,95),
(102,'Anjali','IT','Bangalore',165,88),
(103,'Kiran','CS','Chennai',150,91),
(104,'Sneha','ECE','Hyderabad',140,82),
(105,'Arjun','MECH','Pune',120,78),
(106,'Priya','IT','Hyderabad',190,97),
(107,'Vikram','CS','Bangalore',NULL,84),
(108,'Neha','ECE','Chennai',155,89),
(109,'Rohit','MECH','Hyderabad',98,65),
(110,'Pooja','IT','Pune',175,92),
(111,'Suresh','CS','Chennai',162,87),
(112,'Deepa','ECE','Bangalore',145,90),
(113,'Ajay','MECH','Hyderabad',130,73),
(114,'Kavya','CS','Pune',185,96),
(115,'Manoj','IT','Chennai',170,94),
(116,'Divya','ECE','Hyderabad',NULL,80),
(117,'Nikhil','MECH','Bangalore',158,86),
(118,'Swathi','CS','Hyderabad',148,88),
(119,'Harsha','IT','Pune',110,72),
(120,'Keerthi','ECE','Chennai',182,99);
```

---

## Dataset Summary

- Total Records: **20**
- Departments: **CS, IT, ECE, MECH**
- Cities: **Hyderabad, Bangalore, Chennai, Pune**
- NULL Values:
  - Marks: 2 records
- Primary Key:
  - `student_id`

---

## Topics You Can Practice

- SELECT
- WHERE
- ORDER BY
- DISTINCT
- TOP / LIMIT
- Aggregate Functions
  - COUNT()
  - SUM()
  - AVG()
  - MAX()
  - MIN()
- GROUP BY
- HAVING
- CASE Statement
- IS NULL / IS NOT NULL
- LIKE
- BETWEEN
- IN / NOT IN
- Subqueries
- Common Table Expressions (CTE)
- Window Functions
  - ROW_NUMBER()
  - RANK()
  - DENSE_RANK()
  - NTILE()
- String Functions
- Date Functions (with custom datasets)

---

## Sample Queries

```sql
-- Display all students
SELECT * FROM Students;
```

```sql
-- Students from Hyderabad
SELECT * FROM Students
WHERE city = 'Hyderabad';
```

```sql
-- Average marks
SELECT AVG(marks) AS AverageMarks
FROM Students;
```

```sql
-- Department-wise average marks
SELECT department, AVG(marks) AS AvgMarks
FROM Students
GROUP BY department;
```

```sql
-- Students with attendance above 90
SELECT *
FROM Students
WHERE attendance > 90;
```

---

## Author
Hansika Manem
````
