# SQL

Tables must be created in dbSetup.sql

Use VARCHAR as a data type for strings.

SQL is case sensitive.

<!-- CREATE TABLE -->

CREATE TABLE friends(
    name VARCHAR(100),
    age INT(100),
    born DATETIME DEFAULT CURRENT_TIMESTAMP,
    isStudent BOOLEAN
)