# EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands
## AIM :
To create a database and execute DDL queries using SQL.

## DDL (Data Definition Language) :
DDL or Data Definition Language actually consists of the SQL commands that can be used to define the database schema. It simply deals with descriptions of the database schema and is used to create and modify the structure of database objects in the database. DDL is a set of SQL commands used to create, modify, and delete database structures but not data. These commands are normally not used by a general user, who should be accessing the database via an application.

## List of DDL commands :
INSERT : The insert command is used for inserting one or more rows into a database table with specified table column values.

UPDATE : The UPDATE command in SQL is used to modify or change the existing records in a table. If we want to update a particular value, we use the WHERE clause along with the UPDATE clause. If you do not use the WHERE clause, all the rows will be affected.

DELETE : SQL is a part of the Data Manipulation Language, a sub-language of SQL that allows modification of data in databases. This command is used to delete existing records from a table.

## Query :
INSERT: It is used to insert data into a table.

### SQL QUERY :
```
insert into student1 values('saravanakumar',21,'AI-DS');

insert into student1 values('pravinrajj',19,'AI-ML');

insert into student1 values('tharun',20,'ECE');

insert into student1 values('glodsin paul',20,'ECE');

insert into student1 values('naveen',18,'CSE-IOT');
```

### OUTPUT :
![Screenshot 2023-09-28 080649](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/1d20928d-d90a-4d97-8f4c-be8756f08f70)


## Query :
UPDATE: It is used to update existing data within a table.

### SQL QUERY :
```
update student1 set age=21 where name='naveen';
```

### OUTPUT :
![Screenshot 2023-09-28 080844](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/5ddfdc0b-fd36-4b9f-989f-f9ed1b24f452)


## Query :
DELETE: It is used to delete records from a database table.

### SQL QUERY:
```
delete from student1 where name='saravanakumar';
```

### OUTPUT:
![Screenshot 2023-09-28 081017](https://github.com/Saravana-kumar369/EX-2-Data-Manipulation-Language-DML-and-Data-Control-Language-DCL-Commands/assets/117925254/08c26e29-9a55-48be-9041-727ad4356522)


RESULT :
Thus the all the queries got the output and statifies the given question.
