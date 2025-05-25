# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
![Screenshot 2025-05-25 223636](https://github.com/user-attachments/assets/a025d214-229d-42e7-9e83-7a006242e611)

```sql
SELECT *
FROM CUSTOMERS
WHERE SALARY > 4500;
```
**Output:**
![Screenshot 2025-05-25 224303](https://github.com/user-attachments/assets/78dae72b-9d33-4c5d-add0-f08411515ca9)

**Question 2**
---
![Screenshot 2025-05-25 224336](https://github.com/user-attachments/assets/30025900-e7ac-4ad7-8c21-23e5b413b3bd)

```sql
SELECT *
FROM GRADES
WHERE (subject, grade) IN (
  SELECT subject, MIN(grade)
  FROM GRADES
  GROUP BY subject
);
```

**Output:**
![Screenshot 2025-05-25 224422](https://github.com/user-attachments/assets/c8a5d00e-8169-4234-aebe-e80b71562104)

**Question 3**
---
![Screenshot 2025-05-25 224508](https://github.com/user-attachments/assets/6187abfa-5cde-4201-b29c-29f325289f6d)

```sql
SELECT student_name, grade
FROM GRADES
WHERE (subject, grade) IN (
  SELECT subject, MAX(grade)
  FROM GRADES
  GROUP BY subject
);
```
**Output:**
![Screenshot 2025-05-25 224553](https://github.com/user-attachments/assets/15a7eba8-fd87-483f-a3ad-2cc73d2bfdea)

**Question 4**
---
![Screenshot 2025-05-25 225558](https://github.com/user-attachments/assets/2d5afdec-dbc4-43c2-a545-55b9ea5a57a1)

```sql
SELECT o.ord_no, o.purch_amt, o.ord_date, o.customer_id, o.salesman_id
FROM ORDERS o
JOIN SALESMAN s ON o.salesman_id = s.salesman_id
WHERE s.city = 'New York'; 
```

**Output:**
![Screenshot 2025-05-25 231242](https://github.com/user-attachments/assets/9e071290-f8ef-4768-b43e-380bfe4aeb74)

**Question 5**
---
 ![Screenshot 2025-05-25 231311](https://github.com/user-attachments/assets/d08d6f16-e685-460e-87bf-d05668cb7797)


```sql
SELECT *
FROM customer
WHERE customer_id = (SELECT salesman_id FROM salesman WHERE name = 'Mc Lyon') - 2001;
```

**Output:**
![Screenshot 2025-05-25 232438](https://github.com/user-attachments/assets/7fd6a9b6-0720-4223-8188-be40a123824d)

**Question 6**
---
![Screenshot 2025-05-25 232532](https://github.com/user-attachments/assets/6957683e-b2d3-48e9-a0e1-ea3085d6cdd5)

```sql
SELECT *
FROM Employee
WHERE age < (SELECT AVG(age) FROM Employee WHERE income > 250000);
```

**Output:**
![Screenshot 2025-05-25 232624](https://github.com/user-attachments/assets/30a47081-bc88-49df-94be-30f4a552281f)

**Question 7**
---
![Screenshot 2025-05-25 233159](https://github.com/user-attachments/assets/f4d33350-a2b5-4918-ae7a-013ea0397e2c)

```sql
SELECT commission
FROM salesman
WHERE salesman_id IN ( SELECT salesman_id
                       FROM customer
                       WHERE city LIKE 'Paris' ) ;
```

**Output:**
![Screenshot 2025-05-25 233249](https://github.com/user-attachments/assets/845ac553-0b97-4f8e-bc5f-d69b5199e8f9)

**Question 8**
---
![Screenshot 2025-05-25 233316](https://github.com/user-attachments/assets/b829727a-6119-4c0b-9def-e7f4bad12342)

```sql
SELECT name
FROM customer
WHERE phone IN (
  SELECT phone
  FROM customer
  GROUP BY phone
  HAVING COUNT(*) = 1
);
```

**Output:**
![Screenshot 2025-05-25 233409](https://github.com/user-attachments/assets/84619554-8a4e-4887-b4a3-b7cb0656eec9)

**Question 9**
---
![Screenshot 2025-05-25 233444](https://github.com/user-attachments/assets/9522a509-b438-467a-8a96-cc53bde435a8)

```sql
SELECT department_id, department_name
FROM Departments
WHERE LENGTH(department_name) > (SELECT AVG(LENGTH(department_name)) FROM Departments);
```
**Output:**
![Screenshot 2025-05-25 233534](https://github.com/user-attachments/assets/e61e7d48-62df-4f57-8fb1-dfa4380bcd1f)

**Question 10**
---
![Screenshot 2025-05-25 233601](https://github.com/user-attachments/assets/27932da2-caa5-4c13-b4b4-0761148b79f9)

```sql
SELECT *
FROM CUSTOMERS
WHERE ADDRESS = 'Delhi' AND AGE < 30
ORDER BY ID;
```

**Output:**
![Screenshot 2025-05-25 233658](https://github.com/user-attachments/assets/d3c08254-bffb-4c93-bdf0-f499f426934b)


## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.
![Screenshot 2025-05-25 233809](https://github.com/user-attachments/assets/745857a1-92b1-4dac-935a-be42a76d6b36)

