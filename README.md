# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## DATE:
## AIM:
To create a manager database and execute DML queries using SQL.


## DML(Data Manipulation Language)
<div align="justify">
The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements. It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.
</div>

## List of DML commands: 
<div align="justify">
INSERT: It is used to insert data into a table.<br>
UPDATE: It is used to update existing data within a table.<br>
DELETE: It is used to delete records from a database table.<br>
</div>

## Create the table as given below:
```sql
create table manager(enumber number(6),ename char(15),salary number(5),commission number(4),annualsalary number(7),Hiredate date,designation char(10),deptno number(2),reporting char(10));
```
## insert the following values into the table
```sql
insert into manager values(7369,'Dharsan',2500,500,30000,'30-June-81','clerk',10,'John');
insert into manager values(7839,'Subu',3000,400,36000,'1-Jul-82','manager',null,'James');
insert into manager values(7934,'Aadhi',3500,300,42000,'1-May-82','manager',30,NULL);
insert into manager values(7788,'Vikash',4000,0,48000,'12-Aug-82','clerk',50,'Bond');
```

### Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
```
 UPDATE manager SET salary = salary * 1.10;
```
### OUTPUT:
![Screenshot 2023-11-06 153117](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/e8aa506d-573f-427e-af66-412d997147ce)

### Q2) Delete the records from manager table where the salary less than 2750.

### QUERY:
```
DELETE FROM manager WHERE salary < 2750;
```
### OUTPUT:
![Screenshot 2023-11-06 153245](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/039bacf7-91f1-41ff-8d32-7383501ea334)

### Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)

### QUERY:
```
SELECT ename AS "Name", annualsalary AS "Annual Salary" from manager;
```
### OUTPUT:
![Screenshot 2023-11-06 153455](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/7090f132-a3c1-43a6-91f8-10087a247e5b)

### Q5)	List the names of Clerks from emp table.

### QUERY:
```
SELECT ename FROM manager WHERE designation = 'clerk';
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/81c9f417-f769-4b3e-927d-7aa4a579a091)

### Q6)	List the names of employee who are not Managers.

### QUERY:
```
SELECT ename FROM manager WHERE designation <> 'manager';
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/cd7f7368-30ee-421b-8619-369fb6ec24b2)

### Q7)	List the names of employees not eligible for commission.

### QUERY:
```
SELECT ename FROM manager WHERE commission=0;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/5fddbde6-0861-4f1a-a180-a043b144292d)

### Q8)	List employees whose name either start or end with ‘s’.

### QUERY:
```
SELECT ename FROM manager WHERE ename LIKE 's%' OR ename LIKE '%s';
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/f1521e8a-b79f-461f-9827-1fbb972a7dfd)

### Q9) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

### QUERY:
```
 SELECT ename, designation, deptno, hiredate FROM manager ORDER BY hiredate;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/fbfe4df8-4b63-43f0-8107-8c9cd544070b)

### Q10) List the Details of Employees who have joined before 30 Sept 81.

### QUERY:
```
select * from manager WHERE hiredate < '1981-09-30';
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/2bfa4a4b-c7d0-4577-b3c7-9bfada7b5ab5)

### Q11)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.

### QUERY:
```
 SELECT ename, deptno, salary AS sal from manager ORDER BY deptno ASC, salary DESC;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/24180a7e-14de-425a-b4ec-004856f98486)

### Q12) List the names of employees not belonging to dept no 30,40 & 10

### QUERY:
```
SELECT ename FROM manager WHERE deptno NOT IN (10, 30, 40);
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/e5520430-d97b-435b-998a-a5d07be615db)

### Q13) Find number of rows in the table EMP

### QUERY:
```
 SELECT COUNT(*) AS "Number of Rows" from manager;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/ca5a6c2b-aece-4304-9d6e-5abf25df13c1)

### Q14) Find maximum, minimum and average salary in EMP table.

### QUERY:
```
 SELECT MAX(salary) AS "Maximum Salary" ,MIN(salary) AS "Minimum Salary" ,AVG(salary) AS "Average Salary" from manager;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/d7382b15-e29c-43f3-8aba-3b406cebf488)

### Q15) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
```
 SELECT designation AS "Job", COUNT(*) AS "Number of Employees" from manager group by designation order by count(*) DESC;
```
### OUTPUT:
![image](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/7a19bfb9-3fa8-4b70-90ca-4dcd68930ba3)
