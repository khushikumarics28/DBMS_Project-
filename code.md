<h1 align="center">SMART HOSTEL & MESS MANAGEMENT DATABASE</h1>

## 1. HOSTEL TABLE
```sql
CREATE TABLE HOSTEL (
    Hostel_ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Location VARCHAR(50),
    Total_Rooms INT,
    Warden VARCHAR(50)
) ENGINE=InnoDB;
```


---

## 2. MESS TABLE

```sql
CREATE TABLE MESS (
    Mess_ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Type VARCHAR(30),
    Charge DECIMAL(10,2),
    Timing VARCHAR(30)
) ENGINE=InnoDB;
```

---
## 3. STUDENT TABLE

```sql
CREATE TABLE STUDENT (
    Student_ID INT PRIMARY KEY,
    Name VARCHAR(50),
    Roll_No VARCHAR(20),
    Phone VARCHAR(15),
    Hostel_ID INT,
    Mess_ID INT,
    
    CONSTRAINT fk_hostel
        FOREIGN KEY (Hostel_ID) 
        REFERENCES HOSTEL(Hostel_ID)
        ON DELETE CASCADE
        ON UPDATE CASCADE,
        
    CONSTRAINT fk_mess
        FOREIGN KEY (Mess_ID) 
        REFERENCES MESS(Mess_ID)
        ON DELETE CASCADE
        ON UPDATE CASCADE
) ENGINE=InnoDB;
```

---

## 4. BILL TABLE

```sql
CREATE TABLE BILL (
    Bill_ID INT PRIMARY KEY,
    Bill_Date DATE,
    Amount DECIMAL(10,2),
    Status VARCHAR(20),
    Student_ID INT,
    
    CONSTRAINT fk_student
        FOREIGN KEY (Student_ID)
        REFERENCES STUDENT(Student_ID)
        ON DELETE CASCADE
        ON UPDATE CASCADE
) ENGINE=InnoDB;
```

## 5. TRANSACTION TABLE

```sql
CREATE TABLE PAYMENT_TRANSACTION (
    Trans_ID INT PRIMARY KEY,
    Trans_Date DATE,
    Mode VARCHAR(20),
    Amount DECIMAL(10,2),
    Bill_ID INT,
    
    CONSTRAINT fk_bill
        FOREIGN KEY (Bill_ID)
        REFERENCES BILL(Bill_ID)
        ON DELETE CASCADE
        ON UPDATE CASCADE
) ENGINE=InnoDB;
```