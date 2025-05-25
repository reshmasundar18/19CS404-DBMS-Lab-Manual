# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
![Screenshot 2025-05-25 165215](https://github.com/user-attachments/assets/bf7b8b29-e510-4b32-b289-80996a63ee4f)

```
CREATE TABLE  Bonuses (
BonusID INTEGER PRIMARY KEY,
EmployeeID INTEGER,
BonusAmount REAL CHECK(BonusAmount > 0),
BonusDate DATE,
Reason TEXT NOT NULL,
FOREIGN KEY (EmployeeID) REFERENCES Employees(EmployeeID)
);
```

**Output:**
![Screenshot 2025-05-25 165358](https://github.com/user-attachments/assets/e5ff19bf-7580-4e04-b576-780c11f98919)


**Question 2**
---
![Screenshot 2025-05-25 165515](https://github.com/user-attachments/assets/191702d6-5638-4bfb-9041-a804d8f41599)

```
ALTER TABLE customers
ADD COLUMN email TEXT;
```

**Output:**
![Screenshot 2025-05-25 165622](https://github.com/user-attachments/assets/2f916e6f-16b0-491e-96be-1b74086c9f06)


**Question 3**
---
![Screenshot 2025-05-25 165655](https://github.com/user-attachments/assets/7df3d0ec-9b64-4926-ab90-99e6e6720608)

```
INSERT INTO Student_details (RollNo, Name, Gender, Subject, MARKS)
SELECT RollNo, Name, Gender, Subject, MARKS
FROM Archived_students
```

**Output:**
![Screenshot 2025-05-25 165753](https://github.com/user-attachments/assets/6827097f-a132-44cf-9bbb-09098a91b322)


**Question 4**
---
![Screenshot 2025-05-25 165834](https://github.com/user-attachments/assets/b9ca3170-409a-40c3-9537-adc925640d17)

```
ALTER TABLE Student_details 
ADD COLUMN mobilenumber number;
```

**Output:**
![Screenshot 2025-05-25 170044](https://github.com/user-attachments/assets/d4f7ae2d-ab09-452e-bff8-75aa24747feb)


**Question 5**
---
![Screenshot 2025-05-25 170138](https://github.com/user-attachments/assets/487cb97c-5b18-4c0b-8c36-c56872e57da6)

```
CREATE TABLE Shipments (
ShipmentID INTEGER PRIMARY KEY,
ShipmentDate DATE,
SupplierID INTEGER,
OrderID INTEGER,
FOREIGN KEY (SupplierID) REFERENCES Suppliers(SupplierID),
FOREIGN KEY (OrderID) REFERENCES Orders(OrderID)
);
```

**Output:**
![Screenshot 2025-05-25 170239](https://github.com/user-attachments/assets/3f4bc2b6-37a8-46bb-9149-30b95c782190)


**Question 6**
---
![Screenshot 2025-05-25 170336](https://github.com/user-attachments/assets/63d2170d-b3df-47b3-8e19-80936c8fde06)

```
CREATE TABLE Tasks (
TaskID INTEGER,
TaskName TEXT,
DueDate DATE
);
```

**Output:**
![Screenshot 2025-05-25 170512](https://github.com/user-attachments/assets/f8b34074-d6a9-4360-bfc8-a89ad085af33)


**Question 7**
---
![Screenshot 2025-05-25 170602](https://github.com/user-attachments/assets/c8c70946-34e4-40f0-9493-2f0a3275a407)

```
CREATE TABLE Products (
ProductID INTEGER PRIMARY KEY,
ProductName TEXT NOT NULL,
Price REAL CHECK(Price > 0),
Stock INTEGER CHECK(Stock >= 0)
);
```

**Output:**
![Screenshot 2025-05-25 170720](https://github.com/user-attachments/assets/9ec9a0bd-5c89-4a57-b15b-6fe965af51a5)


**Question 8**
---
![Screenshot 2025-05-25 170808](https://github.com/user-attachments/assets/6f34e357-7633-422b-b6ca-43b6dfd94c7f)

```
INSERT INTO Student_details (RollNo, Name, Gender, Subject, MARKS)
VALUES 
(205, 'Olivia Green', 'F', NULL, NULL),
(207, 'Liam Smith', 'M', 'Mathematic', 85),
(208, 'Sophia Johns', 'F', 'Science', NULL);
```

**Output:**
![Screenshot 2025-05-25 170920](https://github.com/user-attachments/assets/d40f86c0-0050-4ad9-af42-334e28bb78d2)


**Question 9**
---
![Screenshot 2025-05-25 171000](https://github.com/user-attachments/assets/66fdb851-14a1-48d5-b27d-4f490dd4d6f2)

```
CREATE TABLE item (
item_id TEXT PRIMARY KEY,
item_desc TEXT NOT NULL,
rate INTEGER NOT NULL,
icom_id TEXT(4),
FOREIGN KEY (icom_id) REFERENCES company(com_id) ON UPDATE SET NULL ON DELETE SET NULL
);
```

**Output:**

![Screenshot 2025-05-25 171122](https://github.com/user-attachments/assets/924d2f37-33a9-4fa1-b645-1e157df71f1d)


**Question 10**
---
![Screenshot 2025-05-25 171150](https://github.com/user-attachments/assets/94382117-a4a1-48fa-bda5-7d25c5ffb4b9)

```
INSERT INTO Student_details (RollNo, Name, Gender, Subject, MARKS)
VALUES
(201, 'David Lee', 'M', 'Physics', 92)
```

**Output:**

![Screenshot 2025-05-25 171303](https://github.com/user-attachments/assets/404370d9-127b-4fc3-838c-db1d02d74580)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
![Screenshot 2025-05-25 190657](https://github.com/user-attachments/assets/6c09ac65-752a-435e-ab47-5e2e0abe239f)

