# Postgresql cheat sheet

--------------------------
Show server info:
**\conninfo**

Show postgres version:
**show server_version;**

---------------------------

Show current users:
**\du**

Create new user:
**create user <user_name> with password <password>;**

Change user password:
**alter role <user_name> with password <password>**;

Delete user:
drop user <user_name>;

Grant all persmissions on database:
grant all privileges on database <database_name> to <user>;

Revome privileges from the user:
revoke all privileges on database "<database_name>" from <username>;

---------------------------------

Show all databases:
\l

Connect to database:
\c <database_name>

Create database:
create database <database_name>;

Delete database:
drop database <database_name>;

Rename database:
alter database <old_name>
rename to <new_name>;

---------------------------------------

Show all tables:
\dt

Show table's schema:
\d <table_name>

Create table:
create table <table_name>(
    <column_name> type constraints
);

Rename table:
alter table <old_name> 
rename to <new_name>;

Delete table:
drop table <table_name>;

----------------------------------------

Add column:
alter table <table_name>
add <column_name> <type> <constraints>;

Rename column:
alter table <table_name>
rename <column_name>
to <new_name>;

Update column:
alter table <table_name>
alter <column_name> type <data_type> <constraints>;

Delete column:
alter table <table_name>
drop <column_name>;

-----------------------------------------------

Show all data:
select * from <table_name>;

Filter data:
select * from <table_name> 
where <column_name> = > < != AND OR <value>;

Limit rows:
select * from <table_name>
limit <row_number>;

Offset rows:
select * from <table_name>
limit n
offset n;

Order by:
select * from <table_name>  
order by <column_name>;

Check the value in a range:
select * from <table_name>
where <column_name>
between <value> and <value>; 

Check the value in a list of values:
select * from <table_name>
where <column_name> in (value, valuej);

Insert data into all columns:
insert into <table name>
values(<value>, <values>);

Insert data into specific columns:
insert into <table_name> (<column_name>)
values(<value>)

Edit data:
update <table_name>
set <column_name> = <new_value>
where <column_name> = <old_value>;

Delete specific data:
delete from <table_name>
where <column_name> = <value>;

---------------------------------------------

Return the number of rows:
select count(*)
from <table_name>;

Return the sum of values:
select sum(<column_name>)
from <table_name>;

Return the max of values:
select max(<column_name>)
from <table_name>;

Return the min of values:
select min(<column_name>)
from <table_name>;

Return the average of values:
select avg(<column_name>)
from <table_name>;
