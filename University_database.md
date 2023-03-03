# Departments
```sql
create table if not exists Departments
(
    id               serial      not null primary key,
    department_name  varchar(30) not null,
    country          varchar(30)
);
insert into Departments(department_name, country)
values('Civil Engineering', 'USA')
```
![image](https://user-images.githubusercontent.com/122611553/222645642-2071d8cf-3b39-49fb-b684-f2a2b3e44803.png)

# Staff
```sql
create table if not exists Staff
(
    id               serial        not null primary key,
    first_name       varchar(30)   not null,
    last_name        varchar(30)   not null,
    email            varchar(30)   not null,
    gender           varchar(30)   not null,
    phone            varchar(30)   not null,
    birthday         date,
    staff_work       varchar(30)   not null,
    country          varchar(30)

);
insert into Staff(first_name, last_name, email, gender, phone, birthday, staff_work, country)
values ('Sanjar', 'Sharipov', 'Sarvar075', 'Male', 991234567, '12/02/2004', 'Software Engeneering','Tashkent')
```
![image](https://user-images.githubusercontent.com/122611553/222645764-c962cda5-f423-4fc1-9258-4e2506c864dc.png)

# Teacher
```sql
create table if not exists Teacher
(
    id          serial       not null primary key,
    first_name  varchar(30)  not null,
    last_name   varchar(30)  not null,
    phone       varchar(30)  not null,
    birthday    date,
    unversity   varchar(30)  not null,
    subject     varchar(30)  not null,
    country     varchar(30)
);
insert into Teacher(first_name, last_name, phone, birthday, unversity, subject, country)
values ('Harry', 'Semon', 770140404, '08/08/1978', 'WIUT', 'Marketing', 'UK')
```
![image](https://user-images.githubusercontent.com/122611553/222645896-8453a597-d305-487d-813f-2b58267fd7bd.png)

# Student
```sql
create table if not exists Student
(
    id           serial       not null primary key,
    first_name   varchar(30)  not null,
    last_name    varchar(30)  not null,
    email        varchar(30)  not null,
    gender       varchar(30)  not null,
    country      varchar(30)  not null,
    phone        varchar(30)  not null,
    birthday     date         not null,
    unversity    varchar(30)
);
insert into Student(first_name, last_name, email, gender, country, phone, birthday, unversity)
values ('Saidbek', 'Saidmurodov', 'Saidbek101', 'Male', 'Tashkent', 770178008, '20/02/2002', 'TTPU')

```
![image](https://user-images.githubusercontent.com/122611553/222646032-a5faca8f-3d48-418f-884f-3a0b7ff82d88.png)

# Region
```sql
create table if not exists Region
(
    id       serial       not null  primary key,
    country  varchar(30)  not null,
    city     varchar(30)  not null,
    region   varchar(30)  not null
);
insert into Region(country, city, region)
values ('Uzbekistan', 'Tashkent', 'Yunus-obod')
```
![image](https://user-images.githubusercontent.com/122611553/222646183-ea5d0f62-7026-4f51-9e55-574f76a48b8e.png)

