# SQL Tutorial
MySQL Database

```
create user 'username'@'localhost' identified by 'password';        # Create User
grant all on *.* to 'username'@'localhost';                         # Grant permission for all
flush privileges;                                                   

set password for 'username'@'localhost' = 'new_password';           # Set new password

create database school;                                             
                                      
create table student( 
  student_id int primary key,
  name varchar(20),
  subject varchar(20)
  );

describe student;                                                   # Get the details of student table
drop table student;                                                 # Delete the Table student






```
