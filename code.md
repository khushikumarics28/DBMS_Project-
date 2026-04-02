### CREATE DATABASE

```sql
CREATE DATABASE hostel_db;
USE hostel_db;
```
### ROOM

```sql
CREATE TABLE ROOM (
    room_no INT PRIMARY KEY,
    room_type VARCHAR(20),
    capacity INT,
    floor INT,
    block VARCHAR(10)
);
```
###  STUDENTS

```sql
CREATE TABLE STUDENTS (
    student_id INT PRIMARY KEY,
    name VARCHAR(50),
    email_id VARCHAR(50),
    phone VARCHAR(15),
    admit_date DATE,
    room_no INT,
    FOREIGN KEY (room_no) REFERENCES ROOM(room_no)
);
```
### HOSTEL_REPRESENTATIVE

```sql
CREATE TABLE HOSTEL_REPRESENTATIVE (
    rep_id INT PRIMARY KEY,
    name VARCHAR(50),
    email_id VARCHAR(50),
    phone VARCHAR(15),
    warden VARCHAR(50)
);
```

### BILLS

```sql
CREATE TABLE BILLS (
    bill_id INT PRIMARY KEY,
    date DATE,
    amount INT,
    duration INT,
    rep_id INT,
    FOREIGN KEY (rep_id) REFERENCES HOSTEL_REPRESENTATIVE(rep_id)
);
```
### TRANSACTION

```sql
CREATE TABLE TRANSACTION (
    trans_id INT PRIMARY KEY,
    amount INT,
    payment_method VARCHAR(20),
    date DATE,
    bill_id INT,
    FOREIGN KEY (bill_id) REFERENCES BILLS(bill_id)
);
```
