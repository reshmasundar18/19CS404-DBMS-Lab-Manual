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
--
![Screenshot 2025-05-25 191611](https://github.com/user-attachments/assets/c31e6abe-a8fb-4f4b-bb43-ce60cd1be957)

```sql
UPDATE Employees
SET salary = 8000
WHERE employee_id = 105 AND salary < 5000;
```

**Output:**
![Screenshot 2025-05-25 191717](https://github.com/user-attachments/assets/fc248201-688d-4b75-a621-6850eafb8b90)

**Question 2**
---
![Screenshot 2025-05-25 192012](https://github.com/user-attachments/assets/f283298a-38e7-4875-bb00-22e55c56d311)

```sql
UPDATE purchases
SET per_unit_price = 25,
    total_price = quantity * 25
WHERE purchase_date = '2022-08-15' AND product_id = 12;
```

**Output:**
![Screenshot 2025-05-25 192120](https://github.com/user-attachments/assets/c3447be9-da27-4a77-a72a-832c56091694)

**Question 3**
---
![Screenshot 2025-05-25 192154](https://github.com/user-attachments/assets/4b11fe87-beb3-4b4a-8d94-1e9ccf315911)

```sql
UPDATE Employees
SET salary = salary * 2
WHERE department_id = 20 AND job_id LIKE '%MAN';
```

**Output:**
![Screenshot 2025-05-25 192319](https://github.com/user-attachments/assets/2106cba5-eb2b-4e9d-9e4e-5da7dceca46e)

**Question 4**
---
![Screenshot 2025-05-25 192408](https://github.com/user-attachments/assets/71b85d12-1500-410c-8ff9-dac73cae06ba)

```sql
UPDATE SALES
SET total_sell_price = quantity * sell_price
WHERE product_id = 10;
```

**Output:**
![Screenshot 2025-05-25 192458](https://github.com/user-attachments/assets/76f62778-7f08-4ae7-93a7-e8d3b09285f9)


**Question 5**
---
![Screenshot 2025-05-25 192523](https://github.com/user-attachments/assets/7b1c0ef9-473d-4cfb-b22f-aaea95bfa299)

```sql
UPDATE Products
SET quantity = quantity * 1.1;
```

**Output:**
![Screenshot 2025-05-25 192611](https://github.com/user-attachments/assets/7ffa43e8-3852-4a39-901a-1680fefb3c0f)

**Question 6**
---
![Screenshot 2025-05-25 192649](https://github.com/user-attachments/assets/e5547692-4899-447c-a2af-b38f1e8d28c0)

```sql
DELETE FROM Customer
WHERE (GRADE > 2 AND PAYMENT_AMT < (SELECT AVG(PAYMENT_AMT) FROM Customer))
OR OUTSTANDING_AMT > 8000;
```

**Output:**
![Screenshot 2025-05-25 192753](https://github.com/user-attachments/assets/4cccd9f5-1290-42b1-a13b-57ba13fe5a23)

**Question 7**
---
![Screenshot 2025-05-25 192923](https://github.com/user-attachments/assets/c40d6ea1-cb6a-4a95-b0b5-a5a7b156a4ab)

```sql
DELETE FROM Doctors
WHERE doctor_id = 1;
```

**Output:**
![Screenshot 2025-05-25 193029](https://github.com/user-attachments/assets/a39d3def-e37d-498d-b15b-451df41a1f0d)

**Question 8**
---
![Screenshot 2025-05-25 193108](https://github.com/user-attachments/assets/9854408e-7435-4009-b665-dee00b959fa9)

```sql
DELETE FROM customer
WHERE cust_country = 'India' AND cust_city != 'Chennai';
```

**Output:**
![Screenshot 2025-05-25 193229](https://github.com/user-attachments/assets/bed148cb-ff05-4406-a0e9-d8659733fa05)

**Question 9**
---
![Screenshot 2025-05-25 193312](https://github.com/user-attachments/assets/5df3d6cc-2853-4e8a-ae6b-c826e1311e69)

```sql
DELETE FROM Customer
WHERE CUST_COUNTRY = 'UK' AND WORKING_AREA = 'London' AND GRADE < 3;
```

**Output:**
![Screenshot 2025-05-25 193401](https://github.com/user-attachments/assets/6816ee9f-a5f4-438f-89ff-cf7e7247f3e7)

**Question 10**
---
![Screenshot 2025-05-25 193435](https://github.com/user-attachments/assets/fd3ce29e-62d7-44d9-8a2b-a2384e450f86)

```sql
DELETE FROM Customer
WHERE GRADE = 3 AND CUST_NAME LIKE '%BBB%' AND PAYMENT_AMT > 2000;
```

**Output:**
![Screenshot 2025-05-25 193528](https://github.com/user-attachments/assets/dcfe058e-9ae5-4180-9ad6-ffc125f0fec1)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
![Screenshot 2025-05-25 193726](https://github.com/user-attachments/assets/84ae42e0-ec87-4609-bd3d-6da59cbb9e57)

