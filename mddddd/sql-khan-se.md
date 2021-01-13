# SQL - KhanAcademy


## Text till eleverna

Du ska nu surfa in [https://sv.khanacademy.org/computing/computer-programming/sql/](https://sv.khanacademy.org/computing/computer-programming/sql/)

När du väl är framme klickar du på **Logga in** och väljer där **Logga in med Google**.

Du ska genomföra följande lektioner:
- SQL-grunder
- Avancerade SQL-frågor
- Relationsfrågor i SQL
- Ändra databaser med SQL

Under varje lektion finns det i slutet ett projekt... Dessa hoppar du över!

## Utmaning: Bokdatabasen

### Steg 1

```SQL
CREATE TABLE books (
    id  INTEGER PRIMARY KEY,
    name TEXT,
    rating INTEGER
);
```

### Steg 2

```SQL
INSERT INTO books VALUES (
    1,
    "Liftarens guide till galaxen",
    5
);

INSERT INTO books VALUES (
    2,
    "Restaurangen vid slutet av universum",
    5
);

INSERT INTO books VALUES (
    3,
    "Livet, universum och allting",
    4
);
```

## Utmaning: Box office hits databas

### Steg 1

```SQL
SELECT * FROM movies;
```

### Steg 2

```SQL
SELECT *
FROM movies
WHERE release_year >= 2000
ORDER BY release_year;
```

## Utmaning: TODO lista databasstatistik

### Steg 1

```SQL
INSERT INTO todo_list VALUES (4, "Eat a banana", 3);
```

### Steg 2

```SQL
SELECT SUM(minutes) FROM todo_list;
```

## Utmaning: Karaoke sångväljare

## Steg 1

```SQL
SELECT title FROM songs;
```

## Steg 2

```SQL
SELECT title
FROM songs
WHERE mood="epic" OR released > 1990;
```

## Steg 3

```SQL
SELECT title
FROM songs
WHERE mood="epic" AND released > 1990 AND duration < 240;
```

## Utmaning: Playlistskapare

### Steg 1

```SQL
SELECT title
FROM songs
WHERE artist="Queen";
```

### Steg 2

```SQL
SELECT name
FROM artists
WHERE genre="Pop";
```

### Steg 3

```SQL
SELECT title
FROM songs
WHERE artist
IN(
    SELECT name
    FROM artists
    WHERE genre="Pop"
);
```

## Utmaning: Den "ordrikaste" författaren


### Steg 1

```SQL
SELECT author, SUM(words) AS total_words
FROM books
GROUP BY author
HAVING total_words > 1000000;
```

### Steg 2

```SQL
SELECT author, AVG(words) AS avg_words
FROM books
GROUP BY author
HAVING avg_words > 150000;
```

## Utmaning: Betygsbok

### Steg 1

```SQL
SELECT name,
number_grade,
ROUND(fraction_completed * 100) AS percent_completed
FROM student_grades;
```

### Steg 2

```SQL
SELECT
COUNT(*) AS number_of_students,
CASE
    WHEN number_grade > 90 THEN "A"
    WHEN number_grade > 80 THEN "B"
    WHEN number_grade > 70 THEN "C"
    ELSE "F"
END AS letter_grade
FROM student_grades
GROUP BY letter_grade;
```

## Utmaning: Bobby's Hobbies

### Steg 1

```SQL
INSERT INTO persons (name, age) VALUES ("Bo Ko", 40);
INSERT INTO hobbies (person_id, name) VALUES (6, "walking");
```

### Steg 2

```SQL
SELECT persons.name, hobbies.name
FROM persons
JOIN hobbies
ON persons.id=hobbies.person_id;
```

### Steg 3

```SQL
SELECT persons.name, hobbies.name
FROM persons
JOIN hobbies
ON persons.id=hobbies.person_id
WHERE persons.name="Bobby McBobbyFace";
```

## Utmaning: Kundens order

### Steg 1

```SQL
SELECT
customers.name,
customers.email,
orders.item,
orders.price
FROM customers
LEFT OUTER JOIN orders
ON customers.id=orders.customer_id;
```

### Steg 2

```SQL
SELECT
customers.name,
customers.email,
SUM(price) as orders
FROM customers
LEFT OUTER JOIN orders
ON customers.id = orders.customer_id
GROUP BY name
ORDER BY orders DESC;
```

## Utmaning: Sequels i SQL

### Steg 1

```SQL
SELECT
movies.title AS movietitle,
sequelmovie.title AS sequelmovietitle
FROM movies
LEFT OUTER JOIN movies AS sequelmovie
ON movies.sequel_id=sequelmovie.id;
```

eller

```SQL
SELECT a.title, b.title
FROM movies AS a
LEFT OUTER JOIN movies AS b
ON a.sequel_id = b.id;
```

## Utmaning: FriendBook

### Steg 1

```SQL
SELECT
persons.fullname,
hobbies.name
FROM persons
JOIN hobbies
ON persons.id=hobbies.person_id;
```

### Steg 2

```SQL
SELECT
p1.fullname AS name,
p2.fullname AS friend
FROM friends
JOIN persons p1
ON friends.person1_id=p1.id
JOIN persons p2
ON friends.person2_id=p2.id;
```

## Utmaning: Dynamiska dokument

### Steg 1

```SQL
UPDATE documents
SET author="Jackie Draper"
WHERE author="Jackie Paper";

SELECT * FROM documents;
```

### Steg 2

```SQL
DELETE FROM documents WHERE id=5;

SELECT * FROM documents;
```

## Utmaning: Klädförändringar

### Steg 1

```SQL
ALTER TABLE clothes ADD price real;

SELECT * FROM clothes;
```

### Steg 2

```SQL
UPDATE clothes SET price=10 WHERE id=1;
UPDATE clothes SET price=20 WHERE id=2;
UPDATE clothes SET price=30 WHERE id=3;

SELECT * FROM clothes;
```

### Steg 3

```SQL
INSERT INTO clothes VALUES (4, "pants", "bananapants", 42);

SELECT * FROM clothes;
```
