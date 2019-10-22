# SQL Tutorial
MySQL Database

```
create user 'username'@'localhost' identified by 'password';        # Create User
grant all on *.* to 'username'@'localhost';                         # Grant permission for all
flush privileges;                                                   

set password for 'username'@'localhost' = 'new_password';           # Set new password

create database school;                                             # Create database student                                  
                   
# Create table student with defining the schema 
create table student( 
  student_id int primary key,
  name varchar(20),
  subject varchar(20)
  );

describe student;                                                   # Get the details of student table

alter table student add gpa decimal(3,2);                           # Modify table schema (3 is precision, 2 is scale)
Note: decimal(3.2) ==> -9.99 to 9.99

alter table student drop column gpa;                                # Drop gpa column of student table
drop table student;                                                 # Delete the Table student

insert into student values(1, 'Prasad', "Data Science");            # Insert Data into table (inserted sequentially)
insert into student(student_id, name) values(3, 'Pranit');          # Enter specific info (Here, Subject will be Null)

# Though default sequence has been changed, the value mapping is correct below 
insert into student(subject, student_id, name) values('Physics', 4, 'Pranit');

name varchar(20) not null,                                          # Declare not to be null (is a constraint)
subject varchar(20) unique,                                         # Unique field (can not have duplicate entry)
# Note: Primary Key is by default not null and unique 

name varchar(20) default 'not decided',                             # Declare a default value for name field
student_id int primary key auto_increment                           # Make the field as primary and auto incremental








```
