# Lab 3 – Introduction to Amazon Elastic Compute Cloud (EC2)

## Author

* **Name**: KEERTHANA M
* **Register Number**: 212225040185
* **Date of Submission**: 21-11-26

---

## Objective

The objective of this experiment is to understand the fundamentals of Amazon Elastic Compute Cloud (EC2). This lab focuses on launching and managing a virtual server, understanding instance types and AMIs, connecting to an EC2 instance, monitoring its status, and performing basic instance operations such as start, stop, and terminate.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity
* Basic knowledge of Linux commands (optional)

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Key Pair
* Security Group
* SSH Client (PuTTY / Terminal)

---

## Tasks Performed

### Task 1: Explore Amazon EC2 Dashboard

Explore the EC2 service dashboard in the AWS Management Console. Observe the different sections such as Instances, AMIs, Instance Types, Key Pairs, Security Groups, and Elastic IPs.

---

### Task 2: Launch an EC2 Instance

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type (t2.micro) under the free tier. Configure basic settings such as instance name, key pair, and security group.

---

### Task 3: Configure Security Group

Configure a security group to allow inbound access:

* SSH (Port 22) from your IP address
* HTTP (Port 80) from anywhere (0.0.0.0/0)

This security group acts as a firewall for the instance.

---

### Task 4: Connect to EC2 Instance

Connect to the running EC2 instance using SSH. Use the downloaded key pair and connect via terminal or PuTTY.

For Amazon Linux:

```
ssh -i "keyname.pem" ec2-user@<Public-IP>
```

---

### Task 5: Perform Basic Instance Operations

Perform the following operations from the EC2 console:

* Stop the instance
* Start the instance
* Reboot the instance

Observe the state changes of the instance.

---

### Task 6: Monitor EC2 Instance

Monitor the EC2 instance using the Monitoring tab. Observe metrics such as CPU utilization, network in/out, and instance status checks.

---

### Task 7: Terminate EC2 Instance

Terminate the EC2 instance after completing the experiment to avoid unnecessary AWS charges.

---

## Workflow (Student Explanation)
1. Launch an EC2 instance named Web Server.



2. Check instance status, monitoring, system log and screenshot.



3. Add HTTP rule and access the web server using its public IP.



4. Change instance type to t2.small and increase storage to 10 GiB.



5. Test stop protection, stop the instance and submit the lab.
---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Dashboard / Instance List

<img width="1919" height="982" alt="image" src="https://github.com/user-attachments/assets/52ddeb3f-3e59-4a08-b0f9-612aa9e0ac25" />


---

### Screenshot 2: SSH Connection to Instance

<img width="1919" height="982" alt="image" src="https://github.com/user-attachments/assets/91aa7877-6823-41e9-8852-0f243bef0e9d" />
<img width="1424" height="917" alt="image" src="https://github.com/user-attachments/assets/8cc889e1-6152-4c6b-8db6-c35313e34156" />

---

### Screenshot 3: Instance Monitoring / Status

<img width="1919" height="925" alt="image" src="https://github.com/user-attachments/assets/3ad5ac79-f145-4852-a174-3abede450c83" />
<img width="1905" height="946" alt="image" src="https://github.com/user-attachments/assets/5a17f04a-1d5c-49fc-889b-c2cc19d1669f" />

---

## Result 

This experiment provided hands-on experience with Amazon EC2 by demonstrating how to launch, connect, manage, and monitor a virtual server in AWS. It helped in understanding the concept of Infrastructure as a Service (IaaS) and how compute resources can be provisioned and controlled on demand in the cloud.
