# Database Management System

## Database

- A Database is a shared collection of logically related data and description of these data, designed to meet the information needs of an organization.

- Data Storage: A database is used to store large amounts of structured data,
making it easily accessible, searchable, and retrievable.
- Data Analysis: A database can be used to perform complex data analysis,
generate reports, and provide insights into the data.
- Record Keeping: A database is often used to keep track of important records,
such as financial transactions, customer information, and inventory levels.
- Web Applications: Databases are an essential component of many web
applications, providing dynamic content and user management.

### Properties of an Ideal Database

1. Integrity
2. Availability
3. Security
4. Independent of Application
5. Concurrency

### Types of Databases

1. Relational Databases

    - Also known as SQL databases, these databases use a relational model to
    organize data into tables with rows and columns.

2. NoSQL Databases

    - These databases are designed to handle large amounts of unstructured or semi-structured data, such as documents, images, or videos. (MongoDB)

3. Column Databases

    - These databases store data in columns rather than rows, making them well-suited for data warehousing and analytical applications. (Amazon Redshift,Google BigQuery)

4. Graph Databases

    - These databases are used to store and query graph-structured data, such as social network connections or systems. (Neo4j, Amazon Neptune)

5. Key-value databases

    - These databases store data as a collection of keys and values, making them well-suited for caching and simple data storage needs (Redis and Amazon DynamoDB)

### Relational Databases

- Also known as SQL databases, these databases use a relational model to organize data into tables with rows and columns.

- table/relation
- rows/records/tuples
- columns/fields/attributes
- cardinality of the relation/number of rows
- degree of the relation/number of attributes
- null
- domain

### DBMS

- A database management system (DBMS) is a software system that provides the
interfaces and tools needed to store, organize, and manage data in a database.
- A DBMS acts as an intermediary between the database and the applications or users
that access the data stored in the database.
- users -> application -> dbms -> database -> os -> hardware

### Function of DBMS

1. Data Management - Store, retrieve and modify data
2. Integrity - Maintain accuracy of data
3. Concurrency - Simultaneous data access for multiple users
4. Transaction - Modification to database must either be successful or
must not happen at all
5. Security - Access to authorized users only
6. Utilities - Data import/export, user management, backup, logging

### Database Keys

- A key in a database is an attribute or a set of attributes that uniquely identifies a tuple (row) in a table. Keys play a crucial role in ensuring the integrity and reliability of a database by enforcing unique constraints on the data and establishing relationships between tables.

1. Super Key
    - A Super key is a combination of columns that uniquely identifies any row within a relational database management system (RDBMS) table
2. Candidate key
    - A candidate key is a minimal Super key, meaning it has no redundant attributes.
    - In other words, it's the smallest set of attributes that can be used to
    uniquely identify a tuple (row) in the table
3. Primary Key
    - A primary key is a unique identifier for each tuple in a table. There can only be one primary key in a table, and it cannot contain null values.
4. Alternate Key
    - An alternate key is a candidate key that is not used as the primary key.
5. Composite Key
    - A composite key is a primary key that is made up of two or more attributes.
    - Composite keys are used when a single attribute is not sufficient to uniquely identify a tuple in a table.
6. Surrogate Key

7. Foreign Key
    - A foreign key is a set of attributes in a table that refers to the primary key of another table. The foreign key links these two tables.

### Cardinality of Relationships

- Cardinality in database relationships refers to the number of occurrences of an entity in a relationship with another entity. Cardinality defines the number of instances of one entity that can be associated with a single instance of the related entity.

- 1:1, 1:N, M:N

Examples:

1. Person -> Driving License Number
2. Student -> college branch
3. Restaurants -> orders
4. Restaurants -> menu
5. Students -> courses

### Drawbacks of Database

1. Complexity: Setting up and maintaining a database can be complex and time- consuming, especially for large and complex systems.
2. Cost: The cost of setting up and maintaining a database, including hardware, software, and personnel, can be high.
3. Scalability: As the amount of data stored in a database grows, it can become more difficult to manage, leading to performance and scalability issues.
4. Data Integrity: Ensuring the accuracy and consistency of data stored in a database can be a challenge, especially when multiple users are updating the data simultaneously.
5. Security: Securing a database from unauthorized access and protecting sensitive information can be difficult, especially with the increasing threat of cyber attacks.
6. Data Migration: Moving data from one database to another or upgrading to a new database can be a complex and time-consuming process.
7. Flexibility: The structure of a database is often rigid and inflexible, making it difficult to adapt to changing requirements or to accommodate new types of data.

## Data integrity

- Data integrity in databases refers to the accuracy, completeness, and consistency
of the data stored in a database.
- It is a measure of the reliability and
trustworthiness of the data and ensures that the data in a database is protected
from errors, corruption, or unauthorized changes.
- There are various methods used to ensure data integrity, including:

1. Constraints

    - Constraints in databases are rules or conditions that must be met for data to be
    inserted, updated, or deleted in a database table.
    - They are used to enforce the
    integrity of the data stored in a database and to prevent data from becoming
    inconsistent or corrupted.

2. Transactions

    - A sequence of database operations that are treated as a single unit
    of work.

3. Normalization
    - A design technique that minimizes data redundancy and ensures data consistency by organizing data into separate tables.

## Constraints in MySQL

- Constraints in databases are rules or conditions that must be met for data to be
inserted, updated, or deleted in a database table.
- They are used to enforce the
integrity of the data stored in a database and to prevent data from becoming inconsistent or corrupted.

1. NOT NULL
2. UNIQUE
3. PRIMARY KEY
4. AUTO INCREMENT
5. CHECK
6. DEFAULT
7. FOREIGN KEY

Referential Actions :

1. RESTRICT
2. CASCADE
3. SET NULL
4. SET DEFAULT

## SQL

- SQL (Structured Query Language) is a programming language used for managing
and manipulating data in relational databases.
- It allows you to insert, update,
retrieve, and delete data in a database.
- It is widely used for data management in
many applications, websites, and businesses. In simple terms, SQL is used to
communicate with and control databases.

## Types of SQL commands

1. DDL | Data Definition Language
    1. CREATE
    2. ALTER
    3. DROP
    4. TRUNCATE
    5. RENAME
2. DML | Data Manipulation Language
    1. INSERT
    2. UPDATE
    3. DELETE
3. DQL | Data Query Language
    1. SELECT
4. DCL | Data Control Language
    1. GRANT
    2. REVOKE
5. TCL | Transaction Control Language
    1. COMMIT
    2. ROLLBACK
    3. SAVEPOINT

## DDL

### DDL commands for Databases

1. CREATE
2. DROP

```sql
-- 1. CREATE DATABASE
CREATE DATABASE IF NOT EXISTS db;

-- 2. DROP DATABASE
DROP DATABASE IF EXISTS db;
```

### DDL commands for Tables

1. CREATE
2. TRUNCATE
3. DROP
4. ALTER
5. RENAME

```sql
-- 1. CREATE TABLE
CREATE TABLE department(
    department_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL
)

CREATE TABLE employee(
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(50) UNIQUE,
    hire_date DATE DEFAULT '2002-11-12',
    salary DECIMAL(10,2) CHECK (salary >= 0),
    department_id INT,
    
    CONSTRAINT name_salary_unique UNIQUE(name, salary),
    FOREIGN KEY (department_id) REFERENCES department (department_id)
    ON DELETE RESTRICT
    ON UPDATE CASCADE
)

INSERT INTO department (department_id, name) VALUES
(1, 'it'),
(2, 'hr');

INSERT INTO employee (id, name, email, hire_date, salary, department_id)
VALUES 
  (1, 'John Doe', 'jdoe@example.com', '2022-01-01', 50000, 1),
  (2, 'Jane Smith', 'jsmith@example.com', '2022-02-15', 60000, 2),
  (3, 'Bob Johnson', 'bjohnson@example.com', '2022-03-01', 55000, 1),
  (4, 'Sarah Williams', 'swilliams@example.com', '2022-04-01', 65000, 2),
  (5, 'Mike Davis', 'mdavis@example.com', '2022-05-15', 70000, 1);

-- 2. TRUNCATE TABLE
TRUNCATE TABLE employee

-- 3. DROP TABLE
DROP TABLE employee
```

### ALTER TABLE command

- The "ALTER TABLE" statement in SQL is used to modify the structure of an existing table.
- Some of the things that can be done using the ALTER TABLE statement include

1. Add columns
2. Delete columns
3. Modify columns
4. Add Constraints
5. Delete Constraints

```sql
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

```sql
-- 5. RENAME TABLE
RENAME TABLE old_name To new_name;
```

## DML

- The main three DML (Data Manipulation Language) commands in MySQL are:

1. INSERT
2. UPDATE
3. DELETE

### 1. INSERT

```sql
CREATE TABLE department(
    department_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(50) NOT NULL
)

CREATE TABLE employee(
    id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(50) NOT NULL,
    email VARCHAR(50) UNIQUE,
    hire_date DATE DEFAULT '2002-11-12',
    salary DECIMAL(10,2) CHECK (salary >= 0),
    department_id INT,
    
    CONSTRAINT name_salary_unique UNIQUE(name, salary),
    FOREIGN KEY (department_id) REFERENCES department (department_id)
    ON DELETE RESTRICT
    ON UPDATE CASCADE
)

INSERT INTO department (department_id, name) VALUES
(1, 'it'),
(2, 'hr');

INSERT INTO employee (id, name, email, hire_date, salary, department_id)
VALUES 
  (1, 'John Doe', 'jdoe@example.com', '2022-01-01', 50000, 1),
  (2, 'Jane Smith', 'jsmith@example.com', '2022-02-15', 60000, 2),
  (3, 'Bob Johnson', 'bjohnson@example.com', '2022-03-01', 55000, 1),
  (4, 'Sarah Williams', 'swilliams@example.com', '2022-04-01', 65000, 2),
  (5, 'Mike Davis', 'mdavis@example.com', '2022-05-15', 70000, 1);
```

### 2. UPDATE

```SQL
UPDATE TB
SET c1 = 'JAVA', c2 = 'second'
WHERE c1 = 'C' AND c1 = 'C++;
```

### 3. DELETE

```SQL
DELETE FROM TB
WHERE c1 = 'C' AND c1 = 'C++;
```

## MYSQL FUNCTION

### BUILT-IN FUNCTION

```SQL
SELECT ABS(c1) FROM TB;
SELECT COUNT(c1) FROM TB;
```

#### Scalar function

- ABS()
- ROUND()
- CEIL()
- FLOOR()

#### Aggregate function

- MAX()
- MIN()
- SUM()
- AVG()
- COUNT()
- STD()
- VARIANCE()

## DQL

### SELECT

```sql
    SELECT * FROM TB LIMIT 10;

    SELECT c1,c2 FROM TB;

    SELECT DISTINCT(c1) FROM TB;

    SELECT DISTINCT c1,c2 FROM TB;

    SELECT c1 FROM TB
    WHERE c2 IN ('APPLE','NOKIA');

    SELECT c1 FROM TB
    WHERE c2 NOT IN ('APPLE','NOKIA');

    SELECT c1 FROM TB
    WHERE c2 BETWEEN 10 AND 20;

    SELECT c1,SQRT(c2),rating/10 AS star FROM TB;

    SELECT c1, 'value' As new_tmp_col FROM TB;
```

### ORDER BY

```sql
    SELECT model,screen_size FROM db.phones
    WHERE brand_name = 'samsung'
    ORDER BY screen_size DESC
    LIMIT 3 ;

    SELECT model, num_front_cameras + num_rear_cameras as 'Total' FROM db.phones
    ORDER BY Total DESC
    LIMIT 3;

    SELECT model, battery_capacity FROM db.phones
    ORDER BY battery_capacity DESC
    LIMIT 1,1;

    SELECT model,rating FROM db.phones
    WHERE brand_name = 'apple'
    ORDER BY rating ASC
    LIMIT 3;

    SELECT brand_name, price FROM db.phones
    ORDER BY brand_name ASC, price DESC; 
```

### GROUP BY

```sql
    SELECT brand_name, COUNT(*) AS 'no_phones',
    ROUND(AVG(price)) AS 'avg price',
    MAX(rating) AS 'max rating',
    ROUND(AVG(screen_size), 2) AS 'screen size',
    ROUND(AVG(battery_capacity)) AS 'avg battery capacity'
    FROM db.phones
    GROUP BY brand_name
    ORDER BY no_phones DESC;

    SELECT has_5g,
    ROUND(AVG(price)) AS 'avg price',
    ROUND(AVG(rating)) AS 'avg rating'
    FROM db.phones
    GROUP BY has_5g

    SELECT brand_name,
    processor_brand,
    COUNT(*) AS 'no_phones',
    ROUND(AVG(primary_camera_rear)) AS 'res'
    FROM db.phones
    WHERE brand_name = 'samsung'
    GROUP BY brand_name, processor_brand

    SELECT brand_name, 
    ROUND(AVG(price)) AS 'avg_price'
    FROM db.phones
    GROUP BY brand_name
    ORDER BY avg_price DESC LIMIT 3

    SELECT brand_name, COUNT(*) AS 'no_phones'
    FROM db.phones
    WHERE has_nfc = 'True' AND has_ir_blaster = 'True'
    GROUP BY brand_name
    ORDER BY no_phones DESC LIMIT 3

    SELECT has_5g,
    ROUND(AVG(price)) AS 'avg_price'
    FROM db.phones
    WHERE brand_name = 'samsung'
    GROUP BY has_5g;
```

### HAVING

```sql
    SELECT brand_name, 
    COUNT(*) AS 'count', 
    ROUND(AVG(rating)) AS 'avg_rating'
    FROM db.phones
    GROUP BY brand_name
    HAVING count > 80
    ORDER BY avg_rating DESC

    SELECT brand_name, 
    round((ram_capacity)) AS 'avg_ram'
    FROM db.phones
    WHERE refresh_rate > 90 AND fast_charging_available = 1
    GROUP BY brand_name
    HAVING COUNT(*) > 10
    ORDER BY avg_ram DESC LIMIT 3;

    SELECT brand_name,
    COUNT(*) AS 'num_phones',
    AVG(price) AS 'avg_price',
    AVG(rating) AS 'avg_rating'
    FROM db.phones
    WHERE has_5g = 'True'
    GROUP BY brand_name
    having avg_rating > 70 AND num_phones > 10
    ORDER BY avg_price DESC;
```

## JOIN

### 1. CROSS JOIN

```sql
SELECT * FROM T1
CROSS JOIN T2;
```

### 2. INNER JOIN

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id;
```

### 3. LEFT JOIN

```sql
SELECT * FROM T1
LEFT JOIN T2
ON T1.id = T2.id;
```

### 4. RIGHT JOIN

```sql
SELECT * FROM T1
RIGHT JOIN T2
ON T1.id = T2.id;
```

### 5. FULL OUTER JOIN

```sql
SELECT * FROM T1
LEFT JOIN T2
ON T1.id = T2.id

UNION

SELECT * FROM T1
RIGHT JOIN T2
ON T1.id = T2.id;
```

### 6. SELF JOIN

```sql
SELECT * FROM T1
INNER JOIN SELECT * FROM T1
ON T1.ID = T1.EID;
```

### SQL SET OPRERATIONS

```sql
SELECT * FROM T1
UNION
SELECT * FROM T2;
```

1. UNION
2. UNION ALL
3. INTERSECT
4. EXCEPT

### Joining on more than one column

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id AND T1.eyr = T2.cyr;
```

### Joining more than 2 tables

```sql
SELECT * FROM T1
INNER JOIN T2
ON T1.id = T2.id
INNER JOIN T3
ON T2.uid = T3.uid;
```

## SUBQUERY

### Types of SUBQUERY

1. Based on Result
    1. Scalar
    2. Row
    3. Table
2. Based on Working
    1. Independent
    2. Correlated

### Where Subquery Place

1. INSERT
2. UPDATE
3. DELETE
4. SELECT
    1. WHERE
    2. SELECT
    3. FROM
    4. HAVING

### SCALAR SUBQUERY

```sql
SELECT * FROM T1
WHERE C1 = (SELECT MAX(C1) FROM T1);
```

### ROW SUBQUERY

```sql
SELECT * FROM T1
WHERE C1 IN (SELECT C1 FROM T1
                WHERE C2 > AVG(C2));
```

### TABLE SUBQUERY

```sql
SELECT * FROM T1
WHERE (C1,C2) IN (SELECT C1,MAX(C2) 
                    FROM T1
                    GROUP BY C1);
```

### USAGE WITH WHERE

```sql
SELECT * FROM T1 M1
WHERE C1 > (SELECT AVG(C1) FROM T1 M2 WHERE M1.C2 = M1.C2)
```

### USAGE WITH SELECT

```sql
SELECT C1,C2,C3, 
(SELECT AVG(C3) FROM T1 M2 WHERE M2.C2 = M1.C2)
FROM T1 M1
```

### USAGE WITH FROM

```sql
SELECT C2, AVG(C3) FROM 
(SELECT C1, AVG(C3) FROM T3) T1 
JOIN T2
ON T1.C1=T2.C1
```

### USAGE WITH HAVING

```sql
SELECT * FROM T1
GROUP BY C1
HAVING AVG(C2) > (SELECT AVG(C2) FROM T1)
```

### USAGE WITH INSERT

```sql
INSERT INTO NT
(C1, C2)
SELECT C1, C2 FROM T1 WHERE C2 > (SELECT AVG(C2) FROM T1)
```

### USAGE WITH UPDATE

```sql
UPDATE NT
SET C3 = (
    SELECT SUM(C2) FROM T1
    WHERE T1.C1 = NT.C1
)
```

### USAGE WITH DELETE

```sql
DELETE FROM T1
WHERE C1 IN (
    {query|sq|ssq}
)
```
