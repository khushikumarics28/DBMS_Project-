# SMART HOSTEL MANAGEMENT DATABASE  
## Transactions and Billing System  

---

## 📌 Project Title
**Smart Hostel Management Database (Transactions and Billing System)**

---

## 👥 Team Members
- Hiya – 2410030573  
- Ishita Chauhan – 2410030636  
- Janvi Jaiswal – 2410030535  
- Khushi Kumari – 2410030753  

---

## 📝 Description
The Smart Hostel Management Database is designed to manage hostel operations efficiently by storing and organizing data related to students, rooms, billing, and transactions.  
It focuses on handling billing and payment processes in a structured and automated way.

---

## 📄 Abstract
This project presents a database system for managing hostel activities with a focus on transactions and billing.  
The system stores information about students, room allocation, hostel representatives, bills, and payment transactions.  

Students are allocated rooms, and hostel representatives manage rooms and generate bills.  
Each bill is associated with a student and is paid through transactions.  

The system reduces manual work, improves accuracy, and ensures efficient tracking of payments and records.

---

## 📚 Contents
- ER Diagram  
- Relational Schema  
- SQL Table Creation  

---

## 🛠️ Tools Used
- draw.io  
- MySQL  
- XAMPP  

---

## 🧩 Entities and Attributes

### 1️⃣ STUDENTS
- Student_ID (Primary Key)  
- Name  
- Email_ID  
- Phone  
- Admit_Date  

### 2️⃣ ROOM
- Room_No (Primary Key)  
- Room_Type  
- Capacity  
- Floor  
- Block  

### 3️⃣ HOSTEL_REPRESENTATIVE
- Rep_ID (Primary Key)  
- Name  
- Email_ID  
- Phone  
- Warden  

### 4️⃣ BILLS
- Bill_ID (Primary Key)  
- Date  
- Amount  
- Duration  

### 5️⃣ TRANSACTION
- Trans_ID (Primary Key)  
- Date  
- Amount  
- PaymentMethod  

---

## 🔗 Relationships and Cardinality

### 1️⃣ STUDENTS allocated to ROOM
- Relationship: ALLOCATES  
- Cardinality:  
  - Many STUDENTS → One ROOM (M : 1)  
  - One ROOM → Many STUDENTS  

### 2️⃣ HOSTEL_REPRESENTATIVE manages ROOM
- Relationship: MANAGES  
- Cardinality:  
  - One REPRESENTATIVE → Many ROOMS (1 : M)  

### 3️⃣ HOSTEL_REPRESENTATIVE generates BILLS
- Relationship: GENERATES  
- Cardinality:  
  - One REPRESENTATIVE → Many BILLS (1 : M)  

### 4️⃣ STUDENTS receive BILLS
- Relationship: RECEIVE  
- Cardinality:  
  - One STUDENT → Many BILLS (1 : M)  

### 5️⃣ BILLS paid through TRANSACTION
- Relationship: PAID_THROUGH  
- Cardinality:  
  - One BILL → Many TRANSACTIONS (1 : M)  

---

## 🗂️ Tables Created in Database

1. STUDENTS(Student_ID, Name, Email_ID, Phone, Admit_Date, Room_No)  

2. ROOM(Room_No, Room_Type, Capacity, Floor, Block)  

3. HOSTEL_REPRESENTATIVE(Rep_ID, Name, Email_ID, Phone, Warden)  

4. BILLS(Bill_ID, Date, Amount, Duration, Student_ID, Rep_ID)  

5. TRANSACTION(Trans_ID, Date, Amount, PaymentMethod, Bill_ID)  

---
