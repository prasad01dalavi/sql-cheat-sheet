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

# Few Constraints
name varchar(20) not null,                                          # Declare not to be null
subject varchar(20) unique,                                         # Unique field (can not have duplicate entry)
# Note: Primary Key is by default not null and unique 

name varchar(20) default 'not decided',                             # Declare a default value for name field
student_id int primary key auto_increment                           # Make the field as primary and auto incremental

describe student;                                                   # Get the schema details of student table

alter table student add gpa decimal(3,2);                           # Modify table schema (3 is precision, 2 is scale)
Note: decimal(3.2) ==> -9.99 to 9.99

alter table student drop column gpa;                                # Drop gpa column of student table
drop table student;                                                 # Delete the Table student

insert into student values(1, 'Prasad', "Data Science");            # Insert Data into table (inserted sequentially)
insert into student(student_id, name) values(3, 'Pranit');          # Enter specific info (Here, Subject will be Null)

# Though default sequence has been changed, the value mapping is correct below 
insert into student(subject, student_id, name) values('Physics', 4, 'Pranit');

update student set subject='DS' where subject='Data Science';       # Update the value in row from Data Science to DS

# sudo update syntax
where subject='Data Science' OR subject='Biology' ;                 # Check any of the condition and set the value
set name='Tom', subject='CS' where student_id=1;                    # set name and subject where student id = 1
set subject='CS';                                                   # Set all record field value to CS

delete from student;                                                # Delete all records of student table
delete from student where name='Prasad';                            # Delete the matched record

select column_name from table;                                      # Get column info (* to get all info)
select subject, name from student order by subject desc;            # Get two columns by descending order of subject 
select * from student order by student_id desc limit 1;             # Get only 1 row also order student_id by desc
select name from student where subject = 'Python';                  # Get specific rows  (other sudo logics are also applied)









```
