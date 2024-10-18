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

# Database Structure

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
```sql


