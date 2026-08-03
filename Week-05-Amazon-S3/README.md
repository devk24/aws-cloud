# Week 5 - Amazon Simple Storage Service (S3)

## Overview

Amazon Simple Storage Service (Amazon S3) is a scalable object storage service used to store and retrieve any amount of data from anywhere. It is designed for high durability, availability, security, and performance.

Amazon S3 is commonly used for:
- Backup and restore
- Static website hosting
- Data archiving
- Media storage
- Data lakes
- Application storage

---

## Key Features

- Highly durable (99.999999999% durability)
- Virtually unlimited storage
- Secure access using IAM and Bucket Policies
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
| S3 Standard-IA | Infrequently accessed data | Backups |
| S3 One Zone-IA | Lower-cost infrequent access | Secondary backups |
| S3 Glacier Instant Retrieval | Fast archive retrieval | Long-term storage |
| S3 Glacier Flexible Retrieval | Archive storage | Compliance and backup |
| S3 Glacier Deep Archive | Lowest-cost archive | Long-term retention |

---

## Hands-on Lab

### Lab 1: Create an S3 Bucket

### Steps Performed

1. Open the AWS Management Console.
2. Navigate to **Amazon S3**.
3. Click **Create bucket**.
4. Enter a globally unique bucket name.
5. Select the AWS Region.
6. Keep the default settings.
7. Click **Create bucket**.

---

### Lab 2: Upload Objects

### Steps Performed

1. Open the bucket.
2. Click **Upload**.
3. Select files from the local computer.
4. Click **Upload**.

Verified that the objects were uploaded successfully.

---

### Lab 3: Static Website Hosting

### Steps Performed

1. Open the S3 bucket.
2. Go to **Properties**.
3. Enable **Static website hosting**.
4. Specify:
   - Index document: `index.html`
5. Save the configuration.

Uploaded a sample HTML file and accessed the website using the generated endpoint.

---

### Lab 4: Configure Bucket Policy

Configured a bucket policy to allow public read access for the website.

Example policy:

```json
{
  "Version":"2012-10-17",
  "Statement":[
    {
      "Sid":"PublicRead",
      "Effect":"Allow",
      "Principal":"*",
      "Action":"s3:GetObject",
      "Resource":"arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```

---

### Lab 5: Enable Versioning

### Steps Performed

1. Open the bucket.
2. Navigate to **Properties**.
3. Enable **Bucket Versioning**.
4. Save the changes.

---

## Outcome

Successfully:

- Created an Amazon S3 bucket.
- Uploaded objects.
- Enabled Static Website Hosting.
- Hosted a sample website.
- Configured a Bucket Policy.
- Enabled Versioning.

---

## Skills Gained

- Creating and managing S3 buckets.
- Uploading and organizing objects.
- Hosting static websites.
- Managing bucket permissions.
- Understanding storage classes.
- Working with versioning.

---

## AWS Services Used

- Amazon S3
- AWS IAM

---

## Key Takeaways

- Amazon S3 is an object storage service.
- Buckets store objects such as files and folders.
- Static websites can be hosted directly from Amazon S3.
- Bucket Policies control access permissions.
- Versioning protects against accidental deletion and overwrites.
