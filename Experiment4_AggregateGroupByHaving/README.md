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
--
![Screenshot 2025-05-25 194246](https://github.com/user-attachments/assets/fa09e1ab-2fb5-4a30-8975-b43f8a42ad2e)

```sql
SELECT DoctorID, COUNT(*) AS TotalPrescriptions
FROM Prescriptions
GROUP BY DoctorID;
```

**Output:**
![Screenshot 2025-05-25 194326](https://github.com/user-attachments/assets/8865c40f-d31b-422b-b636-87bed6b6afe4)

**Question 2**
---
![Screenshot 2025-05-25 194352](https://github.com/user-attachments/assets/98aed71b-abd8-47fa-b11f-c4ae6345c974)


```sql
SELECT InsuranceCompany, COUNT(DISTINCT PatientID) AS TotalPatients
FROM Insurance
GROUP BY InsuranceCompany;
```

**Output:**
![Screenshot 2025-05-25 194450](https://github.com/user-attachments/assets/ee75b3cd-69c2-4972-966b-c437ff16f470)

**Question 3**
---
![Screenshot 2025-05-25 194521](https://github.com/user-attachments/assets/aa7d758b-2414-4ab7-944e-4bd87919e16c)

```sql
SELECT Diagnosis, COUNT(*) AS DiagnosisCount
FROM MedicalRecords
GROUP BY Diagnosis
ORDER BY DiagnosisCount DESC
LIMIT 1;
```

**Output:**
![Screenshot 2025-05-25 194619](https://github.com/user-attachments/assets/ae6d67c4-a931-4d00-b459-3b87519f8c89)

**Question 4**
---
![Screenshot 2025-05-25 194647](https://github.com/user-attachments/assets/2a787f88-3796-468e-bce8-f6cd3231ff6d)

```sql
SELECT COUNT(DISTINCT city) AS unique_cities
FROM customer;
```

**Output:**
![Screenshot 2025-05-25 194749](https://github.com/user-attachments/assets/7eec116e-0e0a-49bc-8a22-b5fcf4ba2e64)

**Question 5**
---
![Screenshot 2025-05-25 195020](https://github.com/user-attachments/assets/99d299bc-9e3a-490c-b7c1-d50dfcd9b2d7)

```sql
SELECT AVG(LENGTH(email)) AS avg_email_length
FROM customer;
```

**Output:**
![Screenshot 2025-05-25 195106](https://github.com/user-attachments/assets/24a78042-7ef5-44e5-bdb0-7ff744ced819)

**Question 6**
---
![Screenshot 2025-05-25 195140](https://github.com/user-attachments/assets/219c3ee6-4b31-4726-8f3c-258b17c7c14b)

```sql
SELECT MIN(purch_amt) AS MINIMUM
FROM orders;
```

**Output:**
![Screenshot 2025-05-25 195254](https://github.com/user-attachments/assets/61ce07b4-34d0-4ed1-870d-cbf12f3cff61)

**Question 7**
---
![Screenshot 2025-05-25 195335](https://github.com/user-attachments/assets/80fc97bb-b9ce-4574-9064-ad1269a02b95)

```sql
SELECT COUNT(*) AS employees_in_california
FROM employee
WHERE city = 'California';
```

**Output:**
![Screenshot 2025-05-25 195428](https://github.com/user-attachments/assets/8db7f80f-5f77-4f1a-a391-79d959949dc6)

**Question 8**
---
![Screenshot 2025-05-25 195457](https://github.com/user-attachments/assets/a1610adb-3330-4aa2-92cc-ed7372df2d8c)

```sql
SELECT (age / 5) * 5 AS age_group, SUM(salary)
FROM customer1
GROUP BY age / 5
HAVING Sum(salary) > 5000;
```

**Output:**
![Screenshot 2025-05-25 195745](https://github.com/user-attachments/assets/47961615-408d-4953-905d-2031f7df7e6e)


**Question 9**
---
![Screenshot 2025-05-25 200144](https://github.com/user-attachments/assets/d734980b-a4ec-4386-8aaa-fd0d3d6a030f)

```sql
SELECT jdate, MIN(workhour) 
FROM employee1
GROUP BY jdate
HAVING MIN(workhour) < 10;
```

**Output:**
![Screenshot 2025-05-25 200355](https://github.com/user-attachments/assets/0640309e-9290-4692-89d2-5f3d2cfcab5a)

**Question 10**
---
![Screenshot 2025-05-25 200526](https://github.com/user-attachments/assets/b70a5314-1325-4ae9-9328-6cfd8ed58ef6)

```sql
SELECT category_id, MIN(price) AS Price
FROM products
GROUP BY category_id
HAVING MIN(price) < 10;
```

**Output:**
![Screenshot 2025-05-25 200619](https://github.com/user-attachments/assets/fd4a4796-870a-48bf-9e2c-99982ae688bf)

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
![Screenshot 2025-05-25 200740](https://github.com/user-attachments/assets/55b91b2f-55ef-47cd-ac92-edde78d6247c)


