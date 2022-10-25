mysql> use homework12;
Database changed
mysql> show tables;
+----------------------+
| Tables_in_homework12 |
+----------------------+
| movies               |
+----------------------+
1 row in set (0.00 sec)

mysql> describe movies;
+----------+--------------+------+-----+---------+----------------+
| Field    | Type         | Null | Key | Default | Extra          |
+----------+--------------+------+-----+---------+----------------+
| id       | int unsigned | NO   | PRI | NULL    | auto_increment |
| title    | varchar(20)  | NO   |     |         |                |
| genre    | varchar(100) | NO   |     |         |                |
| duration | int unsigned | NO   |     | 0       |                |
+----------+--------------+------+-----+---------+----------------+
4 rows in set (0.00 sec)

mysql> insert info movies(title, genre, duration) values('Metropolis', 'Sci-Fi', 153);
ERROR 1064 (42000): You have an error in your SQL syntax; check the manual that corresponds to your MySQL server version for the right syntax to use near 'movies(title, genre, duration) values('Metropolis', 'Sci-Fi', 153)' at line 1
mysql> insert into movies(title, genre, duration) values('Metropolis', 'Sci-Fi', 153);
Query OK, 1 row affected (0.01 sec)

mysql> select * from movies
    -> ;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
+----+------------+--------+----------+
1 row in set (0.00 sec)

mysql> insert into movies(title, genre, duration) values('Nosferatu', 'Horror', 94);
Query OK, 1 row affected (0.01 sec)

mysql> select * from movies;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
|  2 | Nosferatu  | Horror |       94 |
+----+------------+--------+----------+
2 rows in set (0.00 sec)

mysql> insert into movies(title, genre, duration) values('The Kid', 'Comedy', 68)
    -> ;
Query OK, 1 row affected (0.01 sec)

mysql> select * from movies;
+----+------------+--------+----------+
| id | title      | genre  | duration |
+----+------------+--------+----------+
|  1 | Metropolis | Sci-Fi |      153 |
|  2 | Nosferatu  | Horror |       94 |
|  3 | The Kid    | Comedy |       68 |
+----+------------+--------+----------+
3 rows in set (0.00 sec)

mysql> insert into movies(title, genre, duration) values('The Gold Rush', 'Adventure', 95)
    -> ;
Query OK, 1 row affected (0.01 sec)

mysql> select * from movies;
+----+---------------+-----------+----------+
| id | title         | genre     | duration |
+----+---------------+-----------+----------+
|  1 | Metropolis    | Sci-Fi    |      153 |
|  2 | Nosferatu     | Horror    |       94 |
|  3 | The Kid       | Comedy    |       68 |
|  4 | The Gold Rush | Adventure |       95 |
+----+---------------+-----------+----------+
4 rows in set (0.00 sec)
