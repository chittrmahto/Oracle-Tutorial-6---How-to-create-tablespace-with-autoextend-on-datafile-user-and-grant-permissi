# Oracle-Tutorial-6---How-to-create-tablespace-with-autoextend-on-datafile-user-and-grant-permissi
Oracle Tutorial 6 - How to create tablespace (with autoextend on), datafile, user and grant permission to user


Steps: ---
1. Login to your Oracle Database. (sqlplus / as sysdba)
2. run the below commands.

  Check the path of datafiles.
  SQL> select name from v$datafile;

  You ll get the location of datafiles. So i ll create new datafile in same location.
  Here testdb is tablespace name. and also user is testdb. Creating datafile with size 1 GB.

  SQL> CREATE TABLESPACE testdb DATAFILE 'D:\APP\CHIRAG\ORADATA\ORCL\testdb01.dbf' size 1G autoextend on;

Tablespace created. Now creating user for tablespace.

  SQL> create user testdb identified by testdb default tablespace testdb;

User created. Now give the permission to user.
  SQL> grant dba to testdb;

Grant succeeded.

3. Now check in path that 'testdb01.dbf' file is created or not.
  Datafile is created with given size. now check in oracle. file is created.
  
  
  Video URL : https://chittranjanmahto.blogspot.com/2019/08/oracle-tutorial-6-how-to-create.html
