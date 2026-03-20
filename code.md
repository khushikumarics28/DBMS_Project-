<h1 align="center">SMART HOSTEL & MESS MANAGEMENT DATABASE</h1>

## 1. Hostel Representative

```sql
CREATE TABLE hostel_representative (
    rep_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    phone VARCHAR(15),
    email VARCHAR(100),
    warden VARCHAR(100)
);
```

---

##  2. Room

```sql
CREATE TABLE room (
    room_id INT PRIMARY KEY AUTO_INCREMENT,
    block VARCHAR(50),
    capacity INT,
    room_type VARCHAR(50),
    floor INT
);
```

---
##  3. Student

```sql
CREATE TABLE student (
    student_id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    email VARCHAR(100),
    phone VARCHAR(15),
    admit_date DATE,
    room_id INT,
    
    FOREIGN KEY (room_id) REFERENCES room(room_id)
);
```

---

##  4. Bill

```sql
CREATE TABLE bill (
    bill_id INT PRIMARY KEY AUTO_INCREMENT,
    month VARCHAR(20),
    amount DECIMAL(10,2),
    date DATE,
    duration INT,
    rep_id INT,
    student_id INT,
    
    FOREIGN KEY (rep_id) REFERENCES hostel_representative(rep_id),
    FOREIGN KEY (student_id) REFERENCES student(student_id)
);
``` 

##  5. Transaction

```sql
CREATE TABLE transaction (
    trans_id INT PRIMARY KEY AUTO_INCREMENT,
    amount DECIMAL(10,2),
    mode VARCHAR(50),
    date DATE,
    reference_no VARCHAR(100),
    bill_id INT,
    
    FOREIGN KEY (bill_id) REFERENCES bill(bill_id)
);
```
