# DBMS-Expt02

## Aim
To learn and practice the uses of Create , Alter and Insert in SQL.

### Create a table name as "Students" with the following attributes
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

### 
## Result
Thus , Create , Alter and Insert in SQL is practiced successfully.
