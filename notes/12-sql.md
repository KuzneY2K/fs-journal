# SQL

Tables must be created in dbSetup.sql

Use VARCHAR as a data type for strings.

SQL is case sensitive.

<!-- CREATE TABLE -->

CREATE TABLE friends(
    name VARCHAR(100),
    age INT(100),
    born DATETIME DEFAULT CURRENT_TIMESTAMP,
    isStudent BOOLEAN,
    hasJob BOOLEAN
)

INSERT INTO friends(
    name, age, isStudent, hasJob
)
VALUES(
    'Mark', '24', born, true, false
)

SELECT name, age FROM friends;

SELECT * FROM FRIENDS; <= get all columns

SELECT name FROM FRIENDS WHERE 'isStudent' = true;