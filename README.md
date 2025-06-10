# Hotel-Management-System-Updated
# 🏨 Hotel Management System (Java + Swing + MySQL)

This Hotel Management System is a Java desktop application built using the Swing framework and MySQL as the backend. It allows hotel staff to manage rooms, employees, customers, check-ins/check-outs, and view departmental data through an easy-to-use graphical interface.

## ✨ Features

- 🧑 Admin Dashboard with Navigation
- 🛏️ Add and Manage Rooms
- 👥 Add and Manage Employees
- 👨‍💼 View Department Details
- 📝 Customer Check-in and Checkout
- 📊 Customer Information Overview
- 🚗 Driver Management
- 💾 JDBC-based MySQL connectivity

## 🧾 Project Files Overview

| File Name           | Description                            |
|---------------------|----------------------------------------|
| `Dashboard.java`     | Main window with navigation menu       |
| `AddRoom.java`       | Add and manage hotel room data         |
| `AddEmployee.java`   | Add and manage employee data           |
| `Department.java`    | View department details                |
| `CustomerInfo.java`  | View customer booking info             |
| `CheckOut.java`      | Customer checkout operations           |
| `AddDrivers.java`    | Add and manage driver information      |
| `Employee.java`      | Display employee list                  |
| `conn.java`          | Database connection configuration      |

## 🔧 Technologies Used

- Java (JDK 8+)
- Swing (GUI)
- MySQL Database
- JDBC Connector

## 🗃️ Database Schema (Sample)

```sql
CREATE DATABASE HotelDB;

CREATE TABLE room (
    room_number VARCHAR(10) PRIMARY KEY,
    availability VARCHAR(10),
    status VARCHAR(20),
    price INT,
    bed_type VARCHAR(20),
    room_type VARCHAR(20)
);

CREATE TABLE employee (
    id INT PRIMARY KEY AUTO_INCREMENT,
    name VARCHAR(100),
    age INT,
    gender VARCHAR(10),
    job VARCHAR(50),
    salary INT,
    phone VARCHAR(15),
    aadhar VARCHAR(20),
    email VARCHAR(100)
);

CREATE TABLE customer (
    number VARCHAR(10) PRIMARY KEY,
    name VARCHAR(100),
    gender VARCHAR(10),
    country VARCHAR(50),
    room VARCHAR(10),
    status VARCHAR(20),
    deposit INT,
    checkin_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);

-- Add other necessary tables as per functionality
