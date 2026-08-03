# Week 5 - Amazon DynamoDB

## Overview

Amazon DynamoDB is a fully managed NoSQL database service provided by AWS. It delivers fast and predictable performance with seamless scalability. DynamoDB stores data in tables using primary keys and is designed for applications that require low-latency data access.

Amazon DynamoDB is commonly used for:
- Web and mobile applications
- Gaming applications
- IoT applications
- Real-time analytics
- Session management

---

## Key Features

- Fully managed NoSQL database
- High availability and durability
- Automatic scaling
- Low-latency performance
- Serverless architecture
- Built-in security with IAM integration
- Backup and restore support

---

## Key Concepts

### Table
A table is used to store data in DynamoDB.

### Item
An item is a single record in a table.

### Attribute
Attributes are pieces of data stored within an item, similar to columns in a relational database.

### Primary Key

A primary key uniquely identifies each item in a table.

There are two types:
- Partition Key
- Partition Key + Sort Key

---

## Hands-on Lab

### Lab 1: Create a DynamoDB Table

#### Steps Performed

1. Opened the AWS Management Console.
2. Navigated to **Amazon DynamoDB**.
3. Clicked **Create Table**.
4. Configured:
   - Table Name: **Students**
   - Partition Key: **student_id**
5. Selected the default settings.
6. Created the table.

---

### Lab 2: Add Items

#### Steps Performed

Added sample student records to the table.

Example:

| student_id | Name | Age |
|------------|------|-----|
| 101 | Alice | 20 |
| 102 | Bob | 21 |
| 103 | Charlie | 22 |

---

### Lab 3: View Table Data

#### Steps Performed

1. Opened the **Students** table.
2. Navigated to **Explore Table Items**.
3. Verified that the inserted records were displayed successfully.

---

## Outcome

Successfully:

- Created a DynamoDB table.
- Configured the partition key.
- Added sample items.
- Retrieved and verified stored data.

---

## Skills Gained

- Creating DynamoDB tables.
- Understanding NoSQL database concepts.
- Working with partition keys.
- Managing items in DynamoDB.
- Retrieving data from a table.

---

## AWS Services Used

- Amazon DynamoDB

---

## Key Takeaways

- DynamoDB is a fully managed NoSQL database service.
- Data is stored as items within tables.
- Each item is uniquely identified by a primary key.
- DynamoDB automatically scales to meet application demands.
- It is ideal for high-performance, low-latency applications.
