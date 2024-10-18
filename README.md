# Employee and Department Management System
# Project Description
This project showcases the use of PL/SQL in Oracle for managing employees and departments within a company. It includes the creation of two main tables—employees and departments—as well as SQL queries to insert and retrieve data. Additionally, basic database operations such as table creation, data insertion, and querying are demonstrated. This project serves as a practical portfolio example for SQL and PL/SQL skills.

# Project Objectives
* Create tables for managing employees and departments.
* Insert, retrieve, and manipulate data using SQL queries.
* Show the use of SQL in a business context.
* Highlight basic database operations using Oracle PL/SQL.

# Technologies Used
* Oracle Database
* SQL and PL/SQL

# SQL Structure

Here is the SQL script to create the structure of the database used in this project:

```sql
-- Create Employees table
CREATE TABLE empleados (
    empleado_id INT PRIMARY KEY,
    nombre VARCHAR2(100),
    apellido VARCHAR2(100),
    fecha_contratacion DATE,
    salario NUMBER(10, 2)
);

-- Create Departments table
CREATE TABLE departamentos (
    departamento_id INT PRIMARY KEY,
    nombre VARCHAR2(100),
    ubicacion VARCHAR2(100)
);

-- Insert data into Employees
INSERT INTO empleados (empleado_id, nombre, apellido, fecha_contratacion, salario)
VALUES (1, 'Juan', 'Pérez', TO_DATE('2020-01-15', 'YYYY-MM-DD'), 2500.00);

-- Insert data into Departments
INSERT INTO departamentos(departamento_id, nombre, ubicacion)
VALUES (1, 'Recursos Humanos', 'Madrid');

-- Updating employee salary using the UPDATE statement
UPDATE empleados
SET salario = salario + 200
WHERE empleado_id = 1;

-- Deleting an employee using DELETE statement
DELETE FROM empleados
WHERE empleado_id = 3;

-- Grouping employees by department and calculating average salary using GROUP BY
SELECT d.nombre AS departamento, AVG(e.salario) AS salario_promedio
FROM empleados e
JOIN departamentos d ON e.departamento_id = d.departamento_id
GROUP BY d.nombre;

-- Using SET to update multiple columns in one statement
UPDATE empleados
SET nombre = 'Ana María', salario = 3200
WHERE empleado_id = 2;

-- Retrieve data with a WHERE clause
SELECT * FROM empleados
WHERE salario > 2500;

-- Use ORDER BY to sort data
SELECT * FROM empleados
ORDER BY fecha_contratacion DESC;

-- Use a JOIN to combine data from two tables
SELECT e.nombre, e.apellido, d.nombre AS departamento
FROM empleados e
JOIN departamentos d ON e.departamento_id = d.departamento_id;
```

# Conclusion:
This project aims to demonstrate basic SQL functionality such as CREATE TABLE, as well as data manipulation (INSERT, UPDATE, DELETE), data retrieval with filtering and sorting (WHERE, ORDER BY) and more complex queries that combine data from multiple tables (JOIN, GROUP BY). It highlights how SQL can be used for effective data management in a relational database system such as Oracle.




