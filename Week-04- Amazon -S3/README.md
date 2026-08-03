# Week 4 - Amazon Simple Storage Service (S3)

## Overview

Amazon Simple Storage Service (Amazon S3) is a highly scalable object storage service that allows you to store and retrieve any amount of data from anywhere on the web. It is designed for high durability, availability, security, and performance.

Amazon S3 is commonly used for:
- Static website hosting
- Backup and recovery
- Data archiving
- Media storage
- Data lakes
- Application storage

---

## Key Features

- Scalable object storage
- 99.999999999% (11 9's) durability
- High availability
- Secure access with IAM and Bucket Policies
- Versioning support
- Lifecycle management
- Static website hosting
- Multiple storage classes

---

## S3 Storage Classes

| Storage Class | Description | Use Case |
|---------------|-------------|----------|
| S3 Standard | Frequently accessed data | Websites, applications |
| S3 Intelligent-Tiering | Automatically optimizes storage costs | Unknown access patterns |
| S3 Standard-IA | Infrequently accessed data | Backup storage |
| S3 One Zone-IA | Lower-cost infrequent access | Secondary backups |
| S3 Glacier | Low-cost archival storage | Long-term archive |
| S3 Glacier Deep Archive | Lowest-cost archive | Compliance data |

---

## Hands-on Labs

### Lab 1: Create an S3 Bucket

#### Steps Performed

1. Opened the AWS Management Console.
2. Navigated to **Amazon S3**.
3. Clicked **Create Bucket**.
4. Entered a globally unique bucket name.
5. Selected the AWS Region.
6. Created the bucket.

---

### Lab 2: Upload Objects

#### Steps Performed

1. Opened the bucket.
2. Uploaded an **index.html** file.
3. Verified that the file was uploaded successfully.

---

### Lab 3: Enable Static Website Hosting

#### Steps Performed

1. Opened the bucket.
2. Navigated to **Properties**.
3. Enabled **Static Website Hosting**.
4. Configured:
   - Index document: `index.html`
5. Saved the configuration.

---

### Lab 4: Configure Bucket Policy

Configured a bucket policy to allow public read access to the website.

---

### Lab 5: Verify Website Access

- Accessed the S3 Website Endpoint.
- Verified that the static website loaded successfully.

---

## Outcome

Successfully:

- Created an Amazon S3 bucket.
- Uploaded website files.
- Enabled Static Website Hosting.
- Configured bucket permissions.
- Hosted a static website using Amazon S3.

---

## Skills Gained

- Creating and managing Amazon S3 buckets.
- Uploading and organizing objects.
- Configuring Static Website Hosting.
- Managing bucket permissions.
- Understanding object storage concepts.

---

## AWS Services Used

- Amazon S3
- AWS IAM

---

## Key Takeaways

- Amazon S3 is an object storage service.
- Buckets store objects such as files, images, videos, and documents.
- Static websites can be hosted directly from Amazon S3.
- Bucket policies help control access to stored objects.
- Amazon S3 provides secure, durable, and scalable cloud storage.
