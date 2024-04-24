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
![Uploading Screenshot 2024-04-24 132352.png…]()





### 
## Result
Thus , Create , Alter and Insert in SQL is practiced successfully.
