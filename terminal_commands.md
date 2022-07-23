### postgreSQL 

\l    \d    \c


psql --username=name dbname=postgres
CREATE DATABASE name_database;
CREATE TABLE name_table();

//adds new table
ALTER TABLE second_table ADD COLUMN first_column INT; 


//delete a column
ALTER TABLE table_name DROP COLUMN column_name;


VARCHAR(30)

ALTER TABLE table_name RENAME COLUMN column_name TO new_name;


// values
INSERT INTO table_name(column_1, column_2) VALUES(value1, value2);

DELETE FROM table_name WHERE condition;

DROP TABLE table_name;

ALTER DATABASE database_name RENAME TO new_database_name;

UPDATE table_name SET column_name=new_value WHERE condition;
