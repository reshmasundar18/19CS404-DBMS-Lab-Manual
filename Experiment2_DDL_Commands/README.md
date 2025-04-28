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
Write an SQL query to add a new column email of type TEXT to the Student_details table, and ensure that this column cannot contain NULL values and make default value as 'Invalid'

![Screenshot (562)](https://github.com/user-attachments/assets/2c9031e9-3a5d-4b50-9d4a-59a2bab75925)


**Output:**

![Screenshot (563)](https://github.com/user-attachments/assets/22ba52c2-cf4b-4c5e-a217-2f5d9baa71f0)



**Question 2**

Write a SQL query to add birth_date attribute as timestamp (datatype) in the table customer 

Sample table: customer

![Screenshot (564)](https://github.com/user-attachments/assets/526d34a5-0a3a-4f66-bbc3-38a7800a3372)



**Output:**

![Screenshot (565)](https://github.com/user-attachments/assets/687006af-3c5e-4b00-ad2e-f14dfb1e946d)



**Question 3**

Create a table named Invoices with the following constraints:

InvoiceID as INTEGER should be the primary key.
InvoiceDate as DATE.
DueDate as DATE should be greater than the InvoiceDate.
Amount as REAL should be greater than 0.

![Screenshot (566)](https://github.com/user-attachments/assets/6e0ca33d-3af2-4b03-9dad-cea58cfaea96)

**Output:**

![Screenshot (568)](https://github.com/user-attachments/assets/5dc31042-b668-4363-b5cb-985d1010d9f9)


**Question 4**

Insert all students from Archived_students table into the Student_details table.
![Screenshot (567)](https://github.com/user-attachments/assets/0887579d-b476-46a7-9885-14e40f9203c8)


**Output:**

![Screenshot (569)](https://github.com/user-attachments/assets/e1ec8c75-70ae-4da1-90a6-9e152f662076)



**Question 5**
Create a table named Customers with the following columns:

CustomerID as INTEGER
Name as TEXT
Email as TEXT
JoinDate as DATETIME

![Screenshot (570)](https://github.com/user-attachments/assets/2173739b-d0db-49eb-abd0-1ff7e7b6e450)


**Output:**
![Screenshot (571)](https://github.com/user-attachments/assets/dec33c28-72bb-495e-b0bc-5cbd79309b9a)


**Question 6**

Create a new table named orders with the following specifications:
ord_id as TEXT with a length of 4.
item_id as TEXT.
ord_date as DATE.
ord_qty as INTEGER.
cost as INTEGER.
The primary key is a composite key consisting of item_id and ord_date.
ord_id and item_id should not accept NULL

![Screenshot (572)](https://github.com/user-attachments/assets/3ec36549-1328-4fc0-8839-dd8982b7a22a)



**Output:**

![Screenshot (573)](https://github.com/user-attachments/assets/a0bb056e-b40c-4b78-a16c-6eb7e5bc94b5)



**Question 7**

Create a table named Invoices with the following constraints:
InvoiceID as INTEGER should be the primary key.
InvoiceDate as DATE.
Amount as REAL should be greater than 0.
DueDate as DATE should be greater than the InvoiceDate.
OrderID as INTEGER should be a foreign key referencing Orders(OrderID).

![Screenshot (574)](https://github.com/user-attachments/assets/7f58f2d1-d4fe-4164-93fe-5ca6b2de2358)



**Output:**
![Screenshot (575)](https://github.com/user-attachments/assets/309589de-fe9f-4882-843e-1207f5081152)


**Question 8**

Insert the below data into the Customers table, allowing the City and ZipCode columns to take their default values.

![Screenshot (576)](https://github.com/user-attachments/assets/c6ab31fd-298c-4ed4-93cc-2ce2d1913610)



**Output:**

![Screenshot (577)](https://github.com/user-attachments/assets/967fdc40-8d10-4b12-b6ab-228916158b27)


**Question 9**

In the Student_details table, insert a student record where some fields are NULL, another record where all fields are filled without any NULL values, and a third record where some fields are filled, and others are left as NULL.


![Screenshot (579)](https://github.com/user-attachments/assets/6db2f61d-f8c8-4f4f-8d8a-e7f9e1a744dd)

**Output:**

![Screenshot (580)](https://github.com/user-attachments/assets/496b6bd4-46e0-477b-ab7e-06f11577810b)


**Question 10**

Create a table named Departments with the following columns:

DepartmentID as INTEGER
DepartmentName as TEXT

![Screenshot (581)](https://github.com/user-attachments/assets/8cfd6864-b90e-41e2-8b27-2d63bf594473)


**Output:**

![Screenshot (582)](https://github.com/user-attachments/assets/e8345f0a-abbb-404e-9bdb-ef57ac038327)


## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
