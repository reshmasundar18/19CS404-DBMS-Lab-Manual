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

![image](https://github.com/user-attachments/assets/749060d2-c50f-47bb-9f16-f1ac60ee8104)

**Output:**

![image](https://github.com/user-attachments/assets/f5515294-f1b6-4459-86ec-9a3ca0df3abe)



**Question 2**

Decrease the reorder level by 30 percent where the product name contains 'cream' and quantity in stock is higher than reorder level in the products table.

PRODUCTS TABLE
![image](https://github.com/user-attachments/assets/f33c03fa-76f4-44ec-8875-dbd76cf854ee)

**Output:**

![image](https://github.com/user-attachments/assets/783364b6-abb8-4b03-8199-cdae43070f3b)


**Question 3**

Write a SQL statement to Increase the selling price by 10% for all products in the 'Bakery' category in the products table.

Products table
![image](https://github.com/user-attachments/assets/3fefd9c0-436a-453a-adf0-885761055a24)


**Output:**


![image](https://github.com/user-attachments/assets/acafadb0-3d7f-43e2-95ad-a12d9c86b4f8)



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

![image](https://github.com/user-attachments/assets/81b4d975-ebf7-4044-824d-07304eff61ec)




**Output:**

![image](https://github.com/user-attachments/assets/b03eec29-5248-4176-9a63-83369d464b55)



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

![image](https://github.com/user-attachments/assets/612d83d4-74af-48dd-97a9-748b8f5fd444)


**Output:**


![image](https://github.com/user-attachments/assets/4d8af776-dc21-449e-973c-784986f66025)



**Question 6**

Write a SQL query to Delete customers from 'customer' table where 'GRADE' is greater than or equal to 2.
![image](https://github.com/user-attachments/assets/3e99b990-7501-4977-8282-6a9f69c19051)


**Output:**

![image](https://github.com/user-attachments/assets/e715d834-1a58-4e70-b852-b4da107096ec)



**Question 7**
Write a SQL query to remove rows from the table 'customer' with the following condition -

1. 'cust_country' must be 'India',

2. 'cus_city' must not be 'Chennai',

3. ![image](https://github.com/user-attachments/assets/a0e6e47c-ac17-4610-86cb-dd488fe79f23)



**Output:**


![image](https://github.com/user-attachments/assets/552e94d1-c23b-4358-b6b8-0a8d2cfc7c61)


**Question 8**

Write a SQL query to Delete customers with following conditions

'CUST_COUNTRY' is not in a list of specified countries ('UK', 'USA', 'Canada')
'GRADE' is greater than or equal to 3
![image](https://github.com/user-attachments/assets/d1be6c14-4655-4e1d-9760-7c8daba46bcb)


**Output:**
![image](https://github.com/user-attachments/assets/33ae747a-ecb4-4d13-93b4-3bbcff855d33)


**Question 9**

Write a SQL query to Delete All Doctors with a NULL Specialization

![image](https://github.com/user-attachments/assets/13fa52bc-8132-4c05-8abe-ca787c569e42)

**Output:**

![image](https://github.com/user-attachments/assets/6384630f-a460-48ef-91f0-08e3b66b6182)




**Question 10**

Write a SQL query to Delete All Doctors with a NULL Last Name

![image](https://github.com/user-attachments/assets/ec083648-e88f-478c-88f8-60bc144d4136)


**Output:**

![image](https://github.com/user-attachments/assets/e7794c5e-b6f5-495b-80a0-a7e91016a377)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
