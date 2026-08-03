# Week 6 - Amazon Relational Database Service (RDS)

## Overview

Amazon Relational Database Service (Amazon RDS) is a fully managed relational database service that simplifies database setup, operation, scaling, and maintenance in the cloud. It supports multiple database engines, including PostgreSQL, MySQL, MariaDB, Oracle, Microsoft SQL Server, and Amazon Aurora.

Amazon RDS automates routine administrative tasks such as backups, software patching, monitoring, and scaling.

---

## Key Features

- Fully managed relational database service
- Automated backups
- Multi-AZ deployment for high availability
- Read replicas
- Automatic software patching
- Easy scaling of storage and compute
- Monitoring with Amazon CloudWatch

---

## Supported Database Engines

- PostgreSQL
- MySQL
- MariaDB
- Oracle
- Microsoft SQL Server
- Amazon Aurora

---

## Hands-on Lab

### Lab 1: Create an Amazon RDS PostgreSQL Instance

#### Steps Performed

1. Opened the AWS Management Console.
2. Navigated to **Amazon RDS**.
3. Clicked **Create Database**.
4. Selected:
   - Engine: PostgreSQL
   - Template: Free Tier
5. Configured:
   - DB Instance Identifier
   - Master Username
   - Master Password
6. Configured networking and security.
7. Created the database instance.

---

### Lab 2: Launch an EC2 Instance

#### Steps Performed

1. Created an Amazon EC2 instance.
2. Connected to the instance using EC2 Instance Connect.
3. Installed the PostgreSQL client.

---

### Lab 3: Connect EC2 to Amazon RDS

Used the PostgreSQL client to connect to the RDS instance.

Example command:

```bash
psql -h <RDS-ENDPOINT> -U <MASTER-USERNAME> -d postgres
```

Successfully connected to the PostgreSQL database.

---

### Lab 4: Create a Database

Created a new database:

```sql
CREATE DATABASE student;
```

Connected to the database:

```sql
\c student
```

---

### Lab 5: Create a Table and Insert Data

Created a sample table and inserted records.

Example:

```sql
CREATE TABLE students (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100),
    age INT
);
```

Inserted sample records and verified the data using:

```sql
SELECT * FROM students;
```

---

### Lab 6: Connect Using pgAdmin

- Enabled public access for the RDS instance.
- Updated the security group to allow PostgreSQL (Port 5432).
- Connected to the RDS instance using pgAdmin.
- Verified successful database access.

---

## Outcome

Successfully:

- Created an Amazon RDS PostgreSQL instance.
- Connected an EC2 instance to Amazon RDS.
- Created a PostgreSQL database.
- Created tables and inserted data.
- Connected to Amazon RDS using pgAdmin.

---

## Skills Gained

- Creating and managing Amazon RDS databases.
- Connecting EC2 instances to RDS.
- Using PostgreSQL with Amazon RDS.
- Managing databases using pgAdmin.
- Understanding secure database connectivity.

---

## AWS Services Used

- Amazon RDS
- Amazon EC2
- PostgreSQL
- pgAdmin

---

## Key Takeaways

- Amazon RDS simplifies database management by automating routine tasks.
- Security Groups control database access.
- EC2 instances can securely communicate with RDS within the same VPC.
- pgAdmin provides a graphical interface for managing PostgreSQL databases.
