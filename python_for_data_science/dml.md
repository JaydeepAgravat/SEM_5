# MYSQL DML command

- The main three DML (Data Manipulation Language) commands in MySQL are:

1. INSERT
2. UPDATE
3. DELETE

## 1. INSERT

```mysql
CREATE TABLE employees (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(50) NOT NULL,
  email VARCHAR(50) UNIQUE,
  hire_date DATE,
  salary DECIMAL(10,2) CHECK (salary >= 0),
  department_id INT,
  FOREIGN KEY (department_id) REFERENCES department(id)
);

INSERT INTO employees (id, name, email, hire_date, salary, department_id)
VALUES 
  (1, 'John Doe', 'jdoe@example.com', '2022-01-01', 50000, 1),
  (2, 'Jane Smith', 'jsmith@example.com', '2022-02-15', 60000, 2),
  (3, 'Bob Johnson', 'bjohnson@example.com', '2022-03-01', 55000, 1),
  (4, 'Sarah Williams', 'swilliams@example.com', '2022-04-01', 65000, 2),
  (5, 'Mike Davis', 'mdavis@example.com', '2022-05-15', 70000, 1);
```

## 2. UPDATE

```MYSQL
UPDATE TB
SET c1 = 'JAVA', c2 = 'second'
WHERE c1 = 'C' AND c1 = 'C++;
```

## 3. DELETE

```MYSQL
DELETE FROM TB
WHERE c1 = 'C' AND c1 = 'C++;
```
