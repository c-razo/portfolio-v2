# SQL Filtering Lab

**By Christopher Razo**

---

## Project Overview

The **SQL Filtering Lab** is designed to showcase practical SQL queries to filter and manipulate data. This project highlights the use of SQL for cybersecurity investigations and organizational data management, all executed within a MariaDB environment on a Kali Linux VM.

---

## Steps and Queries

### **Step 1: Open the MariaDB Shell**

**Explanation**: Opened the MariaDB shell to interact with the database on my Kali Linux VM. Accessing the database shell is essential for executing SQL commands directly and managing data effectively.

**Command Used**: `sudo mysql -u root`

![Open the MariaDB Shell](assets/images/1.png)

---

### **Step 2: Create the Organization Database**

**Explanation**: Created the organization database as the primary container for storing tables used in the lab. Databases organize data into tables, allowing efficient storage and retrieval of information for analysis.

**Command Used**:  
```
CREATE DATABASE organization;  
USE organization;
```

![Create the Organization Database](assets/images/3.png)

---

### **Step 3: Create the log_in_attempts Table**

**Explanation**: Set up the `log_in_attempts` table to record login data, including timestamps, success status, and country of origin. This table helped simulate data related to login activities.

**Command Used**:  
```
CREATE TABLE log_in_attempts (
    id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50),
    login_time TIME,
    login_date DATE,
    success BOOLEAN,
    country VARCHAR(50)
);
```

![Create the log_in_attempts Table](assets/images/4.png)

---

### **Step 4: Insert Sample Data into log_in_attempts**

**Explanation**: Populated the `log_in_attempts` table with sample data, including successful and failed login attempts at various times, dates, and countries.

**Command Used**:  
```
INSERT INTO log_in_attempts (username, login_time, login_date, success, country) VALUES
('user1', '19:30:00', '2022-05-08', 0, 'USA'),
('user2', '09:15:00', '2022-05-08', 1, 'MEX'),
('user3', '20:00:00', '2022-05-08', 0, 'CANADA');
```

![Insert Sample Data into log_in_attempts](assets/images/5.png)

---

### **Step 5: Run Query for Task 1 (After-Hours Failed Login Attempts)**

**Explanation**: Used the AND operator to filter for login attempts that failed after business hours, simulating suspicious activity after-hours.

**SQL Query Used**:  
```
SELECT * FROM log_in_attempts
WHERE login_time > '18:00:00' AND success = 0;
```

![Run Query for Task 1 (After-Hours Failed Login Attempts)](assets/images/6.png)

---

### **Step 6: Run Query for Task 2 (Login Attempts on Specific Dates)**

**Explanation**: Used the OR operator to filter for login attempts on specified dates, useful for investigating incidents on specific days.

**SQL Query Used**:  
```
SELECT * FROM log_in_attempts
WHERE login_date = '2022-05-08' OR login_date = '2022-05-09';
```

![Run Query for Task 2 (Login Attempts on Specific Dates)](assets/images/7.png)

---

### **Step 7: Run Query for Task 3 (Login Attempts Outside of Mexico)**

**Explanation**: Used the NOT and LIKE operators to retrieve login attempts that didn’t originate from Mexico.

**SQL Query Used**:  
```
SELECT * FROM log_in_attempts
WHERE NOT country LIKE 'MEX%';
```

![Run Query for Task 3 (Login Attempts Outside of Mexico)](assets/images/8.png)

---

### **Step 8: Create the employees Table**

**Explanation**: Created the `employees` table to store employee information, including usernames, departments, and office locations.

**Command Used**:  
```
CREATE TABLE employees (
    id INT PRIMARY KEY AUTO_INCREMENT,
    username VARCHAR(50),
    department VARCHAR(50),
    office VARCHAR(50)
);
```

![Create the employees Table](assets/images/9.png)

---

### **Step 9: Insert Sample Data into employees**

**Explanation**: Populated the `employees` table with sample records across different departments and locations.

**Command Used**:  
```
INSERT INTO employees (username, department, office) VALUES
('elarson', 'Marketing', 'East-170'),
('jclark', 'Marketing', 'East-320'),
('alevitsk', 'Finance', 'West-210');
```

![Insert Sample Data into employees](assets/images/10.png)

---

### **Step 10: Run Query for Task 4 (Employees in Marketing, East Building)**

**Explanation**: Used the AND and LIKE operators to filter for employees in the Marketing department located in the East building.

**SQL Query Used**:  
```
SELECT * FROM employees
WHERE department = 'Marketing' AND office LIKE 'East%';
```

![Run Query for Task 4 (Employees in Marketing, East Building)](assets/images/11.png)

---

### **Step 11: Run Query for Task 5 (Employees in Finance or Sales Departments)**

**Explanation**: Used the OR operator to retrieve employees in either the Finance or Sales departments.

**SQL Query Used**:  
```
SELECT * FROM employees
WHERE department = 'Finance' OR department = 'Sales';
```

![Run Query for Task 5 (Employees in Finance or Sales Departments)](assets/images/12.png)

---

### **Step 12: Run Query for Task 6 (Employees Not in Information Technology)**

**Explanation**: Used the != operator to exclude employees in the Information Technology department.

**SQL Query Used**:  
```
SELECT * FROM employees
WHERE department != 'Information Technology';
```

![Run Query for Task 6 (Employees Not in Information Technology)](assets/images/13.png)

---

## Navigation

[⬅️ Back to Projects](../index.md#projects)  
[🔝 Back to Top](#sql-filtering-lab)
