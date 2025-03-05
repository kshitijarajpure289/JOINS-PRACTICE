# JOINS-PRACTICE

*COMPANY*: CODTECH IT SOLUTIONS

*NAME*: KSHITIJA RAMESH RAJPURE

*INTERN ID*: CT08NTD

*DOMAIN*: SQL

*DURATION*: 4 WEEKS

*MENTOR*: NELLA SANTOSH KUMAR
##In this task, we focused on writing SQL queries utilizing different types of JOIN operations to retrieve and combine data from multiple tables. The objective was to showcase how JOINs function and how they are commonly applied in real-world scenarios. JOINs are fundamental in relational databases as they allow efficient data retrieval by linking records across tables based on related keys.

##Tools Used
To execute and test our SQL JOIN queries, we used the following tools:

1.MySQL Workbench – A graphical interface used for running SQL queries and managing databases.
2.Visual Studio Code – Used to edit, save, and document SQL scripts for further reference and sharing.

##Types of Joins and Their Applications

###1. INNER JOIN

An INNER JOIN returns only the matching records between two tables based on a common key. It excludes records that do not have corresponding matches in both tables.
Example Use Case: Fetching a list of employees along with their department names.
Real-World Use:
Used in HR systems to retrieve employees along with their assigned departments.

###2. LEFT JOIN (LEFT OUTER JOIN)
A LEFT JOIN returns all records from the left table and only matching records from the right table. If there’s no match, NULL is returned for columns from the right table.
Example Use Case: Listing all employees, including those not assigned to any department.
Real-World Use:
Used in payroll systems to list all employees, even those without an assigned department.

###3. RIGHT JOIN (RIGHT OUTER JOIN)
A RIGHT JOIN is the opposite of a LEFT JOIN—it retrieves all records from the right table and the matching records from the left table. NULL values appear for unmatched records from the left table.
Example Use Case: Displaying all departments, even those that do not have assigned employees.
Real-World Use:
Used in academic systems to list all courses (departments) and students (employees), even if no students are enrolled in some courses.

###4. FULL JOIN (FULL OUTER JOIN)
A FULL JOIN returns all records from both tables, filling unmatched rows with NULL values.
Example Use Case: Generating a report that includes all employees and all departments, even if some employees do not belong to a department or some departments do not have employees.
Real-World Use:
Used in business analytics to compare datasets from different departments for reporting.

###Practical Applications of JOINs

E-commerce: Analyzing purchase behavior by joining orders with customers.

Banking: Merging transactions with accounts for fraud detection.

Healthcare: Combining patients with appointments for medical scheduling.

Education: Linking students with courses for enrollment tracking.

Inventory Management: Joining products with suppliers to monitor stock levels.

JOINs are essential in SQL, allowing efficient data retrieval across tables. They are widely used across industries for reporting, data analysis, and application development. Mastering JOINs is crucial for database management and optimizing complex queries.
