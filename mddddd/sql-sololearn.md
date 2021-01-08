# SQL-SoloLearn

**Tips! Hoppa över "Try it Yourself"**

## Basic Concepts

### Introduction to Databases

**Q: Which of the following is true about a database?**

A: A database is a collection of data

**Q: Tables are made up of:**

A: Columns and rows

**Q: The unique column used to identify the records is called:**

A: Primary Key

**Q: What is the name of the language used in creating & accessing databases?**

A: SQL

### SQL Statements: SELECT

**Q: Drag and drop from the options below to complete the command to list all of the databases.**

```sql
SHOW DATABASES
```

**Q: Drag and drop from the options below to view a list of tables for the currently selected database.**

A: TABLES

**Q: Drag and drop from the options below to view the columns from the 'customers' table**

```sql
SHOW COLUMNS FROM customers
```

**Q: Rearrange the code to select the ''name'' column values from the ''customers'' table.**

```sql
SELECT name FROM customers
```

### SQL Syntax Rules

**Q: Whenever you run multiple queries**

A: Each query must end with a semicolon

**Q: Each query must end with a semicolon**

A: Case insensitive

**Q: Which is true about whitespaces?**

A: Whitespaces and line breaks are ignored

### Selecting Multiple Columns

**Q: Fill in the blanks to select name and city from the "people" table.**

```sql
SELECT name, city FROM people;
```
**Q: Type in the missing symbol to select all of the columns from the ''students'' table.**

```sql
SELECT * FROM students;
```

### DISTINCT and LIMIT

**Q: Drag and drop from the options below to build a query to get distinct results from the ''customers'' table.**

```sql
SELECT DISTINCT state
FROM customers;
```

**Q: Drag and drop from the options below to complete the following statement, which selects five names from ''students''.**

```sql
SELECT name
FROM students
LIMIT 5;
```

**Q: Use LIMIT to select the ''id'' and ''name'' columns from ''customers''. Show 12 results, starting from the fifth.**

```sql
SELECT id, name
FROM customers
LIMIT 4, 12;
```
### Sorting Results

**Q: Fill in the blanks to select the ''address'' from ''customers'', using the fully qualified name for the ''address'' column.**

```sql
SELECT customers.address
FROM customers;
```
**Q: Build a query to select ''name'' and ''city'' from the ''people'' table, and order by the ''id''.**

```sql
SELECT name, city
FROM people
ORDER BY id;
```
**Q: Fill in the blanks to order the query results by ''name'', and then by ''state''.**

```sql
SELECT name, state, address
FROM customers
ORDER BY name, state;
```
### Module 1 Quiz

**Q: A database consists of:**

A: Tables

**Q: Drag and drop from the options below to list the table names.**

```sql
SHOW TABLES;
```
**Q: Why use primary keys?**

A: To guarantee the uniqueness of a row

**Q: Drag and drop from the options below to select distinct names from the ''students'' table, ordered by name.**

```sql
SELECT DISTINCT name
FROM students
ORDER BY name;
```
#### Cakes

```sql
SELECT name, calories
FROM cakes
ORDER BY calories
LIMIT 3;
```

## Filtering, Functions, Subqueries

### The WHERE Statement

**Q:**

```sql
SELECT id, name 
FROM students
WHERE id=23
```
**Q: Fill in the blank to select student names whose id is greater than or equal to 12.**

```sql
SELECT id, name
FROM students
WHERE id >= 12;
```
**Q: Drag and drop from the options below to build a query to select the names of students whose ids are between 13 and 45.**

```sql
SELECT id, name
FROM students
WHERE id BETWEEN 13 AND 45;
```
**Q: Rearrange the code to select all values from the ''people'' table where the city equals to ''Boston''.**

```sql
SELECT *
FROM people
WHERE city='Boston';
```
**Q: Drag and drop from the options below to select customers who live in Hollywood, CA.**

```sql
SELECT * FROM customers
WHERE state = 'CA' AND city = 'Hollywood'
```
**Q: Drag and drop from the options below to select customers who live either in CA or in Boston.**

```sql
SELECT name, state, city
FROM customers
WHERE state='CA' OR city='Boston';
```
**Q: Drag and drop from the options below to select customers whose ids are either 1 or 2, and whose city is ''Boston''.**

```sql
SELECT *
FROM customers
WHERE (id = 1 OR id = 2) AND city = 'Boston'
```
### IN, NOT IN Statements

**Q: Drag and drop from the options below to select users from NY and CA:**

```sql
SELECT *
FROM users
WHERE state='NY' OR state='CA'
```
**Q: Select customers from NY, CA, or NC, using the IN statement.**

```sql
SELECT name, state
FROM customers
WHERE state IN ('CA', 'NY', 'NC')
```
**Q: Drag and drop from the options below to exclude customers from the states CA, NY.**

```sql
SELECT name, state
FROM customers
WHERE state NOT IN ('CA', 'NY', 'NC')
```

### Custom Columns

**Q: What do we call the function used for concatenation?**

A: concat

**Q: Type in the keyword used to create custom columns.**

A: as

**Q: Drag and drop from the options below to select concatenated 'city' and 'state' columns, represented with a new custom column named 'new_address'.**

```sql
SELECT
CONCAT (city, ' ', state) AS new_address
FROM customers;
```
### Functions

**Q: What is the name of the function that converts the text to lowercase?**

A: LOWER

**Q: Drag adn drop from the options below to select average cost from the "items" table.**

```sql
SELECT AVG(cost)
FROM items;
```
**Q: Type in the aggregate function name used to calculate the sum of a column's values.**

A: sum

### Subqueries

**Q: Drag and drop from the options below to select all items from the ''items'' table for which cost is greater than 463. Order the result by cost in descending order.**

```sql
SELECT * FROM items
WHERE cost > 463
ORDER BY cost DESC
```
**Q: Drag and drop from the options below to select all items from the ''items'' table for which the cost is greater than the average of costs. Use a subquery to calculate the average cost.**

```sql
SELECT* FROM items
WHERE cost > (
    SELECT AVG(cost) FROM items
)
```
### LIKE and MIN

**Q: Drag and drop from the options below to search ''boxes'' in the ''name'' column of the ''items'' table.**

```sql
SELECT seller_id
FROM items
WHERE name
LIKE '%boxes'
```
**Q: Drag and drop from the options below to complete the statement, which selects ''name'' and minimum of the "cost'' from ''items'', filtering by name and seller id.**

```sql
SELECT name, MIN(cost)
FROM items
WHERE name
LIKE '%boxes of frogs'
AND seller_id IN (68, 6, 18)
```
### Module 2 Quiz

**Q: Fill in the blanks to select all values from the ''students'' table in which the field ''university'' equals ''MIT''.**

```sql
SELECT *
FROM students
WHERE university='MIT'
```
**Q: Rearrange the code to select students from MIT and Stanford, and order the results by the ''university'' column.**

```sql
SELECT name. university
FROM students
WHERE university
IN ('Stanford', 'MIT')
ORDER BY university;
```
**Q: Which keyword is the correct one for custom columns?**

A: AS

**Q: What is the name of the aggregate function for calculating the sum?**

A: SUM

**Q: Drag and drop from the options below to select name and age from ''students'', where age is greater than the average of all ages. Use a subquery to calculate the average value of age.**

```sql
SELECT name, age
FROM students
WHERE age>(
    SELECT AVG(age)
    FROM students
)
```
#### Apartments

```sql
SELECT *
FROM Apartments 
WHERE price>=(
    SELECT avg(price)
    FROM Apartments
)
AND status='Not rented'
ORDER BY Price
```
## JOIN, Table Operations

### Joining Tables

**Q: What does the Table Join do?**

A: Creates a temporary table with the joined tables' data

**Q: Drag and drop from the options below to select ''id'' from ''students''. Order the results by id, in descending order.**

```sql
SELECT id
FROM students
ORDER BY id DESC
```
**Q: Drag and drop from the options below to complete the following statement, which shows item names and the names of customers who bought the items.**

```SQL
SELECT customers.name, items.names
FROM customers, items
WHERE items.seller_id=customers.id;

```
### Types of Join

**Q: Fill in the blanks to select item names and names of customers who bought the items. Use custom names to shorten the statement.**

```SQL
SELECT ct.name, it.name
FROM
customers AS ct,
items AS it
WHERE it.seller_id=ct.id;
```
**Q: Rearrange the query to select the names of students and the names of the universities where those students study.**

```SQL
SELECT students.name, universities.name
FROM students, universities
WHERE students.university_id=universities.id;
```
**Q: Drag and drop from the options below to outer join the table 'items' with 'customers'.**

```SQL
SELECT customers.name, items.name
FROM customers
LEFT OUTER JOIN items
ON customers.id=seller_id;
```
**Q: Rearrange the code to select student names and all university names (use right join to show all university names).**

```SQL
SELECT students.names. universities.names
FROM students
RIGHT OUTER JOIN universities
ON students.university_id=universities.id
```

### Union

**Q: Drag and drop from the options below to select name, cost, and bids from the ''items'' table. Select only those items whose bids are greater than 123.**

```SQL
SELECT name, cost, bids
FROM items
WHERE bids>123
```
**Q: To perform a union operation:**

A: Columns in the queries must be the same

**Q: Type in the command to unite the query results without removing the duplicates.**

A: union all

### The INSERT Statement

**Q: Drag and drop from the options below to insert the data into the ''students'' table.**

```SQL
INSERT INTO students
VALUES ('John Smith', 'MIT')
```
**Q: Rearrange the code to insert the data into the ''student'' table, using actual column names.**

```SQL
INSERT INTO students (name, university)
VALUES ('Peter Parker', 'Stanford')
```
**Q: When inserting data into a table:**

A: We don't have to insert values for all columns in the table

### UPDATE and DELETE Statements

**Q: Type in the command used to update a table.**

A: update

**Q: Drag and drop from the options below to update the ''students'' table by changing the university's value to ''Stanford'' if the student's name is ''John''.**

```SQL
UPDATE students
SET university='Stanford'
WHERE name='John'
```
**Q: Rearrange the code to update the ''name'' and ''age'' columns of the ''students'' table.**

```SQL
UPDATE students
SET name='Peter', age=32
WHERE id=147
```
**Q: Drag and drop from the options below to delete a row from ''people'' in which the ids falls in the range of 5 to 10.**

```SQL
DELETE FROM people
WHERE id>5 AND id<10;
```
### Creating a Table

**Q: Which choice is the correct command to use when creating a table?**

A: CREATE TABLE

**Q: Type in the keyword used as type for integer numbers.**

A: int

**Q: Type in the keyword used as type for a text in the lesson:**

A: varchar

**Q: Fill in the blanks to define a column named ''some_column'' of type varchar with a size of 50.**

A: some_column varchar(50)

**Q: Drag and drop from the options below to make the ''id'' column a primary key.**

A: PRIMARY KEY (id)

**Q: Drag and drop from the options below to create a table with three columns: ''id'' as a primary key, username and password of type varchar.**

```SQL
CREATE TABLE test (
    id int,
    username varchar(30),
    password varchar(20),
    PRIMARY KEY(id)
);
```
### NOT NULL and AUTO_INCREMENT

**Q: Fill in the missing parts so that the column ''username'' disallows empty values.**

A: username varchar(50) NOT NULL

**Q: Drag and drop from the options below to have the ''id'' column auto increment by one each time a new row is inserted.**

A: id int NOT NULL AUTO_INCREMENT

**Q: Drag and drop from the options below to create a table with an auto incremented and not empty primary key ''id''.**

```SQL
CREATE TABLE test (
    id int NOT NULL AUTO_INCREMENT,
    name varchar(30) NOT NULL,
    PRIMARY KEY (id)
);
```
## Alter, Drop, Rename a Table

**Q: Drag and drop from the options below to add a new column entitled ''specialty'' to the table ''students''.**

```SQL
ALTER TALBE students
ADD specialty varcha(50)
```
**Q: Which choice is the correct command for deleting a table?**

A: DROP TABLE

**Q: Drag and drop from the options below to rename the table ''people'' as ''humans''.**

```SQL
RENAME TABLE people TO humans;
```
### Views

**Q: Which command is used to create a view?**

A: CREATE VIEW

**Q: Drag and drop from the options below to create a view named ''temp'' for students with the highest marks.**

```SQL
CREATE VIEW temp AS SELECT id, name, mark
FROM students
ORDER BY mark
LIMIT 10 DESC;
```
**Q: Which statement in regard to views is correct?**

A: Views are being updated dynamically

### Module 3 Quiz

**Q: Rearrange to select all student names and university names (use left join to show all student names).**

```SQL
SELECT students.names, universities.names
FROM students
LEFT OUTER JOIN universities
ON students.university_id=universities.id;
```
**Q: Drag and drop from the options below to insert a data item into the ''people'' table.**

```SQL
INSERT INTO people
VALUES (
    'John Smith, '1', 22
)
```
**Q: Drag and drop from the options below to update the ''people'' table.**

```SQL
UPDATE people
SET name='Jordan'
WHERE id=147
```
**Q: Fill in the blanks to create a table with two columns: ''id'' as a primary key integer, and ''name'' of type varchar.**

```SQL
>>>> CREATE TABLE id int, name varchar(30), PRIMARY KEY(id);
```
**Q: Rearrange to remove the column ''age'' from the ''people'' table.**

```SQL
ALTER TABLE people
DROP COLUMN age
```
**Q: Which choice is the correct command for changing the name of a table?**

A: RENAME

**Q: Drag and drop from the options below to create a view named ''most_abs'' for the students with the greatest number of absences.**

```SQL
CREATE VIEW most_abs AS SELECT id, name, absences
FROM students
ORDER BY absences
DESC LIMIT 10;
```
**Q: Drag and drop from the options below to delete the table ''students'' from the database.**

```SQL
DROP TABLE students
```
**Q: Drag and drop from the options below to remove the column ''temp'' from the table ''students''.**

```SQL
ALTER TABLE students DROP COLUMN temp
```

#### Zoo

```SQL
INSERT INTO animals VALUES ('Slim', 'Giraffe', 1);

SELECT animals.name, animals.type, countries.country FROM animals, countries WHERE animals.country_id=countries.id order by animals.country_id desc
```
--------------------------------------------
## Challenges

### Challenge 1

**Q: In the "users" table of website logins and passwords, select the first 10 records in the table.**

```SQL
SELECT* FROM users LIMIT 10
```
**Q: Drag and drop from the options below to create the table "users" to store website user logins and passwords.**

```SQL
CREATE TABLE users (id INT NOT NULL AUTO_INCREMENT, login VARCHAR(100), password VARCHAR(100))
```
**Q: Rearrange the query to select all students under age 21. The result should be sorted according to the students' names.**

```SQL
SELECT * FROM students WHERE age < 21 ORDER BY name
```
**Q: Your boss asks you to print the list of the first one hundred customers who have balances greater than $1000 or who are from NY.**

A:

```SQL
SELECT * FROM customers WHERE balance>1000 OR city='NY' LIMIT 100
```
**Q: You need the ages of all bears and lions. The first query shows the ages of bears and birds from zoo1, the other shows the ages of lions and crocodiles from zoo2.**

A:

```SQL
SELECT age FROM zoo1 WHERE animal IN('bear', 'bird')
UNION
SELECT age FROM zzoo2 WHERE animal IN ('lion', 'crocodile');
```
**Q: Drag and drop from the options below to create a list of customers in the form "name is from city".**

A:

```SQL
SELECT CONCAT(name, ' is from ', city) FROM customers;
```

**Q: The zoo administration wants a list of animals whose age is greater than the average age of all of the animals.**

A:

```SQL
SELECT * FROM zoo
WHERE age > (
    SELECT AVG(age)
    FROM zoo
)
```

**Q: There are many wolves in the zoo: black wolf, white wolf, lucky wolf, little wolf. They all have 'wolf' at the end of their names. Print the ages of all of the wolves.**

A:

```SQL
SELECT age FROM zoo
WHERE animal LIKE '%wolf'
```

#### Challenge 2

**Q: Drag and drop from the options below to retrieve all students between the ages of 18 and 22.**

A:

```SQL
SELECT name
FROM students
WHERE BETWEEN age 18 AND 22;
```

**Q: Drag and drop from the options below to update the "students" table to set Jake's university to MIT. His id is 682.**

A:

**Q:**

A:

```SQL
UPDATE students
SET university='MIT'
WHERE id=682
```

**Q: When you inserted "elephant" as a new animal, you forgot to include the elephant's age. Correct this mistake by updating the "zoo" table.**

A:

```SQL
UPDATE zoo
SET age=14
WHERE animal='elephant'
```

**Q: Drag and drop from the options below to update the food_balance to 23 for animals whose age is greater than the average age of the animals.**

A:

```SQL
UPDATE zoo
SET food_balance=23
WHERE age> (
    SELECT AVG(age)
    FROM zoo
)
```

**Q: You need your customer's names, along with the names of the cities in which they live. The names of the cities are stored in a separate table called "cities".**

A:

```SQL
SELECT customers.name, cities.name
FROM customers
RIGHT OUTER JOIN cities
ON cities.id=customers.city_id;
```

**Q: In the university's table containing student data, the students' last names have been omitted. Correct this by adding a new column to the table.**

A:

```SQL
ALTER TABLE students
ADD last_name VARCHAR(100)
```

**Q: Drag and drop from the options below to retrieve from MIT, Stanford, and Harvard the names of all students whose first name is Jake.**

A:

```SQL
SELECT name FROM students
WHERE university
IN ('MIT', 'Stanford', 'Harvard')
AND name='Jake';
```