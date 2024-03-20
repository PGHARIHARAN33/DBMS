# EX.NO 4 Data Control Language (DCL) Commands and Transaction Control Languages (TCL) in SQL
### DATE:
## AIM:
To create a manager database and execute DML queries using SQL.
DEVELOPED BY: HARIHARAN P G
REG NO: 212222040050

# THEORY
## Data Control Language (DCL) commands
* Data control language (DCL) is used to access the stored data.
* It is mainly used for revoke and to grant the user the required access to a database.
## List of DCL commands: 
1. GRANT : It is used to insert data into a table.
2. REVOKE: It is used to update existing data within a table.
## Transaction control language(TCL) commands
1. COMMIT : COMMIT command in SQL is used to save all the transaction-related changes permanently to the disk
2. START TRANSACTION : to start the transaction
3. ROLLBACK : undo the transaction upto savepoint 
4. SAVEPOINT : create a savepoint to save the different parts of the same transaction using different names

### *Q1) Create a table employee with employee id ,name and Address

### QUERY:
create table employee(
emp_id numeric,
emp_name varchar(10),
addr varchar(40)
);

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/bcc493a9-b46e-4dfd-9bad-a2d2cbb5ea93)

### *Q2) Insert three rows into emploee table 


### QUERY:
INSERT INTO employee (employee_id, name, address)
VALUES (1, 'John Doe', '123 Main Street'),
       (2, 'Jane Doe', '456 Elm Street'),
       (3, 'Peter Parker', '789 Queens Boulevard');

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/32dc4bcb-4a0e-46b9-a05f-cfe960d7c40f)

### *Q3) Start the transaction and create a save point s1.

### QUERY:
START TRANSACTION;
SAVEPOINT s1;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/94a6cd82-84d3-4067-9cc2-9f22c8fb2a88)

### *Q4) Perform insertion into employee table.

### QUERY:
INSERT INTO employee (employee_id, name, address)
VALUES (4, 'Mary Jane Watson', '1011 Mockingbird Lane');

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/bb1b48a2-1e9d-4662-abda-9c484876eb1c)


### *Q5)	Display the employee table and create a save point s2 .


### QUERY:
SELECT * FROM employee;
SAVEPOINT s2;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/ca13c112-2561-436a-8488-58b004b130b9)


### *Q6)	Perform updation on any one of the row.


### QUERY:
UPDATE employee SET name = 'Spider-Man' WHERE employee_id = 3;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/c2b293de-ae00-484a-a8ad-64a5704a739f)


### *Q7) Display the employee table and rollback to  save point s2 


### QUERY:
SELECT * FROM employee;
ROLLBACK TO SAVEPOINT s2;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/8070008a-00c9-4292-b686-52c31c97184e)


### *Q8) Display the employee table and commit the changes; 


### QUERY:
SELECT * FROM employee;
COMMIT;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/0e8c90f1-6d5e-4308-8eb1-90b32bd1ddc9)


### *Q9) Rollback to save point s1;


### QUERY:
ROLLBACK TO SAVEPOINT s1;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/3979d0a3-bef3-4990-a5ff-f5d2a0bb933c)


### *Q10)	Create a new user and grant access to any one database with "insert and update"


### QUERY:
CREATE USER new_user;
GRANT INSERT, UPDATE ON database_name TO new_user;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/c04afcb8-c336-4cd8-a31c-60fc685abd1e)


### *Q11) Check the user access and display the result 


### QUERY:
SHOW GRANTS FOR new_user;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/4cec5c25-b86f-494b-b352-bba6c16b14b9)

### *Q12) Revoke the privillages.

### QUERY:
SHOW GRANTS FOR new_user;
REVOKE INSERT, UPDATE ON database_name FROM new_user;
SHOW GRANTS FOR new_user;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/10ab01c5-be48-4df6-a376-ffb4b0e5b212)

## RESULT :
Thus the basic TCL and DCL commands are executed.
