# PROJECT TITLE
Smart Resume Builder & Stock Market Trend Tracker
# PROJECT DESCRIPTION
This project is developed using MongoDB, a NoSQL database that stores data in the form of flexible JSON-like documents. The system consists of two main modules:

🔹 1. Smart Resume Builder

The Resume Builder module is used to store and manage candidate information.
It includes:
Personal details (Name, Email)
Skills (as an array)
Work experience
Purpose:
To maintain structured resume data
To perform operations like adding, updating, viewing, and deleting resumes
To ensure data correctness using validation rules

🔹 2. Stock Market Trend Tracker

This module stores and tracks stock-related data.
It includes:
Company name
Stock price
Date of record
Trend (UP / DOWN / STABLE)
Purpose:
To analyze stock performance
To filter stocks based on trends
To maintain historical records of stock prices
# TECHNOLOGIES USED
MongoDB → Database
Mongo Shell (mongosh) → Query execution
JavaScript-based queries → Used for database operations
# EXPLANATION OF TASKS 
 1. Creation 
What is done:
A database named smartProjectDB is created
Two collections are created:
resumes
stocks
Why:
Collections are used to store related data
Separating resume and stock data improves organization
 2. Insertion 

What is done:

Data is inserted using:
insertOne() → inserts a single document
insertMany() → inserts multiple documents
Example:
Resume data (name, skills, etc.)
Stock data (company, price, trend)
Why:
To populate the database with real-world data
Helps in testing queries and operations
3. CRUD Operations
CRUD = Create, Read, Update, Delete

🔸 CREATE
Done using insertOne() and insertMany()

🔸 READ
Using find()
Example:
View all resumes
Filter stocks with trend = "UP"
 Purpose:
Retrieve and analyze stored data

🔸 UPDATE
Using updateOne()
Example:
Updating experience of a candidate
Changing stock trend
 Purpose:
Modify existing data without deleting it

🔸 DELETE
Using deleteOne()
Example:
Remove a resume
Remove stock data
 Purpose:
Maintain clean and relevant database

 4. Validation & Verification 

🔹 Validation

Validation is implemented using JSON Schema in MongoDB.
In Resume Collection:
name → must be string
email → must follow email format
skills → must be an array
experience → must be non-negative
In Stock Collection:
company → string
price → must be positive
date → must be a valid date
trend → only allowed values:
"UP"
"DOWN"
"STABLE"

🔹 Why Validation is Important:
Prevents wrong data entry
Maintains data consistency
Improves reliability of the system

🔹 Verification
Verification is done by:
Running queries like find() to check inserted data
Ensuring updates are applied correctly
Confirming deleted data is removed
# KEY FEATURES
Structured resume storage

Stock trend analysis

Full CRUD functionality

Strong data validation

Easy data retrieval and filtering

Scalable NoSQL design

# CONCLUSION
This project demonstrates the effective use of MongoDB for real-world applications. It highlights how NoSQL databases can be used to manage structured and semi-structured data efficiently while ensuring data accuracy through validation.
