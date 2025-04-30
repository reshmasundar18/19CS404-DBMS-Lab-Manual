# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**

Write a SQL statement to Change the category to 'Household' where product name contains 'Detergent' in the products table.

Products Table 

![image](https://github.com/user-attachments/assets/53caab71-b36e-41d5-aeb0-15956fc73068)


**Output:**

![image](https://github.com/user-attachments/assets/23417043-0704-4fe3-aced-1c24f6e65184)


**Question 2**

Decrease the reorder level by 30 percent where the product name contains 'cream' and quantity in stock is higher than reorder level in the products table.

PRODUCTS TABLE


**Output:**



**Question 3**

Write a SQL statement to Increase the selling price by 10% for all products in the 'Bakery' category in the products table.

Products table



**Output:**






**Question 4**

Write a SQL statement to Double the salary for employees in department 20 who have a job_id ending with 'MAN'

Employees table

---------------
employee_id
first_name
last_name
email
phone_number
hire_date
job_id
salary
commission_pct
manager_id
department_id






**Output:**





**Question 5**

Write a SQL statement to change the email column of employees table with 'Unavailable' for all employees in employees table.

Employees table

---------------
employee_id
first_name
last_name
email
phone_number
hire_date
job_id
salary
commission_pct
manager_id
department_id




**Output:**






**Question 6**

Write a SQL query to Delete customers from 'customer' table where 'GRADE' is greater than or equal to 2.



**Output:**





**Question 7**
Write a SQL query to remove rows from the table 'customer' with the following condition -

1. 'cust_country' must be 'India',

2. 'cus_city' must not be 'Chennai',





**Output:**





**Question 8**

Write a SQL query to Delete customers with following conditions

'CUST_COUNTRY' is not in a list of specified countries ('UK', 'USA', 'Canada')
'GRADE' is greater than or equal to 3



**Output:**



**Question 9**

Write a SQL query to Delete All Doctors with a NULL Specialization



**Output:**






**Question 10**

Write a SQL query to Delete All Doctors with a NULL Last Name



**Output:**

![image](https://github.com/user-attachments/assets/e7794c5e-b6f5-495b-80a0-a7e91016a377)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
