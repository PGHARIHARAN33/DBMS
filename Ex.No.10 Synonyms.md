# EXP NO 10: SYNONYMS AND ASSERTIONS IN SQL 
### DATE: 
## AIM:
To create a student database and create a synonym and assertions.

## THEORY
## SYNONYM
<div align="justify">
A SYNONYM provides another name for database object, referred to as original object, that may exist on a local or another server.
</div>
## ASSERTIONS
<div align="justify">
* An assertion is a piece of SQL which makes sure a condition is satisfied, else or it stops the action being taken on a database.
* An assertion is a constraint that might be dependent upon multiple rows of multiple tables.
</div>

## Query:
### *1) Create a table EMPLOYEE and perform insertion of two rows.

### SQL QUERY: 
CREATE TABLE EMPLOYEE (
    employee_id INT ,
    name VARCHAR(255),
    department VARCHAR(255),
    salary DECIMAL(10, 2)
);

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/99524abe-4670-471f-b9c6-492ec4a332a8)
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/4df6a047-63f5-4c88-a9b2-bb2ba89d8ff6)


### *2) Create a synonym S1 for EMPLOYEE  table.

### SQL QUERY: 
CREATE SYNONYM S1 FOR EMPLOYEE;
### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/b6be0a34-7d50-4df6-926e-ed6537415728)


### *3) Display the EMPLOYEE  table using synonym S1.
 
### SQL QUERY: 
SELECT * FROM S1;

### OUTPUT:

![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/643dc2cc-87fa-420c-836c-66eeb3d3c438)


### *4) Drop the synonym.

### SQL QUERY: 
DROP SYNONYM S1;

### OUTPUT:

![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/bd3bdb05-2b2c-4a86-8608-d76993e7849e)



### *5) Create a supplier table and create a sequence S2 for supplier table id.

### SQL QUERY: 
CREATE TABLE supplier (
    id INT,
    name VARCHAR(255),
    address VARCHAR(255),
    contact_person VARCHAR(255)
);

CREATE SEQUENCE S2 START 1;


### OUTPUT:

![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/213605f2-920f-413a-b71e-68cef165d0e9)


### *6) insert the data into supplier table use sequence.

### SQL QUERY: 
INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'ABC Suppliers', '123 Main Street', 'John Doe');

INSERT INTO supplier (id, name, address, contact_person)
VALUES (NEXTVAL('S2'), 'XYZ Distributors', '456 Elm Road', 'Jane Smith');

### OUTPUT:

![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/e00f86d8-64e3-4fc5-ad51-bd0abde4f795)

### 7) Drop the sequence

### SQL QUERY: 
DROP SEQUENCE S2;

### OUTPUT:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/ec99cb43-3eaa-4b6f-99f5-a3d11eed7267)

## RESULT :
### Thus the sequence and synonym created and used in SQL.
