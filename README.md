# 📊 Employee Performance Evaluation System



## 📜 Project Overview
The **Employee Performance Evaluation System** is a Java-based desktop application developed to automate and streamline the HR appraisal process. It replaces manual paperwork with a secure, digital platform where managers can evaluate employees, and employees can track their progress, set goals, and submit feedback.

This project was built to demonstrate **Java Swing (GUI)** capabilities integrated with a **MySQL Database** via JDBC.

---

## 🌟 Key Features

### 👨‍💼 For Managers (Admin)
- **Secure Login:** Role-based authentication to prevent unauthorized access.
- **Team Dashboard:** View a real-time roster of all employees and their departments.
- **Performance Evaluation:** Rate employees (1-10) and provide detailed feedback/comments.
- **Data Persistence:** All evaluations are instantly saved to the database.

### 👨‍💻 For Employees (Users)
- **Personal Dashboard:** A dedicated hub displaying the user's profile.
- **Goal Setting:** Create and track professional goals with deadlines and priority levels.
- **Feedback System:** Submit anonymous or signed feedback/complaints to HR.
- **View Reports:** Access past performance reports and manager feedback.

---

## 🛠️ Tech Stack

- **Language:** Java (JDK 24)
- **Frontend:** Java Swing (JFrame, JPanel, JTable)
- **Backend:** MySQL Database
- **Connectivity:** JDBC (Java Database Connectivity)
- **Driver:** MySQL Connector/J 9.5.0
- **Tools:** IntelliJ IDEA, MySQL Workbench

---

## 🗄️ Database Schema

The project uses a database named `employee_system` with the following tables:

| Table Name | Description |
| :--- | :--- |
| **`users`** | Stores Employee IDs, Names, Passwords, Roles, and Departments. |
| **`evaluations`** | Stores performance ratings and feedback from managers. |
| **`goals`** | Stores professional goals set by employees. |
| **`feedback`** | Stores complaints or suggestions submitted by employees. |

---

## ⚙️ Installation & Setup Guide

Follow these steps to run the project on your local machine.

### 1️⃣ Prerequisites
* Java Development Kit (JDK) installed.
* MySQL Server installed and running.
* IntelliJ IDEA (or Eclipse/NetBeans).

### 2️⃣ Database Configuration
1.  Open **MySQL Workbench**.
2.  Copy the SQL script below and run it to set up the database:

```sql
CREATE DATABASE employee_system;
USE employee_system;

-- Create Tables
CREATE TABLE users (empId VARCHAR(20) PRIMARY KEY, name VARCHAR(50), email VARCHAR(50), password VARCHAR(30), role VARCHAR(20), department VARCHAR(30));
CREATE TABLE evaluations (review_id INT AUTO_INCREMENT PRIMARY KEY, empId VARCHAR(20), rating VARCHAR(20), feedback VARCHAR(255), date TIMESTAMP DEFAULT CURRENT_TIMESTAMP);
CREATE TABLE goals (goal_id INT AUTO_INCREMENT PRIMARY KEY, empId VARCHAR(20), title VARCHAR(100), description VARCHAR(255), deadline VARCHAR(20), priority VARCHAR(20), status VARCHAR(20) DEFAULT 'Pending');
CREATE TABLE feedback (feedback_id INT AUTO_INCREMENT PRIMARY KEY, empId VARCHAR(20), type VARCHAR(20), message VARCHAR(255), rating INT, submitted_by VARCHAR(50));

-- Insert Default Admin User
INSERT INTO users VALUES('M001', 'Admin Manager', 'admin@test.com', 'admin123', 'Manager', 'HR');
