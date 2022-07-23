### terminal commands postgreSQL

`\l` `\d` `\c`

```
psql --username=name dbname=postgres
CREATE DATABASE name_database;
CREATE TABLE name_table();
```

> adds new column to table with INT

```
ALTER TABLE second_table ADD COLUMN first_column INT;
```

//delete a column

```
ALTER TABLE table_name DROP COLUMN column_name;
```

VARCHAR(30)

ALTER TABLE table_name RENAME COLUMN column_name TO new_name;

// values
INSERT INTO table_name(column_1, column_2) VALUES(value1, value2);

DELETE FROM table_name WHERE condition;

DROP TABLE table_name;

ALTER DATABASE database_name RENAME TO new_database_name;

UPDATE table_name SET column_name=new_value WHERE condition;

SELECT columns FROM table_name ORDER BY column_name;

## primary key

It's a column that uniquely identifies each row in the table. Here's an example of how to set a PRIMARY KEY:

ALTER TABLE table_name ADD PRIMARY KEY(column_name);

## drop primary key

ALTER TABLE table_name DROP CONSTRAINT constraint_name;

## foreign key

To know what row a character is for, you need to set a foreign key so you can relate rows from this table to rows from your characters table. Here's an example that creates a column as a foreign key:

ALTER TABLE table_name ADD COLUMN column_name DATATYPE REFERENCES referenced_table_name(referenced_column_name);

## enforce 1to1 relation

ALTER TABLE table_name ADD UNIQUE(column_name);

ALTER TABLE sounds ADD COLUMN character_id INT NOT NULL CONSTRAINT character_id REFERENCES characters(character_id);

Every table should have a primary key. Your previous tables had a single column as a primary key. This one will be different. You can create a primary key from two columns, known as a composite primary key. Here's an example:

ALTER TABLE table_name ADD PRIMARY KEY(column1, column2);

## join 2 tables

You added that as a foreign key, that means you can get all the data from both tables with a JOIN command:

SELECT columns FROM table_1 FULL JOIN table_2 ON table_1.primary_key_column = table_2.foreign_key_column;
