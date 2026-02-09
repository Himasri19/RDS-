
AWS RDS
=========
1) What is Database
2) Why we need database
3) On-Prem Database & Challenges
4) What is RDS & Why
5) RDS Setup
6) Connecting with RDS DB Server using MySQL Workbench
7) Conclusion


What is Database ?
===================
Database : It is a software which is used to store the data permanently.
Whatsapp Application -------------> Database
- Text msgs
- Audio files
- Video files
- Documents
=> Every s/w application will use database to store the data permanently.
=> Software applications will use SQL to communicate with databases.
=> SQL stands for Structured Query Language.
SQL
Application ------------> Database
=> Using SQL we can perform CRUD operations in the database.
C -> Create
R -> Retrieve
U -> Update
D -> Delete
=> We have several databases in the market
- Oracle
- MySQL
- SQLServer
- PostGres ....
=> The above databases are called as Relational Databases.
=> Relational databases will store the data using tables.
=> Table represents data using Rows and columns.


Database Setup
=================
=> We can setup database in 2 ways
1) On-Prem Database
2) Cloud Database


Challenges with On-Prem Database
==================================
1) Purchase DB server license
2) Install DB Server s/w
3) Security
4) Network
5) Availability
6) Scalability
7) Backup
8) Adminstration (DBA)
=> To overcome above challenges it is highly recommended to use Cloud Database.
=> If we use cloud database then cloud provider will manage database server for us.
=> AWS RDS service providing cloud databases
=> RDS stands for relational database service in AWS cloud
=> RDS is used to create & manage relational databases
=> RDS is a fully managed service in AWS cloud.
=> RDS works based on "pay as you go" model.


============================
MySQL DB Creation Steps
============================
CREATE DATABASE → STANDARD → ENGINE: MYSQL
You are:
1.Choosing Standard Create
2.Selecting MySQL as database engine
3.So AWS will host a MySQL database for you in the cloud
4.You are selecting Free Tier template (cost-optimized).

====================
Database Details
====================
DB Endpoint
DB username
DB password
DB port
Note : Using above details we can check database connectivity.
=> Once connectivity is successful then we will share database details with
developmen team.
Master username :
Master password :
Endpoint :
Note: Use MySQL Workbench and test database connectivitity. If you are able to
connect that means your RDS Setup is successful.
============================
SQL Queries For Practice
============================
=> Execute below sql queries using workbench
show databases;
use sbidb;
show tables;
## table creation query
create table emp(
eid int(10),
ename varchar(100),
esal int(10)
);
## retrieve records query
select * from emp;
## insert query
insert into emp values(1, 'john', 1000);
insert into emp values(2, 'smith', 2000);
select * from emp;
#### note: once practice completed, delete RDS instance ######
===========
Assigment
===========
1) Connect with RDS DB Server using EC2 Linux VM and execute above sql queries.
### Springboot with RDS Integration : https://www.youtube.com/watch?v=GSu1g9jvFhY
