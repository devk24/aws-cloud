# Week 2 - Amazon EC2 (Elastic Compute Cloud)

## Objective

Learn the basics of Amazon EC2 and understand how to launch and configure an EC2 instance.

---

## Topics Covered

- What is Amazon EC2?
- Why EC2 is used
- EC2 Instance Types
- Ubuntu AMI
- Default VPC
- Key Pair
- Security Groups
- Elastic IP
- EC2 Instance Lifecycle

---

## Hands-on Lab

### Tasks Performed

- Created an EC2 instance using the AWS Management Console.
- Launched an Ubuntu EC2 instance using the default VPC.
- Created a new Key Pair.
- Selected the t2.micro instance type.
- Configured the Security Group to allow SSH (Port 22).
- Verified the EC2 instance reached the Running state.
- Allocated an Elastic IP address.
- Associated the Elastic IP with the EC2 instance.
- Verified the Elastic IP attachment.
- Disassociated and re-associated the Elastic IP.

---

## Key Learnings

- EC2 is a virtual server in AWS.
- Ubuntu is the operating system installed on the EC2 instance.
- A Key Pair is required to securely connect to a Linux EC2 instance.
- Security Groups act as virtual firewalls.
- SSH uses Port 22 to connect to Linux servers.
- Elastic IP provides a static public IP address that can be reattached to an EC2 instance.

---

## Services Used

- Amazon EC2
- Amazon VPC
- Security Groups
- Elastic IP

---

## Interview Notes

### What is EC2?

Amazon EC2 (Elastic Compute Cloud) is a service that provides scalable virtual servers in the AWS Cloud.

### What is a Key Pair?

A Key Pair is used to securely connect to an EC2 instance using SSH.

### What is a Security Group?

A Security Group is a virtual firewall that controls inbound and outbound traffic for an EC2 instance.

### What is an Elastic IP?

An Elastic IP is a static public IPv4 address that can be attached to an EC2 instance.
