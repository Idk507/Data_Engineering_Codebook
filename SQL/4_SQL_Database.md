-- 1. SQL Database
-- Concept: A database is a structured collection of data organized into tables, managed by an RDBMS.
-- Use Case: Storing and managing related data, e.g., customer and order data for an e-commerce system.

-- 2. SQL CREATE DB
-- Creates a new database.
-- Syntax: CREATE DATABASE database_name;
CREATE DATABASE ECommerceDB;
-- Result: Creates a database named 'ECommerceDB'.

-- 3. SQL DROP DB
-- Deletes an entire database and all its contents.
-- Syntax: DROP DATABASE database_name;
DROP DATABASE ECommerceDB;
-- Result: Deletes 'ECommerceDB' and all its tables. Use with caution!

-- 4. SQL BACKUP DB
-- Creates a backup of a database (syntax varies by DBMS).
-- Example (SQL Server):
BACKUP DATABASE ECommerceDB
TO DISK = 'C:\Backups\ECommerceDB.bak';
-- Result: Creates a backup file of 'ECommerceDB'.
-- Note: MySQL uses tools like mysqldump, e.g., `mysqldump -u user -p ECommerceDB > backup.sql`

-- 5. SQL CREATE TABLE
-- Creates a new table with defined columns and constraints.
-- Syntax: CREATE TABLE table_name (column1 datatype constraints, ...);
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Email VARCHAR(100) UNIQUE,
    City VARCHAR(50) DEFAULT 'Unknown',
    Age INT CHECK (Age >= 18)
);
-- Result: Creates a 'Customers' table with specified columns and constraints.

-- 6. SQL DROP TABLE
-- Deletes a table and all its data.
-- Syntax: DROP TABLE table_name;
DROP TABLE Customers;
-- Result: Deletes the 'Customers' table and its data.

-- 7. SQL ALTER TABLE
-- Modifies an existing table (add, modify, or drop columns/constraints).
-- Syntax: ALTER TABLE table_name ADD/MODIFY/DROP column_name datatype;
ALTER TABLE Customers
ADD Phone VARCHAR(15);
-- Result: Adds a 'Phone' column to the 'Customers' table.

-- 8. SQL Constraints
-- Rules to enforce data integrity and consistency.
-- Types: NOT NULL, UNIQUE, PRIMARY KEY, FOREIGN KEY, CHECK, DEFAULT.

-- 9. SQL NOT NULL
-- Ensures a column cannot have NULL values.
CREATE TABLE Orders (
    OrderID INT NOT NULL,
    CustomerID INT,
    OrderDate DATE NOT NULL,
    TotalAmount DECIMAL(10,2)
);
-- Result: 'OrderID' and 'OrderDate' cannot be NULL.

-- 10. SQL UNIQUE
-- Ensures all values in a column are unique.
CREATE TABLE Products (
    ProductID INT PRIMARY KEY,
    ProductName VARCHAR(50) UNIQUE,
    Price DECIMAL(10,2)
);
-- Result: 'ProductName' must have unique values (e.g., no two products can have the same name).

-- 11. SQL PRIMARY KEY
-- Uniquely identifies each row; implies NOT NULL and UNIQUE.
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL,
    Email VARCHAR(100)
);
-- Result: 'CustomerID' is the unique identifier for each row.

-- 12. SQL FOREIGN KEY
-- Links a column in one table to the primary key of another, ensuring referential integrity.
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    OrderDate DATE,
    FOREIGN KEY (CustomerID) REFERENCES Customers(CustomerID)
);
-- Result: 'CustomerID' in 'Orders' must match a 'CustomerID' in 'Customers' or be NULL.

-- 13. SQL CHECK
-- Ensures values in a column meet a specific condition.
CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    Name VARCHAR(50),
    Age INT CHECK (Age >= 18)
);
-- Result: 'Age' must be 18 or greater.

-- 14. SQL DEFAULT
-- Sets a default value for a column if no value is provided.
CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    Name VARCHAR(50),
    City VARCHAR(50) DEFAULT 'Unknown'
);
-- Result: If 'City' is not specified during insertion, it defaults to 'Unknown'.

-- 15. SQL INDEX
-- Improves query performance by creating an index on a column.
-- Syntax: CREATE INDEX index_name ON table_name (column);
CREATE INDEX idx_customer_city
ON Customers (City);
-- Result: Speeds up queries filtering or sorting by 'City'.

-- 16. SQL AUTO INCREMENT
-- Automatically generates a unique, sequential value for a column (often used for primary keys).
CREATE TABLE Customers (
    CustomerID INT AUTO_INCREMENT PRIMARY KEY,
    Name VARCHAR(50) NOT NULL
);
-- Result: 'CustomerID' automatically increments (e.g., 1, 2, 3, ...) for each new row.
-- Example Insert:
INSERT INTO Customers (Name) VALUES ('John Doe');
-- Result: Inserts a row with CustomerID = 1.
