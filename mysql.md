# MySQL

## Database

1. `SHOW DATABASES;` show all databases
2. `CREATE DATABASE [name];` create database

   ```sql
   CREATE DATABASE hello_world;
   CREATE DATABASE `hello world`;
   ```
3. `USE [name];` use database

   ```sql
   USE hello_world;
   USE `hello world`;
   ```
4. `SELECT DATABASE();` show selected database
5. `SHOW VARIABLES LIKE 'datadir';` show data store path

## Table

1. `SHOW TABLES;` show all tables
2. `SHOW CREATE TABLE [name]` show created table
3. `DESC [name];` show datatype in this table
4. `INSERT INTO [name] ([col1],[col2],[col3]) VALUES ([value1],[value2],[value3]),([value1],[value2],[value3]); `insert
5. `UPDATE [name] SET [col1]=[value1],[col2]=[value2] WHERE [col3]=[value3];`update
6. `DELETE FROM [name] WHERE [col1]=[value1] AND [col2]=[value2];`delete
7. `TRUNCATE TABLE [name];` delete the whole table
8. `CREATE TABLE [name] LIKE [name];` clone structure of table
9. create table

* ```sql
  CREATE TABLE [name](
  id INT NOT NULL PRIMARY KEY AUTO_INCREMENT COMMENT 'Primary Key',
  create_time DATETIME COMMENT 'Create Time',
  update_time DATETIME COMMENT 'Update Time',
  [column] VARCHAR(255) COMMENT '',
  [colume] INT(10) DEFAULT NULL,
  [colume] FLOAT(32)
  ) DEFAULT CHARSET UTF8 COMMENT '';
  ```

  datatype:
* Numeric:`TINYINT,SMALLINT,MEDIUMINT,INT,BIGINT,BIT`
* Floating numbers:`DECIMAL,FLOAT,DOUBLE`
* Strings:`CHAR,VARCHAR,BINARY,VARBINARY,BLOB,TEXT,ENUM,SET`
* Json:`JSON`
  constrain:
* primary key(PK):`PRIMARY KEY`
* auto increment:`AUTO_INCREMENT`
* not null:`NOT NULL`
* unique:`UNIQUE`
* default:`DEFAULT NULL`

select table

* `SELECT * FROM [name];` show table all data
* `SELECT [col1],[col2] FROM [name] LIMIT [int];` see specific colume
* `SELECT COUNT(*) FROM [name];` count items
* `SELECT [col] FROM [name] WHERE [col1]=[value1] AND [col2]=[value2];`
* `SELECT [col] FROM [name] WHERE [col1] in ([value1],[value2]);`
* `SELECT [col] FROM [name] WHERE [col1] BETWEEN [value1] AND [value2];`
* `SELECT [col] FROM [name] WHERE [col1] RLIKE [regex];`
* `SELECT [col1],[col2] FROM [name] ORDER BY [col3]; `
* `SELECT SUM([col]),MAX([col]),MIN([col]),AVG([col]) FROM [name] WHERE [col]>200; `
* `SELECT COUNT([col]) FROM [name] GROUP BY [col] HAVING [col];`

## Admin

1. `CREATE USER [user_name]@[host] IDENTIFIED BY [password];` create user ([host]=% login anywhere)
2. `SELECT user,host FROM mysql.user;` see user and host
3. `GRANT [privileges] ON [database_name].[table_name] TO [user_name]`; grant privileges to user. privileges:SELECT,UPDATE,DELETE,ALL
   for all database_name use *
   for all table_name use *
4. `RENAME [user_name]@[host] TO [user_name]@[host];` rename user
5. `ALTER USER [user_name]@[host] IDENTIFIED BY [password];` change password
6. `REVOKE [privileges] ON [database_name].[table_name] TO [user_name];` revoke privileges to user.
7. `DROP USER [user_name]@[host];`Drop user
8. `flush privileges;` refresh privileges
