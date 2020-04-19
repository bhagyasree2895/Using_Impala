# Using_Impala
Impala project using Big data
## Link to the repo: 
https://github.com/bhagyasree2895/Using_Impala
## Link to Slides:
[Impala Slides](https://docs.google.com/presentation/d/1Ita-HKJDhOsyC20zO5CzF5DQfJGMczMbDxkc5YN6Nio/edit#slide=id.g83a80aaf69_1_0)

![Team members](https://github.com/bhagyasree2895/Using_Impala/blob/master/Team_mates.PNG)

## To start Impala:
- Open the clodera VM and type the command ```impala-shell```
- You can also communicate through Hue Query editor.<br />
Once you enter the VM, open the web browser where you can find Hue. Click on that.
## To see the databases present in Impala:
show databases;

## creating a database
create database new_db;

## creating a table
create table employee (name string, years int);

## loading data into impala
hadoop fs -put input.txt /user/impala/
load data inpath '/user/impala/input.txt' into table employee;

## Describe Statement: Metadata about table "employee" 
describe employee;

## Insert records into "employee" using below insert statements
insert into employee (NAME,years)VALUES ('maneesh',25);
insert into employee (NAME,years)VALUES ('bhagya', 23);
insert into employee (NAME,years)VALUES ('Nikitha', 23);
insert into employee (NAME,years)VALUES (' Nandu', 12);
insert into employee (NAME,years)VALUES (' chaitra', 30);
insert into employee (NAME,years)VALUES (' sushma', 50);
insert into employee (NAME,years)VALUES (' sowmya', 3);
insert into employee (NAME,years)VALUES ('pavan',20);
insert into employee (NAME,years)VALUES ('divya',20);

## Select query:
select name from employee where years>25 order by years; 
select * from employee where years>25 order by years;
## References

https://data-flair.training/blogs/pros-and-cons-of-impala/
https://www.dezyre.com/article/impala-vs-hive-difference-between-sql-on-hadoop-components/180
https://www.dezyre.com/hadoop-tutorial/hadoop-impala-tutorial
https://docs.cloudera.com/documentation/enterprise/5-8-x/topics/introduction.html

