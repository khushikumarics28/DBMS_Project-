SMART HOSTEL & MESS MANAGEMENT DATABASE
With Billing Transactions
📌 Project Title
Smart Hostel & Mess Management Database with Billing Transactions

👥 Team Members
Hiya – 2410030573
Ishita Chauhan – 2410030636
Janvi Jaiswal – 2410030535
Khushi Kumari – 2410030753
📝 Description
A Smart Hostel and Mess Management Database manages hostel, student, and mess details, and records bills and payment transactions to automate administration and ensure accurate billing.

📄 Abstract
The Smart Hostel and Mess Management Database aims to provide an organized and computerized system to manage hostel and mess operations. It stores information about hostels, students, mess services, billing, and transactions.
Students are assigned to hostels and use mess services. Bills are generated for students and payments are recorded through transactions. This system reduces manual work, avoids data redundancy, and ensures accurate billing and record-keeping.

📚 Contents
ER Diagram
Relational Schema
SQL Table Creation
🛠️ Tools Used
draw.io
MySQL
XAMPP
🧩 Entities and Attributes
1️⃣ HOSTEL
Hostel_ID (Primary Key)
Name
Location
Total_Rooms
Warden
2️⃣ MESS
Mess_ID (Primary Key)
Name
Type
Charge
Timing
3️⃣ STUDENT
Student_ID (Primary Key)
Name
Roll_No
Phone
4️⃣ BILL
Bill_ID (Primary Key)
Date
Amount
Status
5️⃣ TRANSACTION
Trans_ID (Primary Key)
Date
Mode
Amount
🔗 Relationships and Cardinality
1️⃣ HOSTEL accommodates STUDENT
Relationship: accommodates
Cardinality:
One HOSTEL → Many STUDENTS (1 : N)
One STUDENT → One HOSTEL
2️⃣ STUDENT uses MESS
Relationship: uses
Cardinality:
One MESS → Many STUDENTS (1 : N)
One STUDENT → One MESS
3️⃣ STUDENT generates BILL
Relationship: generates
Cardinality:
One STUDENT → Many BILLS (1 : N)
One BILL → One STUDENT
4️⃣ BILL paid through TRANSACTION
Relationship: paid through
Cardinality:
One BILL → Many TRANSACTIONS (1 : N)
One TRANSACTION → One BILL
🗂️ Tables Created in Database
HOSTEL(Hostel_ID, Name, Location, Total_Rooms, Warden)
MESS(Mess_ID, Name, Type, Charge, Timing)
STUDENT(Student_ID, Name, Roll_No, Phone, Hostel_ID, Mess_ID)
BILL(Bill_ID, Date, Amount, Status, Student_ID)
TRANSACTION(Trans_ID, Date, Mode, Amount, Bill_ID)
