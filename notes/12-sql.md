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

SELECT * FROM friends WHERE id = 1;

DELETE FROM friends; <= delete all rows

DELETE FROM hotdogs WHERE id = 5; <= deletes by id

UPDATE friends SET age = 20 WHERE id = 3;

Create database
Name whatever
Go to overview
Look at username and password
Write it down
Next need master connection end point
Go to database
Create new connection

sgroot
LemkmpZQ9Q-a1YLt

SG-mark-sandbox-7903-mysql-master.servers.mongodirector.com <= connection end point

jdbc:mysql://SG-mark-sandbox-7903-mysql-master.servers.mongodirector.com:3306/<your-database-name> <= connection string
