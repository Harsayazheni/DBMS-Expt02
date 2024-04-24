# DBMS-Expt02

## Aim
To learn and practice the uses of Create , Alter and Insert in SQL.

### 1.Create a table name as "Students" with the following attributes
![Screenshot 2024-04-23 185111](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/9bf6a267-502f-43eb-a1a5-c2d76fcd6dd9)
#### Program
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

#### Program
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


#### Program
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

#### Program
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

#### Program
```
ALTER TABLE Student_details
ADD COLUMN Mobilenumber number;
```
#### Output
![Screenshot 2024-04-24 141742](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/79e2301b-e02c-4265-9e52-9fdd1b9effcc)

### 6.Write a SQL Query to Add attribute "birth_date"  in the table employee 
![Screenshot 2024-04-24 141835](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/7b1d050b-3637-43f9-8054-bc499e72ccc9)


#### Program
```
ALTER TABLE employee
ADD COLUMN birth_date date;
```
#### Output
![Screenshot 2024-04-24 141910](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/3bbec5e4-a2eb-47be-9954-ed2cb4170315)

### 7.Write a SQL query to Add a new column named "discount" with the data type DECIMAL(5,2) to the "customer" table. 
![Screenshot 2024-04-24 142025](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/2161440c-e476-4cc8-acf4-6b61fe124efa)


#### Program
```
ALTER TABLE customer
ADD COLUMN discount DECIMAL(5,2);
```
#### Output
![Screenshot 2024-04-24 142100](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/c4e44c78-1926-44cf-8d32-eb196b273891)

### 8.Write an SQL query to insert values into the Student_database table. Set 'rollno' as the primary key with auto-increment, specify other attributes appropriately, and set the 'mark' attribute to null.
![Screenshot 2024-04-24 142231](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/f126559d-e478-4c80-a6ae-08248f0517cf)



#### Program
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



#### Program
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




#### Program
```
INSERT INTO new_customers (customer_id, name, email)
SELECT customer_id, name, email
FROM old_customers
WHERE name = 'James';

```
#### Output
![Screenshot 2024-04-24 142657](https://github.com/Harsayazheni/DBMS-Expt02/assets/118708467/879fee14-a413-4869-bea4-c1c170556632)



## Result!
Thus , Create , Alter and Insert in SQL is practiced successfully.
