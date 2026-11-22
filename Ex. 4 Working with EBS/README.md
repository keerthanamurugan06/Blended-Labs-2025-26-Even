# Lab 4 – Working with Amazon Elastic Block Store (EBS)

## Author

* **Name**: KEERTHANA M
* **Register Number**: 212225040185
* **Date of Submission**: 22-11-26

---

## Objective

The objective of this experiment is to understand how Amazon Elastic Block Store (EBS) provides persistent block-level storage for EC2 instances. This lab focuses on creating and attaching an EBS volume, formatting and mounting it on an EC2 instance, storing data, and verifying data persistence after instance reboot.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing EC2 instance (Amazon Linux 2 preferred)
* Basic knowledge of Linux commands

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Amazon EBS
* SSH Client (Terminal / PuTTY)

---

## Tasks Performed

### Task 1: Explore Amazon EBS

Explore the Amazon EBS service through the EC2 dashboard. Observe different volume types such as General Purpose SSD (gp2/gp3), Provisioned IOPS SSD, Throughput Optimized HDD, and Cold HDD.

---

### Task 2: Create an EBS Volume

Create a new EBS volume in the same Availability Zone as the EC2 instance. Choose an appropriate size and volume type.

---

### Task 3: Attach EBS Volume to EC2 Instance

Attach the created EBS volume to the running EC2 instance as an additional block device.

---

### Task 4: Format the EBS Volume

Connect to the EC2 instance using SSH and format the attached volume with a file system (for example, ext4).

---

### Task 5: Mount the EBS Volume

Mount the formatted volume to a directory in the EC2 instance (for example, /data or /mnt/ebs).

---

### Task 6: Store Data in EBS Volume

Create files and directories inside the mounted EBS volume and store sample data.

---

### Task 7: Verify Data Persistence

Reboot the EC2 instance and verify that the data stored in the EBS volume is still available after reboot.

---

## Workflow (Student Explanation)

1. Create EBS Volume: Create a 1 GiB General Purpose SSD (gp2) volume in the same Availability Zone as the Lab EC2 instance and tag it My Volume.

2. Attach and Mount Volume: Attach the volume to the Lab EC2 instance using /dev/sdb, connect through Session Manager, and create an ext3 file system.

3. Configure File System: Create /mnt/data-store, mount the volume, configure automatic mounting using /etc/fstab, and create file.txt.

4. Create and Restore Snapshot: Create an EBS snapshot named My Snapshot, delete the original file, and create a new volume named Restored Volume from the snapshot.

5. Verify and Submit: Attach the restored volume using /dev/sdc, mount it at /mnt/data-store2, verify that file.txt is recovered, and submit the lab to check grades.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EBS Volume Created

<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/42de36af-f018-4883-8233-58e986da618c" />


---

### Screenshot 2: EBS Volume Attached to EC2

<img width="1919" height="910" alt="image" src="https://github.com/user-attachments/assets/8bfeeb16-04fc-4a77-91eb-5bcc000f971a" />
<img width="1917" height="948" alt="Screenshot 2026-11-23 011246" src="https://github.com/user-attachments/assets/cc75f0d2-f681-4913-b337-c4330909a5fd" />

<img width="1910" height="945" alt="Screenshot 2026-11-23 010400" src="https://github.com/user-attachments/assets/5f401212-d851-4299-b926-db354c43c71a" />


---

### Screenshot 3: Mounted Volume with Data
<img width="1919" height="848" alt="image" src="https://github.com/user-attachments/assets/d2382d3e-5024-46eb-a89a-0cc58da58d28" />


<img width="1915" height="961" alt="image" src="https://github.com/user-attachments/assets/20441d76-d767-4361-a671-ca3543084df5" />


---

## Result / Conclusion

This experiment demonstrated how Amazon EBS provides persistent storage for EC2 instances. By creating, attaching, formatting, and mounting an EBS volume, and by verifying data after reboot, the concept of durable block storage in the cloud was clearly understood.
