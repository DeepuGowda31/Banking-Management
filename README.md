##  Banking Management System

# Overview
The Banking Management System is a Java-based application designed to handle basic banking operations.
Users can register, login, open bank accounts, check their balance, and perform transactions such as credit, debit, and transfer of funds.

# Features
User Registration and Login
Opening a New Bank Account
Credit Money to Account
Debit Money from Account
Transfer Money between Accounts
Check Account Balance

# Technologies Used
Java
JDBC
MySQL

## Setup Instructions
# Prerequisites
- Java Development Kit (JDK) installed
- MySQL Database Server installed
- MySQL JDBC Driver added to the project's classpath
- 
# Database Setup
- Create a database named banking.
- Create the following tables within the banking database:

- CREATE TABLE User (
    id INT AUTO_INCREMENT PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);

CREATE TABLE Accounts (
    account_number BIGINT PRIMARY KEY,
    full_name VARCHAR(255) NOT NULL,
    email VARCHAR(255) NOT NULL,
    balance DOUBLE NOT NULL,
    security_pin VARCHAR(255) NOT NULL,
    FOREIGN KEY (email) REFERENCES User(email)
);
