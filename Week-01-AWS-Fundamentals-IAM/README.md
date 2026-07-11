# Week 1 - AWS Fundamentals & IAM

## Objective

Learn the fundamentals of AWS Identity and Access Management (IAM), including users, groups, roles, policies, and AWS security best practices.

---

## Topics Covered

- Introduction to AWS
- AWS Global Infrastructure
- IAM (Identity and Access Management)
- IAM Users
- IAM Groups
- IAM Roles
- IAM Policies
- AWS Managed Policies
- Customer Managed Policies
- Principle of Least Privilege
- Multi-Factor Authentication (MFA)

---

## Hands-on Labs

### Lab 1 - Create an IAM User

**Objective**
Create an IAM user with console access.

**Tasks Performed**
- Created user `john`
- Enabled AWS Management Console access
- Forced password reset on first login
- No permissions assigned initially

**Learning**
- IAM User
- Console Login
- Password Policy

---

### Lab 2 - Create an IAM Group

**Tasks Performed**
- Created Developers group
- Attached AmazonS3ReadOnlyAccess
- Added john to Developers group

**Learning**
- IAM Groups
- AWS Managed Policies
- Permission Inheritance

---

### Lab 3 - Create a Custom IAM Policy

**Tasks Performed**
- Created a customer-managed policy
- Allowed:
  - s3:ListBucket
  - s3:GetObject
- Attached policy to Developers group

**Learning**
- JSON Policy
- Effect
- Action
- Resource

---

### Lab 4 - Create an IAM Role

**Tasks Performed**
- Created IAM Role
- Trusted Entity → EC2
- Attached AmazonS3ReadOnlyAccess
- Attached role to EC2 instance

**Learning**
- IAM Roles
- Trusted Entities
- Temporary Credentials

---

### Lab 5 - Enable MFA

**Tasks Performed**
- Enabled MFA for user john
- Verified login using MFA

**Learning**
- Multi-Factor Authentication
- Security Best Practices

---

### Lab 6 - Read-Only Auditor

**Tasks Performed**
- Created auditor user
- Attached ReadOnlyAccess policy
- Verified:
  - Cannot create EC2
  - Cannot delete S3
  - Can view AWS resources

**Learning**
- ReadOnlyAccess
- Permission Testing

---

### Lab 7 - Least Privilege Principle

**Tasks Performed**
- Created custom policy
- Allowed upload and read access
- Restricted access to company-dev-bucket only

**Learning**
- Least Privilege
- Resource-Level Permissions

---

### Lab 8 - Permission Testing

**Tasks Performed**
- Created developer user
- Created tester user
- Verified EC2 permissions

**Learning**
- Permission Validation
- Access Control

---

### Lab 9 - Explicit Deny

**Tasks Performed**
- Allowed Full S3 Access
- Explicitly Denied DeleteObject

**Learning**
- Explicit Deny overrides Allow

---

### Lab 10 - Cross-Team Permissions

**Tasks Performed**
- Created Developers group
- Created Testers group
- Created Admins group
- Assigned users
- Verified permissions

**Learning**
- Role-Based Access Control (RBAC)

---

## Sample IAM Policies Learned

### S3 Read-Only

Allows users to list buckets and read objects.

### S3 Full Access

Allows all S3 actions.

### EC2 Read-Only

Allows viewing EC2 instances and volumes.

---

## Key Concepts Learned

| Concept | Description |
|----------|-------------|
| IAM User | Individual AWS account user |
| IAM Group | Collection of users with shared permissions |
| IAM Policy | JSON document defining permissions |
| IAM Role | Temporary permissions assigned to AWS services or users |
| MFA | Adds an extra authentication layer |
| Least Privilege | Give only the permissions required |
| Managed Policy | Policy created and maintained by AWS |
| Customer Managed Policy | Custom policy created by the customer |

---

## Interview Notes

### What is IAM?

IAM (Identity and Access Management) is an AWS service used to securely manage authentication and authorization for AWS resources.

---

### Difference between User and Role

User
- Permanent identity
- Login credentials
- Used by people

Role
- Temporary credentials
- No password
- Used by AWS services or users

---

### Why use IAM Groups?

Instead of assigning permissions individually, permissions are assigned to a group, and users inherit those permissions.

---

### What is Least Privilege?

Provide only the minimum permissions required to perform a task.

---

### What is Explicit Deny?

If a policy contains an Explicit Deny, it overrides any Allow permissions.
