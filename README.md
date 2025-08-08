Dairy Farm Management System
This project is a comprehensive Dairy Farm Management System developed as part of a Database Management Systems (DBMS) academic project. It aims to streamline dairy farm operations by efficiently managing user data, cattle, milk production, vaccination tracking, sales, and more using a relational database model.


📌 Features
•	👥 User management (Farmers, Cow Buyers, etc.)
•	🐮 Cattle registration and categorization
•	🍼 Milk collection & buyer tracking
•	💉 Vaccination monitoring system
•	🐄 Cow sales and sale tracking
•	🌾 Feed monitoring for each cow
•	🧾 ER Diagram, Relational Schema & Normalization up to 3NF
•	🧠 SQL queries for reporting, filtering, and data manipulation


🧱 Tech Stack
Database: PostgreSQL / MySQL
Design: ER Diagrams, Relational Schema, Normalization (1NF → 3NF)
Language: SQL


🗃️ ER Diagram & Schema
Detailed schema includes:
•	User(User_Id , User_Name, User_Category, Street_No, House_No, Pin)
•	User_Contact(User_Id, Contact)
•	Cow(Cow_Id, Gender, Date_Of_Birth, Status)
•	Cow_viewer(User_Id, Cow_Id)
•	Milk_Buyer(User_Id, Milk_Sale_Collection, Litres_Sold, Price_Per_Litre, Date_Recorded)
•	Vaccination(Vaccine_Id, Cow_Id, Date_Recorded)
•	Milk_Collection(Milk_Collection_Id, Date_Recorded, Total_Lit)
•	Produce_Milk_Collection(Cow_Id, Milk_Collection_Id, Date_Recorded, Total_Lit)


Normalization includes:
• 1NF: Eliminated repeating groups
• 2NF: Removed partial dependencies
• 3NF: Removed transitive dependencies


📊 Sample SQL Queries
SELECT * FROM Cow_Sales WHERE Cow_Sale_Amount > 15000;
SELECT User_Id, User_Name FROM UserInfo WHERE User_Id IN (101,102);
SELECT Cow_Id, Gender, Cow_Category_Name FROM Cow_Category JOIN Cow_Information ON Cow_Category.Cow_Category_Id = Cow_Information.Cow_Category_Id;
