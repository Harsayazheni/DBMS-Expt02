# DBMS-Expt02

## Aim
To study and implement DDL commands and different types of constraints.

## Theory
 1. CREATE: 
This is used to create a new relation (table) 

Syntax:
CREATE TABLE (field_1 data_type(size),field_2 data_type(size), .. . );
           
 2. ALTER:
This is used to add some extra fields into existing relation. 

Syntax: 
ALTER TABLE relation_name ADD (new field_1 data_type(size) );
      
(a)ALTER TABLE ...ADD...: 
ALTER TABLE std ADD (Address CHAR(10));

(b )ALTER TABLE...MODIFY...:
ALTER TABLE relation_name MODIFY (field_1 newdata_type(Size)

( c) ALTER TABLE..DROP....
ALTER TABLE relation_name DROP COLUMN (field_name); 

(d)ALTER TABLE..RENAME...:
ALTER TABLE relation_name RENAME COLUMN (OLD field_name) to (NEW field_name);

3. DROP TABLE: 
This is used to delete the structure of a relation. It permanently deletes the records in the table. 

Syntax: 
DROP TABLE relation_name;
            
4.RENAME:
It is used to modify the name of the existing database object.
 
Syntax: 
 RENAME TABLE old_relation_name TO new_relation_name;                  


CONSTRAINTS: Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE statement) or after the table is created (using ALTER TABLE statement). 

1. NOT NULL: When a column is defined as NOTNULL, then that column becomes a mandatory column. It implies that a value must be entered into the column if the record is to be accepted for storage in the table. 

Syntax: CREATE TABLE Table_Name (column_name data_type (size) NOT NULL, );

2. UNIQUE: The purpose of a unique key is to ensure that information in the column(s) is unique i.e. a value entered in column(s) defined in the unique constraint must not be repeated across the column(s). A table may have many unique keys. 

Syntax: CREATE TABLE Table_Name(column_name data_type(size) UNIQUE, ….);
3. CHECK: Specifies a condition that each row in the table must satisfy. To satisfy the constraint, each row in the table must make the condition either TRUE or unknown (due to a null). 

Syntax: CREATE TABLE Table_Name(column_name data_type(size) CHECK(logical expression), ….); 

4. PRIMARY KEY: A field which is used to identify a record uniquely. A column or combination of columns can be created as primary key, which can be used as a reference from other tables. A table contains primary key is known as Master Table.  
It must uniquely identify each record in a table.  
It must contain unique values.  
It cannot be a null field. 
It cannot be a multi port field.  
It should contain a minimum number of fields necessary to be called unique. 

Syntax: CREATE TABLE Table_Name(column_name data_type(size) PRIMARY KEY, ….);

5. FOREIGN KEY: It is a table level constraint. We cannot add this at column level. To reference any primary key column from other table this constraint can be used. The table in which the foreign key is defined is called a detail table. The table that defines the primary key and is referenced by the foreign key is called the master table. 

Syntax: CREATE TABLE Table_Name(column_name data_type(size) FOREIGN KEY(column_name) REFERENCES table_name);

6. DEFAULT : The DEFAULT constraint is used to insert a default value into a column. The default value will be added to all new records, if no other value is specified. 

Syntax: CREATE TABLE Table_Name(col_name1,col_name2,col_name3 DEFAULT ‘’);

### 1.Create a table name as "Students" with the following attributes
![Screenshot 2024-04-23 185111](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/9bf6a267-502f-43eb-a1a5-c2d76fcd6dd9)
#### Query
```
CREATE TABLE Students (
    id integer PRIMARY KEY AUTOINCREMENT,
    first_name VARCHAR(50),
    last_name VARCHAR(50),
    email VARCHAR(100) UNIQUE,
    birth_date DATE
);
```
#### Output
![Screenshot 2024-04-23 185306](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/ea121922-a4f7-4d49-a515-1662f5cf9c1d)

### 2.Write a SQL Query for creating a table name as "Students" with the following attributes
![Screenshot 2024-04-24 131025](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/12778c47-8872-4575-921d-17d8e5f6d1b2)

#### Query
```
CREATE TABLE Students (
    id INTEGER PRIMARY KEY AUTOINCREMENT,
    name varchar(20) NULL,
    address text,
    grades varchar(10),
    phone numeric not null
);
);
```
#### Output
![Screenshot 2024-04-24 131058](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/4508f6de-4dd2-4fbd-9739-18586f84bd67)

### 3.Write a SQL query for creating a table named "Orders" with the following attributes:

OrderID as INTEGER  autoincrement not null (Specify OrderID as the Primary Key).
OrderNumber as INTEGER.
ProductName as Varchar(30)
Manufacturename as varchar(30)
PersonID as INTEGER  not null (Specify PersonID as a Foreign Key referencing the table "Person").
![Screenshot 2024-04-24 131220](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/1abfc347-b28c-459c-8933-7052e86b564b)


#### Query
```
CREATE TABLE Orders (
    OrderID INTEGER PRIMARY KEY AUTOINCREMENT NOT NULL,
    OrderNumber INTEGER,
    ProductName Varchar(30),
    Manufacturename varchar(30),
    PersonID INTEGER NOT NULL,
    FOREIGN KEY (PersonID) REFERENCES Person(PersonID)
);
```
#### Output
![Screenshot 2024-04-24 131310](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/6928f42a-c3f3-4763-92db-fb97bd42b72d)

### 4.Create a table name as "Students" with the following attributes
![Screenshot 2024-04-24 132306](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/63b583f9-0473-429d-8b2d-bdbc67eceea1)

rollno as integeprimarykey with autoincrement
stu_name as varchar(50)
year as varchar(30)
parentsoccupation as varchar(30)
address as varchar(30)
![Screenshot 2024-04-24 132332](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/69873f86-af0d-4b67-a03b-c2498fb63430)

#### Query
```
CREATE TABLE Students (
    rollno INTEGER PRIMARY KEY AUTOINCREMENT,
    stu_name VARCHAR(50),
    year VARCHAR(30),
    parents_occupation VARCHAR(30),
    address VARCHAR(30)
);

```
#### Output
![Screenshot 2024-04-24 132352](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/d0337b8c-c0ed-4043-bb85-8bc14cd3d9be)


### 5.Write a SQL query to Add a new column Mobilenumber as number in the Student_details table.
![Screenshot 2024-04-24 141706](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/5643ebfb-2edd-45db-9ac6-440ac9b98d89)

#### Query
```
ALTER TABLE Student_details
ADD COLUMN Mobilenumber number;
```
#### Output
![Screenshot 2024-04-24 141742](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/79e2301b-e02c-4265-9e52-9fdd1b9effcc)

### 6.Write a SQL Query to Add attribute "birth_date"  in the table employee 
![Screenshot 2024-04-24 141835](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/7b1d050b-3637-43f9-8054-bc499e72ccc9)


#### Query
```
ALTER TABLE employee
ADD COLUMN birth_date date;
```
#### Output
![Screenshot 2024-04-24 141910](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/3bbec5e4-a2eb-47be-9954-ed2cb4170315)

### 7.Write a SQL query to Add a new column named "discount" with the data type DECIMAL(5,2) to the "customer" table. 
![Screenshot 2024-04-24 142025](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/2161440c-e476-4cc8-acf4-6b61fe124efa)


#### Query
```
ALTER TABLE customer
ADD COLUMN discount DECIMAL(5,2);
```
#### Output
![Screenshot 2024-04-24 142100](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/c4e44c78-1926-44cf-8d32-eb196b273891)

### 8.Write an SQL query to insert values into the Student_database table. Set 'rollno' as the primary key with auto-increment, specify other attributes appropriately, and set the 'mark' attribute to null.
![Screenshot 2024-04-24 142231](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/f126559d-e478-4c80-a6ae-08248f0517cf)



#### Query
```
INSERT INTO Student_database (fname, lname, Gender, Subject, MARKS)
VALUES 
    ('Emma', 'Johnson', 'Female', 'Physics', NULL),
    ('Samuel', 'Davis', 'Male', 'Chemistry', NULL),
    ('Ethan', 'Moore', 'Male', 'History', NULL),
    ('Olivia', 'Robinson', 'Female', 'ComputerScience', NULL),
    ('Mason', 'Clark', 'Male', 'English', NULL);

```
#### Output
![Screenshot 2024-04-24 142308](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/afd1254e-227e-4ad7-bb35-f89db6580d5f)

### 9.Write a SQL Query for inserting the below values as multiple row format in the table "Student_database" 
![Screenshot 2024-04-24 142450](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/05843f5a-dd46-4ebc-a8de-b385ce556c00)



#### Query
```
INSERT INTO Student_database (fname, lname, Gender, Subject, MARKS) 
VALUES 
    ('Emma', 'Johnson', 'Female', 'Physics', 95),
    ('Samuel', 'Davis', 'Male', 'Chemistry', 82),
    ('Ethan', 'Moore', 'Male', 'History', 78),
    ('Olivia', 'Robinson', 'Female', 'ComputerScience', 92),
    ('Mason', 'Clark', 'Male', 'English', 85);
```
#### Output
![Screenshot 2024-04-24 142537](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/79aa22aa-4354-4c95-95d7-f3341ffc039e)

### 10.Write a SQL query for inserting new customer details (customer_id, name, email) from the 'old_customers' table into the 'new_customers' table with the subquery. Ensure that only customers name as "James' are included in the transfer.
![Screenshot 2024-04-24 142634](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/0c8590f6-46e8-4676-9e81-28467b5d9945)




#### Query
```
INSERT INTO new_customers (customer_id, name, email)
SELECT customer_id, name, email
FROM old_customers
WHERE name = 'James';

```
#### Output
![Screenshot 2024-04-24 142657](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/879fee14-a413-4869-bea4-c1c170556632)



## Result!
Thus , to study and implement DDL commands and different types of constraints.
