# Week 4 - Amazon Elastic Block Store (EBS)

## Overview

Amazon Elastic Block Store (Amazon EBS) is a block-level storage service designed for use with Amazon EC2 instances. It provides persistent storage that remains available even if the EC2 instance is stopped or restarted.

EBS volumes are commonly used for:
- Operating system storage
- Databases
- Enterprise applications
- File systems
- Backup and recovery

---

## Key Features

- Persistent block storage for EC2
- High availability within an Availability Zone
- Supports snapshots for backup
- Volumes can be resized without losing data
- Multiple volume types for different workloads

---

## EBS Volume Types

| Volume Type | Description | Use Case |
|-------------|-------------|----------|
| gp3 | General Purpose SSD | Most applications |
| io2 | Provisioned IOPS SSD | High-performance databases |
| st1 | Throughput Optimized HDD | Big data, log processing |
| sc1 | Cold HDD | Infrequently accessed data |

---

## Hands-on Lab

### Lab 1: Create an EBS Volume

**Steps Performed**
1. Open the AWS Management Console.
2. Navigate to **EC2**.
3. Select **Elastic Block Store → Volumes**.
4. Click **Create Volume**.
5. Choose:
   - Volume Type: **gp3**
   - Size: **10 GB**
   - Availability Zone: Same as the EC2 instance.
6. Click **Create Volume**.

---

### Lab 2: Attach the Volume

**Steps Performed**
1. Select the newly created volume.
2. Click **Actions → Attach Volume**.
3. Choose the EC2 instance.
4. Attach the volume.

---

### Lab 3: Connect to EC2

Connect to the EC2 instance using EC2 Instance Connect or SSH.

Verify the attached volume:

```bash
lsblk
```

---

### Lab 4: Format the Volume

Create a file system:

```bash
sudo mkfs -t xfs /dev/xvdf
```

---

### Lab 5: Mount the Volume

Create a mount directory:

```bash
sudo mkdir /data
```

Mount the volume:

```bash
sudo mount /dev/xvdf /data
```

Verify:

```bash
df -h
```

---

### Lab 6: Create an EBS Snapshot

**Steps Performed**

1. Open **EC2**.
2. Select **Volumes**.
3. Choose the attached volume.
4. Click **Actions → Create Snapshot**.
5. Provide a description.
6. Click **Create Snapshot**.

---

## Commands Used

```bash
lsblk
sudo mkfs -t xfs /dev/xvdf
sudo mkdir /data
sudo mount /dev/xvdf /data
df -h
```

---

## Outcome

Successfully:

- Created an Amazon EBS volume.
- Attached the volume to an EC2 instance.
- Formatted the volume.
- Mounted the volume to the Linux file system.
- Verified persistent storage.
- Created an EBS snapshot for backup.

---

## Skills Gained

- Understanding Amazon EBS architecture.
- Managing persistent block storage.
- Attaching and mounting storage volumes.
- Creating snapshots for backup and recovery.
- Working with Linux storage management commands.

---

## AWS Services Used

- Amazon EC2
- Amazon Elastic Block Store (EBS)

---

## Key Takeaways

- Amazon EBS provides persistent block storage for EC2 instances.
- EBS volumes are independent of the EC2 instance lifecycle.
- Snapshots enable reliable backup and disaster recovery.
- Selecting the appropriate EBS volume type helps optimize performance and cost.
