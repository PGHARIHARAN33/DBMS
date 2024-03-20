# Ex. No: 6 PL/SQL program using Triggers 
### DATE: 
### AIM: To create PL/SQL program to display new and old salary of customer when before/ after updation takes place. 

### Steps:
1. Create a trigger for each row when updation occurs.
2. Declare the variable in Declare section.
3. Start the begin section.
4. Calculate the salary changes.
5. Display the result 
6. End the begin section.

### Program:
CREATE TABLE employed(
  empid NUMBER,
  empname VARCHAR2(10),
  dept VARCHAR2(10),
  salary NUMBER
);

CREATE TABLE sal_log (
  log_id NUMBER GENERATED ALWAYS AS IDENTITY,
  empid NUMBER,
  empname VARCHAR2(10),
  old_salary NUMBER,
  new_salary NUMBER,
  update_date DATE
);

### Output:
![image](https://github.com/PGHARIHARAN33/DBMS/assets/123052484/111b2469-fd51-4071-9373-7ecdf23325dc)


### Result:
Thust the program was performed sucessfully.
