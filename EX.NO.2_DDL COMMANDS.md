# EXP NO 2: DATA DEFINITION LANGUGE COMMANDS 
### DATE
## AIM:
To create a student database and execute DDL queries using SQL.


## THEORY
### DDL (Data Definition Language)

* DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema.
* It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database.
* DDL is a set of SQL commands used to create, modify, and delete database structures but not data.
* These commands are normally not used by a general user, who should be accessing the database via an application.

 
### List of DDL commands: 
1. CREATE: This command is used to create the database or its objects (like table, index, function, views, store procedure, and triggers).
2. DROP: This command is used to delete objects from the database.
3. ALTER: This is used to alter the structure of the database.
4. TRUNCATE: This is used to remove all records from a table, including all spaces allocated for the records are removed.
5. RENAME: This is used to rename an object existing in the database.

## Query:
### *1) Create a database studentdb

### SQL QUERY:
create database student_db;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/caa7fee4-598a-4762-97ac-a74a20dd1faf)


### *2) Create a table student  and insert any two rows with the following fieds RegisterNumber,Name,Age,Address,Phone number

### SQL QUERY: 
create table student(Regno int, Name varchar(20),Age int,Address varchar(50),Phonenumber varchar(10));


### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/18aadf96-e6b5-4ba7-85d3-b4815bf33e84)


### *3) Alter the above student table by adding another attribute department

### SQL QUERY: 
alter table student add dept varchar(20);

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/6f58dec4-cb3d-4c1a-9bbc-e870ff65d926)


### *4) Rename the student table to mystudent

### SQL QUERY: 
rename table student to mystudent;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/1e2c8b4d-13a9-48d1-9e66-952c634240f3)


### *5) Delete the mystudent rows using truncate keyword

### SQL QUERY: 
truncate table mystudent;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/c0c90d77-4671-4adf-9e92-5db773579c5b)

### *6) Drop the mystudent table
 
### SQL QUERY: 
drop table mystudent;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/086fb011-ec7c-4609-af9f-d116ea468728)









## Result:
         Thus the basic DDL commands in SQL are executed. 


