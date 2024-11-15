This project is an E-commerce Database Management System implemented in Python using MySQL. It allows for basic CRUD (Create, Read, Update, Delete) operations on various entities of an e-commerce platform, such as Customers, Products, Orders, Payments, Shipping, Shopping Cart, Reviews, and Categories.

Table of Contents
1. Features
2. Technologies Used
3. Setup and Installation
4. Usage Instructions
5. Database Structure
6. CRUD Operations
7. Future Enhancements
8. License

1. Features
Create, Read, Update, and Delete (CRUD) Operations: Supports full CRUD operations for the database tables.
MySQL Database Integration: Interacts with a MySQL database to store, update, and retrieve records.
Command-Line Interface: User-friendly command-line interface to perform database operations.
Structured and Organized Code: Clear separation of concerns with functions and methods for each operation.
SQL Foreign Key Relationships: Handles relationships between entities (e.g., customers and orders).

2. Technologies Used
Python 3.8+: The application logic is written in Python.
MySQL: Used for the database to store e-commerce records.
MySQL Connector for Python: To establish and interact with the MySQL database.

3. Setup and Installation
3.1. Prerequisites
Python 3.8+ installed on your system.
MySQL server installed and running.
MySQL Connector library for Python
-- pip install mysql-connector-python

3.2. MySQL Database Setup
Open the MySQL command line or any MySQL client.
Create a database named PROJECT:
-- CREATE DATABASE PROJECT;
Grant necessary privileges:
--GRANT ALL PRIVILEGES ON PROJECT.* TO 'root'@'localhost';
Make sure to use your own MySQL password when connecting in the Python script.

3.3. Configure the Python Script
In the EcommerceDatabase class within the Python script, update the MySQL credentials in the constructor:
-- def __init__(self, host='localhost', database='PROJECT', user='root', password='YOUR_PASSWORD'):

3.4. Running the Application
Run the script:
-- python ecommerce_db.py

4. Usage Instructions
4.1. Menu Options
Once the program is started, you will be presented with the following options:
1. Customer
2. Product
3. Orders
4. Payments
5. Shipping
6. Shopping Cart
7. Reviews
8. Category
9. Exit
Select the appropriate entity (e.g., Customer, Product) to perform CRUD operations.
Choose the operation: create, read, update, or delete.

4.2. CRUD Operations
Create: Enter the data for each field to create a new record.
Read: View specific records or all records in a table.
Update: Modify specific records by providing the record ID and the new values for the fields you wish to update.
Delete: Remove a record by specifying the record ID.

4.3. Example Workflow
Select Customer (1) from the main menu.
Choose create to add a new customer.
Provide the necessary details (e.g., First Name, Last Name, Email, etc.).
Repeat similar steps for other entities like Product, Orders, etc.

5. Database Structure
5.1. The following tables are created in the MySQL database:

Customer: Stores customer information.
Category: Stores product categories.
Product: Stores product details.
Orders: Stores order information.
Payments: Stores payment transactions for orders.
Shipping: Stores shipping details for orders.
Shopping_Cart: Stores customer shopping cart items.
Reviews: Stores customer reviews for products.

5.2. Table Relationships
Foreign Keys are used to establish relationships between:
Orders and Customer
Payments and Orders
Shipping and Orders
Product and Category
Reviews and Customer/Product

6. CRUD Operations 
6.1 Create
To create a record in any table, the user is prompted to input values for all fields. Example for creating a Customer:  
-- Enter Customer_ID: 1
Enter First_Name: John
Enter Last_Name: Doe
Enter Email: john.doe@example.com
...

6.2 Read
You can view a specific record or all records. To read a specific customer:
-- Enter Customer_ID: 1
Customer record: (1, 'John', 'Doe', 'john.doe@example.com', ...)

6.3 Update
To update a record, provide the ID of the record you want to modify, followed by the new values for the fields you want to update:
-- Enter Customer_ID: 1
Enter new First_Name (leave blank to keep current): Jonathan
...
Updated Customer record with Customer_ID: 1

6.4 Delete
To delete a record, provide the record ID:
--Enter Customer_ID: 1
Deleted Customer record with Customer_ID: 1

7.Future Enhancements
User Authentication: Add authentication for different roles (e.g., Admin, Customer).
Web Interface: Convert the command-line interface to a web-based interface using Flask or Django.
Auto-Increment IDs: Implement auto-increment for primary key fields to simplify record creation.
Input Validation: Add stricter validation for user inputs, especially for dates and numeric fields

8. License
This project is open-source and available under the MIT License.



#   C S - 4 2 5 - D B O - E - c o m m e r c e - w e b s i t e - p r o j e c t  
 