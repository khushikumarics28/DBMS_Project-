# ROOM 

```sql
INSERT INTO ROOM VALUES
(101,'Single',1,1,'A'),
(102,'Double',2,1,'A'),
(103,'Triple',3,1,'A'),
(201,'Single',1,2,'B'),
(202,'Double',2,2,'B'),
(203,'Triple',3,2,'B'),
(301,'Single',1,3,'C'),
(302,'Double',2,3,'C'),
(303,'Triple',3,3,'C'),
(304,'Double',2,3,'C');
```
##### output
```
SELECT * FROM ROOM;
+---------+-----------+----------+-------+-------+
| room_no | room_type | capacity | floor | block |
+---------+-----------+----------+-------+-------+
|     101 | Single    |        1 |     1 | A     |
|     102 | Double    |        2 |     1 | A     |
|     103 | Triple    |        3 |     1 | A     |
|     201 | Single    |        1 |     2 | B     |
|     202 | Double    |        2 |     2 | B     |
|     203 | Triple    |        3 |     2 | B     |
|     301 | Single    |        1 |     3 | C     |
|     302 | Double    |        2 |     3 | C     |
|     303 | Triple    |        3 |     3 | C     |
|     304 | Double    |        2 |     3 | C     |
+---------+-----------+----------+-------+-------+
10 rows in set (0.001 sec)
```
# STUDENTS

```
INSERT INTO STUDENTS VALUES
(1,'Aman','aman@gmail.com','9876543210','2024-01-10',101),
(2,'Riya','riya@gmail.com','9876543211','2024-01-11',102),
(3,'Karan','karan@gmail.com','9876543212','2024-01-12',103),
(4,'Neha','neha@gmail.com','9876543213','2024-01-13',201),
(5,'Rahul','rahul@gmail.com','9876543214','2024-01-14',202),
(6,'Priya','priya@gmail.com','9876543215','2024-01-15',203),
(7,'Vikas','vikas@gmail.com','9876543216','2024-01-16',301),
(8,'Anjali','anjali@gmail.com','9876543217','2024-01-17',302),
(9,'Rohit','rohit@gmail.com','9876543218','2024-01-18',303),
(10,'Simran','simran@gmail.com','9876543219','2024-01-19',304);
```
##### output
```
SELECT * FROM STUDENTS;
+------------+--------+------------------+------------+------------+---------+
| student_id | name   | email_id         | phone      | admit_date | room_no |
+------------+--------+------------------+------------+------------+---------+
|          1 | Aman   | aman@gmail.com   | 9876543210 | 2024-01-10 |     101 |
|          2 | Riya   | riya@gmail.com   | 9876543211 | 2024-01-11 |     102 |
|          3 | Karan  | karan@gmail.com  | 9876543212 | 2024-01-12 |     103 |
|          4 | Neha   | neha@gmail.com   | 9876543213 | 2024-01-13 |     201 |
|          5 | Rahul  | rahul@gmail.com  | 9876543214 | 2024-01-14 |     202 |
|          6 | Priya  | priya@gmail.com  | 9876543215 | 2024-01-15 |     203 |
|          7 | Vikas  | vikas@gmail.com  | 9876543216 | 2024-01-16 |     301 |
|          8 | Anjali | anjali@gmail.com | 9876543217 | 2024-01-17 |     302 |
|          9 | Rohit  | rohit@gmail.com  | 9876543218 | 2024-01-18 |     303 |
|         10 | Simran | simran@gmail.com | 9876543219 | 2024-01-19 |     304 |
+------------+--------+------------------+------------+------------+---------+
10 rows in set (0.001 sec)
```
# HOSTEL_REPRESENTATIVE
```
INSERT INTO HOSTEL_REPRESENTATIVE VALUES
(1,'Raj','raj@gmail.com','9999991111','Warden1'),
(2,'Amit','amit@gmail.com','9999991112','Warden2'),
(3,'Suresh','suresh@gmail.com','9999991113','Warden3'),
(4,'Deepak','deepak@gmail.com','9999991114','Warden4'),
(5,'Manoj','manoj@gmail.com','9999991115','Warden5'),
(6,'Ramesh','ramesh@gmail.com','9999991116','Warden6'),
(7,'Nitin','nitin@gmail.com','9999991117','Warden7'),
(8,'Kunal','kunal@gmail.com','9999991118','Warden8'),
(9,'Arjun','arjun@gmail.com','9999991119','Warden9'),
(10,'Vivek','vivek@gmail.com','9999991120','Warden10');
```

##### output
```
SELECT * FROM HOSTEL_REPRESENTATIVE;
+--------+--------+------------------+------------+----------+
| rep_id | name   | email_id         | phone      | warden   |
+--------+--------+------------------+------------+----------+
|      1 | Raj    | raj@gmail.com    | 9999991111 | Warden1  |
|      2 | Amit   | amit@gmail.com   | 9999991112 | Warden2  |
|      3 | Suresh | suresh@gmail.com | 9999991113 | Warden3  |
|      4 | Deepak | deepak@gmail.com | 9999991114 | Warden4  |
|      5 | Manoj  | manoj@gmail.com  | 9999991115 | Warden5  |
|      6 | Ramesh | ramesh@gmail.com | 9999991116 | Warden6  |
|      7 | Nitin  | nitin@gmail.com  | 9999991117 | Warden7  |
|      8 | Kunal  | kunal@gmail.com  | 9999991118 | Warden8  |
|      9 | Arjun  | arjun@gmail.com  | 9999991119 | Warden9  |
|     10 | Vivek  | vivek@gmail.com  | 9999991120 | Warden10 |
+--------+--------+------------------+------------+----------+
10 rows in set (0.001 sec)
```

# BILLS

```sql
INSERT INTO BILLS VALUES
(1,'2024-02-01',5000,30,1),
(2,'2024-02-02',6000,30,2),
(3,'2024-02-03',5500,30,3),
(4,'2024-02-04',5200,30,4),
(5,'2024-02-05',5800,30,5),
(6,'2024-02-06',6100,30,6),
(7,'2024-02-07',5300,30,7),
(8,'2024-02-08',6200,30,8),
(9,'2024-02-09',5400,30,9),
(10,'2024-02-10',5900,30,10);
```
##### output
```
SELECT * FROM BILLS;
+---------+------------+--------+----------+--------+
| bill_id | date       | amount | duration | rep_id |
+---------+------------+--------+----------+--------+
|       1 | 2024-02-01 |   5000 |       30 |      1 |
|       2 | 2024-02-02 |   6000 |       30 |      2 |
|       3 | 2024-02-03 |   5500 |       30 |      3 |
|       4 | 2024-02-04 |   5200 |       30 |      4 |
|       5 | 2024-02-05 |   5800 |       30 |      5 |
|       6 | 2024-02-06 |   6100 |       30 |      6 |
|       7 | 2024-02-07 |   5300 |       30 |      7 |
|       8 | 2024-02-08 |   6200 |       30 |      8 |
|       9 | 2024-02-09 |   5400 |       30 |      9 |
|      10 | 2024-02-10 |   5900 |       30 |     10 |
+---------+------------+--------+----------+--------+
10 rows in set (0.000 sec)
```
# TRANSACTIO

```sql
INSERT INTO TRANSACTION VALUES
(1,5000,'UPI','2024-02-02',1),
(2,6000,'Card','2024-02-03',2),
(3,5500,'Cash','2024-02-04',3),
(4,5200,'UPI','2024-02-05',4),
(5,5800,'Card','2024-02-06',5),
(6,6100,'Cash','2024-02-07',6),
(7,5300,'UPI','2024-02-08',7),
(8,6200,'Card','2024-02-09',8),
(9,5400,'Cash','2024-02-10',9),
(10,5900,'UPI','2024-02-11',10);
```

##### output
```
SELECT * FROM TRANSACTION;
+----------+--------+----------------+------------+---------+
| trans_id | amount | payment_method | date       | bill_id |
+----------+--------+----------------+------------+---------+
|        1 |   5000 | UPI            | 2024-02-02 |       1 |
|        2 |   6000 | Card           | 2024-02-03 |       2 |
|        3 |   5500 | Cash           | 2024-02-04 |       3 |
|        4 |   5200 | UPI            | 2024-02-05 |       4 |
|        5 |   5800 | Card           | 2024-02-06 |       5 |
|        6 |   6100 | Cash           | 2024-02-07 |       6 |
|        7 |   5300 | UPI            | 2024-02-08 |       7 |
|        8 |   6200 | Card           | 2024-02-09 |       8 |
|        9 |   5400 | Cash           | 2024-02-10 |       9 |
|       10 |   5900 | UPI            | 2024-02-11 |      10 |
+----------+--------+----------------+------------+---------+
10 rows in set (0.001 sec)
```
