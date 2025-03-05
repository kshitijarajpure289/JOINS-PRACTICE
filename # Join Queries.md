#  Join Queries

### - INNER JOIN
### - LEFT JOIN
### - RIGHT JOIN
### - FULL JOIN

### Let's assume we have 2 tables

### EMPLOYEE_INFO

| EMPLOYEE_ID | NAME   | DEPARTMENT | SALARY |
| ----------- | ------ | ---------- | ------ |
| 1           | SEEMA  | FINANCE    | 20000  |
| 2           | RUTUJA | FINANCE    | 30000  |
| 3           | RUGVED | HR         | 20000  |
| 4           | KHUSHI | FINANCE    | 20000  |
| 5           | TRUPTI | HR         | 50000  |

 ### CUSTOMER_INFO

 | EMPLOYEE_ID | CUSTOMER_ID | NAME    |
 | ----------- | ----------- | ------- |
 | 1           | 89          | KETKI   |
 | 3           | 91          | RISHIKA |
 | 3           | 94          | SUKRUT  |
          
### INNER JOIN
### Query          
```sql
select * FROM EMPLOYEE_INFO
INNER JOIN CUSTOMER_INFO  
ON EMPLOYEE_INFO.EMPLOYEE_ID=CUSTOMER_INFO.EMPLOYEE_ID ;
```
### Result
| EMPLOYEE_ID | NAME   | DEPARTMENT | SALARY | EMPLOYEE_ID | CUSTOMER_ID | NAME    |
|-------------|--------|------------|--------|-------------|-------------|---------|
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |

### LEFT JOIN
### Query
```sql
 select * FROM EMPLOYEE_INFO
   Left JOIN CUSTOMER_INFO
  ON EMPLOYEE_INFO.EMPLOYEE_ID=CUSTOMER_INFO.EMPLOYEE_ID;
  ```
  ### Result
  | EMPLOYEE_ID | NAME   | DEPARTMENT | SALARY | EMPLOYEE_ID | CUSTOMER_ID | NAME    |
|-------------|--------|------------|--------|-------------|-------------|---------|
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 2           | RUTUA  | FINANCE    | 30000  | NULL        | NULL        | NULL    |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 4           | KHSUHI | FINANCE    | 20000  | NULL        | NULL        | NULL    |
| 5           | TRUPTI | HR         | 50000  | NULL        | NULL        | NULL    |

### RIGHT JOIN
### Query
```sql
select * FROM EMPLOYEE_INFO
 right JOIN CUSTOMER_INFO
  ON EMPLOYEE_INFO.EMPLOYEE_ID=CUSTOMER_INFO.EMPLOYEE_ID;
  ```
  ### Result
  | EMPLOYEE_ID | NAME   | DEPARTMENT | SALARY | EMPLOYEE_ID | CUSTOMER_ID | NAME    |
|-------------|--------|------------|--------|-------------|-------------|---------|
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
|             |        |            |        |             |             |         |
|             |        |            |        |             |             |         |
### FULL JOIN
### Query
```sql
 select * FROM EMPLOYEE_INFO 
   left JOIN CUSTOMER_INFO 
  ON EMPLOYEE_INFO.EMPLOYEE_ID=CUSTOMER_INFO.EMPLOYEE_ID
 UNION
 select * FROM EMPlOYEE_INFO
 RIGHT JOIN CUSTOMER_INFO
 ON EMPLOYEE_INFO.EMPLOYEE_ID=CUSTOMER_INFO.EMPLOYEE_ID;
 ```

 ### Result
 | EMPLOYEE_ID | NAME   | DEPARTMENT | SALARY | EMPLOYEE_ID | CUSTOMER_ID | NAME    |
|-------------|--------|------------|--------|-------------|-------------|---------|
| 1           | SEEEMA | FINANCE    | 20000  | 1           | 89          | KETKI   |
| 2           | RUTUA  | FINANCE    | 30000  | NULL        | NULL        | NULL    |
| 3           | RUGVED | HR         | 20000  | 3           | 94          | SUKRUT  |
| 3           | RUGVED | HR         | 20000  | 3           | 91          | RISHIKA |
| 4           | KHSUHI | FINANCE    | 20000  | NULL        | NULL        | NULL    |
| 5           | TRUPTI | HR         | 50000  | NULL        | NULL        | NULL    |
|             |        |            |        |             |             |         |
 
  

  