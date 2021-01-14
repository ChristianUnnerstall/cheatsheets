##### Connect
````
# Connect
mysql -u <username> -p
mysql -u <username> -p <database>
````
##### Databases
````
SHOW DATABASES;             # lists all available databasess
CREATE DATABASE <database>  # create a database
USE <database>              # select databasew databasess;
````
##### Tables
````
SHOW TABLES                 # lists all available tables
DESCRIBE <table>            # show table structure
SHOW INDEX FROM <table>     # list all indexes on a table

# create a table with columns
CREATE TABLE <table> (<column> VARCHAR(100), <anotherColumn> DATETIME);

# adding a column to a table
ALTER TABLE <table> ADD COLUMN <column> VARCHAR(32);
````
##### User
````
# list all users
SELECT user, host FROM mysql.user;

# create user
CREATE USER '<username>'@'localhost' IDENTIFIED BY '<password>';

# grant ALL access to user for all tables
GRANT ALL ON DATABASE.* TO '<username>'@'localhost';
````
