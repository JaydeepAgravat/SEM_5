# MYSQL DDL command

- The main four DDL commands in MySQL are:

1. CREATE
2. ALTER
3. DROP
4. TRUNCATE

## DATABASE

### CREATE & DROP

```mysql
-- 1. CREATE DATABASE
CREATE DATABASE IF NOT EXISTS db;

-- 2. DROP DATABASE
DROP DATABASE IF EXISTS db;
```

## TABLE

### CREATE, TRUNCATE & DROP

```mysql
CREATE TABLE employees (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(50) UNIQUE,
  hire_date DATE DEFAULT '2022-01-01',
  salary DECIMAL(10,2) CHECK (salary >= 0),
  department_id INT,
  CONSTRAINT name_email_unique UNIQUE (name, email),
  FOREIGN KEY (department_id) REFERENCES department(id),
  ON DELETE SET NULL
  ON UPDATE CASCADE
);

INSERT INTO employees (id, name, email, hire_date, salary, department_id)
VALUES 
  (1, 'John Doe', 'jdoe@example.com', '2022-01-01', 50000, 1),
  (2, 'Jane Smith', 'jsmith@example.com', '2022-02-15', 60000, 2),
  (3, 'Bob Johnson', 'bjohnson@example.com', '2022-03-01', 55000, 1),
  (4, 'Sarah Williams', 'swilliams@example.com', '2022-04-01', 65000, 2),
  (5, 'Mike Davis', 'mdavis@example.com', '2022-05-15', 70000, 1);

-- 2. TRUNCATE TABLE
TRUNCATE TABLE employees

-- 3. DROP TABLE
DROP TABLE employees
```

### ALTER

```mysql
-- 4. ALTER TABLE 

-- Add two new column to an existing table:
ALTER TABLE table_name
ADD column_name data_type AFTER|BEFORE other_column_name,
ADD column_name data_type AFTER|BEFORE other_column_name;

-- Drop an existing column from a table:
ALTER TABLE table_name
DROP column_name;

-- Rename an existing column in a table:
ALTER TABLE table_name
CHANGE old_column_name new_column_name data_type;

-- Modify a datatype on column in a table:
ALTER TABLE table_name
MODIFY COLUMN column_name new_data_type;

-- Add Constraint
ALTER TABLE table_name
ADD CONSTRAINT name_of_constraint CHECK (column_name > 18)

-- Delete Constraint
ALTER TABLE table_name
DROP CONSTRAINT name_of_constraint

-- Add a primary key to a table:
ALTER TABLE table_name
ADD PRIMARY KEY (column_name);

-- Add a foreign key to a table:
ALTER TABLE table_name
ADD FOREIGN KEY (column_name)
REFERENCES referenced_table_name(referenced_column_name);

-- Drop a primary key or foreign key constraint from a table:
ALTER TABLE table_name
DROP PRIMARY KEY;

ALTER TABLE table_name
DROP FOREIGN KEY foreign_key_name;
```
