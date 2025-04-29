# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
How many prescriptions were written in each frequency category (e.g., once daily, twice daily)?

Sample tablePrescriptions Table
![Screenshot (583)](https://github.com/user-attachments/assets/fa98ff76-b7b5-4ffb-94b8-41bd279034b4)

**Output:**

![Screenshot (584)](https://github.com/user-attachments/assets/077b9c7d-0239-4209-801f-3e8eaa77bf46)



**Question 2**

What is the average dosage prescribed for each medication?

Sample tablePrescriptions Table
![image](https://github.com/user-attachments/assets/92904f42-f9fe-425d-9028-5e3161d79826)


**Output:**

![image](https://github.com/user-attachments/assets/d1d838f3-c620-4010-a05d-155768af5925)



**Question 3**
How many appointments are scheduled for each doctor?

Sample table:Appointments Table
![image](https://github.com/user-attachments/assets/b3cf0128-8a54-4175-9eee-c4ef85d94b4f)


**Output:**

![image](https://github.com/user-attachments/assets/f2978cdf-8d0c-47b4-be1e-1cc699892568)



**Question 4**

Write a SQL query to return the total number of rows in the 'customer' table where the city is Noida.

Sample table: customer

![image](https://github.com/user-attachments/assets/1047d18f-4c10-4aa9-9de3-53bf0b0450a3)


**Output:**

![image](https://github.com/user-attachments/assets/ec56d92e-c7fa-48b7-ba73-8ca99dafb332)



**Question 5**

Write a SQL query to find the number of employees who are having the same age removing the duplicate values.

Sample table: employee

![image](https://github.com/user-attachments/assets/3e268ad8-496f-49f0-a4e4-0bd7936b29be)

**Output:**

![image](https://github.com/user-attachments/assets/0272d0ad-bcd1-4a89-912c-f3ecba9da486)


**Question 6**

Write a SQL query to calculate the average purchase amount of all orders. Return average purchase amount.

Sample table: orders

![image](https://github.com/user-attachments/assets/5dff57ea-f7b7-4ffa-8078-f6ad521563b6)


**Output:**

![image](https://github.com/user-attachments/assets/a88cabc0-1183-41c0-9764-36aa5bc0fc55)



**Question 7**

Write a SQL query to find the Fruit with the lowest available quantity.

Note: Inventory attribute contains amount of fruits

![image](https://github.com/user-attachments/assets/c09db1c4-2563-4a80-8be5-abbdf63d5b87)

**Output:**

![image](https://github.com/user-attachments/assets/c8189ca9-ac3b-4f9f-aab9-e3615605abc6)



**Question 8**

Write the SQL query that achieves the grouping of data by city, calculates the total income for each city, and includes only those cities where the total income sum is greater than 200,000.

Sample table: employee

![image](https://github.com/user-attachments/assets/600d0719-d0cc-484f-a593-e479763b8e0a)

**Output:**


![image](https://github.com/user-attachments/assets/88d6ab7d-b7f1-4af6-a5cb-a90416047b77)




**Question 9**

Write the SQL query to find how many patients have more than 3 medical records?.

Sample table: MedicalRecords

![image](https://github.com/user-attachments/assets/3252540e-f724-4c06-885e-6d00b2ba25f0)


**Output:**


![image](https://github.com/user-attachments/assets/c05dafa6-51db-4f2e-9e5c-52e9c4d7f7fa)


**Question 10**

Write the SQL query that achieves the grouping of data by occupation, calculates the average work hours for each occupation, and includes only those occupations where the average work hour falls between 10 and 12.

Sample table: employee1

![image](https://github.com/user-attachments/assets/809196ac-7d23-4b32-9ddd-996fc3277c36)


**Output:**

![image](https://github.com/user-attachments/assets/b9c1dd24-9f12-4125-abed-3fe02c1f1a25)



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
