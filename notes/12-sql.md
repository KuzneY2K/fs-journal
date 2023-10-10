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

SELECT name FROM FRIENDS WHERE 'isStudent' = true; <= gets all names that has 'isStudent as true'

SELECT name FROM FRIENDS WHERE 'hasJOB' = true AND age < 30; <= gets names for people with jobs and under 30;

SELECT name FROM FRIENDS WHERE name LIKE '%mark%'; <= regex search;

SELECT name FROM friends ORDER BY age; <= can use ASC or DESC

SELECT name FROM friends LIMIT 2; <= offset skips

DELETE FROM friends; <= delete all rows