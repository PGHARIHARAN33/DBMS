# EXP NO 1: ER DIAGRAM CREATION, RELATIONAL MODEL AND SCHEMA GENERATION  
### DATE
## AIM:
<div align="justify">
   To create a ER Diagram for Bank management system or College management system using ERD Plus tool and generate the relational model with schema. 
</div>

## Algorithm
1. Create a login with https://erdplus.com.
2. Create a new ER Diagram with name
3. Create a strong entity, relation and attributes.
4. Create a weak entity, relation and attributes.
5. Specify attributes unique, multivalued and composite attributes.

### ER Diagram 
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/967ecb7d-0a42-44e5-b7fb-dd8e1bd66dea)



### Relational model
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/d256560d-8b69-4cc1-b50e-d61d47a66e5f)



### SQL DDL Schema 
CREATE TABLE BANK
(
  code INT NOT NULL,
  Name INT NOT NULL,
  Addr INT NOT NULL,
  PRIMARY KEY (code)
);

CREATE TABLE BANK_BRANCH
(
  Addr INT NOT NULL,
  Branch_no INT NOT NULL,
  PRIMARY KEY (Branch_no)
);

CREATE TABLE Loan
(
  Loan_no INT NOT NULL,
  Amount INT NOT NULL,
  Type INT NOT NULL,
  PRIMARY KEY (Loan_no)
);

CREATE TABLE Account
(
  Acct_no INT NOT NULL,
  Balance INT NOT NULL,
  Type INT NOT NULL
);

CREATE TABLE CUSTOMER
(
  Name INT NOT NULL,
  Ssn INT NOT NULL,
  Addr INT NOT NULL,
  Phone INT NOT NULL,
  PRIMARY KEY (Ssn)
);

## RESULT 
<div align="justify">
Thus the ER diagram was drawn and relational diagram, SQL DDL staements are generated using ERD plus tool.
</div>
