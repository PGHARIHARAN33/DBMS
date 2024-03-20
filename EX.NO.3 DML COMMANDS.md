# EX 2 Data Manipulation Language (DML) Commands and built in functions in SQL
## AIM:
To create a manager database and execute DML queries using SQL.

# THEORY
## DML(Data Manipulation Language)
*  The SQL commands that deal with the manipulation of data present in the database belong to DML or Data Manipulation Language and this includes most of the SQL statements.
*  It is the component of the SQL statement that controls access to data and to the database. Basically, DCL statements are grouped with DML statements.

## List of DML commands: 
1. INSERT: It is used to insert data into a table.
2. UPDATE: It is used to update existing data within a table.
3. DELETE: It is used to delete records from a database table.
4. SELECT: The SELECT command shows the records of the specified table.

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

### *Q1) Update all the records of manager table by increasing 10% of their salary as bonus.

### QUERY:
update manager set salary=salary+(salary*0.10);


### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/59a94976-19e7-411c-82af-93120cc62313)


### *Q2) Delete the records from manager table where the salary less than 2750.


### QUERY:
delete from manager where salary<2750;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/ca905989-e2e8-4fb7-bf68-c917136cf93e)


### *Q3) Display each name of the employee as “Name” and annual salary as “Annual Salary” (Note: Salary in emp table is the monthly salary)


### QUERY:
select ename as "Name",salary*12 as "Annual salary" from manager;


### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/54e146d4-840a-44a3-9b64-aeeff065a236)


### *Q4)	List the names of Clerks from emp table.


### QUERY:
select ename from manager where designation='clerk';


### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/604f9e7c-824c-403f-a00f-2d9a73246bdc)


### *Q5)	List the names of employee who are not Managers.


### QUERY:
select ename from manager where designation <> 'manager';

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/4c2d4845-9325-48c4-8a81-a08ff3e1b59c)



### *Q6)	List the names of employees not eligible for commission.


### QUERY:
select ename from manager where commission=0;
### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/1ff1bdfa-8706-4889-9c4f-c1993220f745)


### *Q7)	List employees whose name either start or end with ‘s’.


### QUERY:
select ename from manager where ename like '%s' or ename like 's%';

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/627f25be-1707-46e6-a57c-d5cb23dc97af)


### *Q8) Sort emp table in ascending order by hire-date and list ename, job, deptno and hire-date.

### QUERY:
select ename,designation as "job",deptno,hiredate from manager order by hiredate asc;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/ce8c5783-5bd1-495c-b8d1-37a7d07ec1af)


### *Q9) List the Details of Employees who have joined before 30 Sept 81.


### QUERY:
select * from manager where hiredate<to_date('1981-09-30','YYYY-MM-DD');
### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/602bcb33-dd33-414c-beda-c96989a63303)


### *Q10)	List ename, deptno and sal after sorting emp table in ascending order by deptno and then descending order by sal.


### QUERY:
 select ename,deptno,salary from manager order by deptno asc,salary desc;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/36ddb871-6218-4e49-9f1a-099cbeb018ae)


### *Q11) List the names of employees not belonging to dept no 30,40 & 10


### QUERY:
select ename from manager where deptno not in (30,40,10);

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/0097647d-23e2-4db0-9f08-416b41b2b38c)


### *Q12) Find number of rows in the table EMP

### QUERY:
 select count(*) from manager;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/933d4a69-0d6a-47c1-8b8f-b7e44c9a93c6)


### *Q13) Find maximum, minimum and average salary in EMP table.

### QUERY:
select max(salary) from manager;
select min(salary) from manager;
select avg(salary) from manager;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/4615a0d8-20f2-4d5f-8ae9-3b739a395dfe)
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/759ea093-2a98-4c42-8fa2-4c8255703b97)
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/122dbe42-f2d2-4f6a-881d-a20e325ce60e)


### *Q14) List the jobs and number of employees in each job. The result should be in the descending order of the number of employees.

### QUERY:
SELECT designation AS job, COUNT(*) AS num_employees FROM manager GROUP BY designation ORDER BY num_employees DESC;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/beae01c5-55bb-479f-a5a4-0123237af388)


## RESULT :
Thus the basic DML commands are executed.
