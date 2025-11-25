# Employee-Performance-Evaluation-System

Project Title

Employee Performance Evaluation System



Project Description

A desktop-based application built with Java (Swing) that provides a digital platform where managers can evaluate employee performance, set goals, and provide constructive feedback. Employees can view their evaluations, track goals, and access performance reports and analytics.

Key features:

Performance Evaluation by Managers

Goal Setting and Feedback System

Employee Performance Tracking

Personal Goal Management

Performance Reports and Analytics

Technology Stack

Language: Java

UI: Java Swing (desktop GUI)

Database: MySQL (via JDBC) — mock data is used in the demo code

Build / Run: javac / java (or an IDE like IntelliJ IDEA / Eclipse)

System Workflow Overview

Login: Manager and Employee log into the system.

Performance Evaluation: Managers evaluate employee performance using predefined criteria.

Goal Setting: Managers assign goals with descriptions and target dates.

Feedback: Managers provide ratings and comments.

Performance Tracking: Employees view feedback and progress.

Personal Goals: Employees set and monitor their development goals.

Reports: System generates visual/textual reports for review.

Project Structure (files / classes)
EmployeePerformanceEvaluationSystem/
├── src/
│   ├── Login.java            // Login page (common for manager & employee)
│   ├── SignUp.java           // Sign-up page for new users
│   ├── ManagerDashboard.java // Dashboard for manager
│   ├── EmployeeDashboard.java// Dashboard for employee
│   ├── PerformanceEvaluation.java // Manager input for evaluating employees
│   ├── GoalSetting.java      // Manager sets employee goals
│   ├── Feedback.java         // Manager provides feedback
│   ├── PerformanceReport.java// Generates reports (manager & employee)
│   └── Employee.java         // Employee data model


The demo code included in this README contains two main GUI classes: Login.java and SignUp.java (mock data, no DB). Replace mock data sections with JDBC/MySQL code when integrating with a real database.

How to run (quick start)

Make sure you have JDK (11+) installed and javac/java on PATH.

Create a project folder and place *.java files under src/.

(Optional) If you plan to use MySQL, create the schema and configure JDBC connection strings in a DBHelper or similar class.

Compile:
