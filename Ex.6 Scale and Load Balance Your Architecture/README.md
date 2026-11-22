# Lab 6 – Scale and Load Balance Your Architecture

## Title

Scale and Load Balance Your Architecture
Author : KEERTHANA M  Reg no : 212225040185  Date : 21-11-26

---

## Objective

The objective of this lab is to understand how to design a scalable and highly available architecture on AWS using Auto Scaling and Elastic Load Balancing. This experiment focuses on distributing incoming traffic across multiple EC2 instances, automatically scaling resources based on demand, and validating fault tolerance.

---

## Prerequisites

* Basic knowledge of Amazon EC2 and VPC
* Completion of previous labs (IAM, EC2, EBS, Database Server)
* AWS Academy Lab access
* Stable internet connection

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Elastic Load Balancer (ELB / ALB)
* Auto Scaling Groups (ASG)
* Amazon CloudWatch

---

## Tasks Performed

### Task 1: Review Existing Architecture

Students review the existing EC2-based application architecture created in previous experiments.

### Task 2: Create a Launch Template

Students create a launch template that defines the EC2 instance configuration including AMI, instance type, security group, and user data.

### Task 3: Create an Auto Scaling Group

Students create an Auto Scaling Group using the launch template and configure minimum, maximum, and desired instance capacity.

### Task 4: Configure an Application Load Balancer

Students create an Application Load Balancer and configure target groups for routing traffic to EC2 instances.

### Task 5: Register Auto Scaling Group with Load Balancer

Students attach the Auto Scaling Group to the target group of the load balancer.

### Task 6: Configure Scaling Policies

Students configure scaling policies based on CPU utilization using Amazon CloudWatch alarms.

### Task 7: Test Load Balancing and Scaling

Students test the setup by generating traffic and observing automatic scaling and load distribution.

---

## Workflow (To be filled by Student)

1. Logged in to the AWS Management Console and reviewed the existing EC2 web server.



2. Created an AMI, target group and Application Load Balancer.



3. Created a launch template and configured an Auto Scaling Group.



4. Attached the Auto Scaling Group to the load balancer and configured a CPU-based scaling policy using CloudWatch.



5. Generated traffic, verified automatic scaling from 2 to 4 healthy instances, terminated the original web server and submitted the lab.

---

## Output Screenshots 
<img width="1912" height="892" alt="image" src="https://github.com/user-attachments/assets/c445e9b1-c674-4e7b-bc9f-a2aece5f5f27" />

<img width="1916" height="910" alt="image" src="https://github.com/user-attachments/assets/9ea26c5f-18c6-493a-bacf-bf40c3f4453c" />

<img width="1912" height="920" alt="image" src="https://github.com/user-attachments/assets/736db979-44d7-42af-83ef-fa9e4eee4a9c" />

---


## Result

This experiment demonstrated how to build a scalable and fault-tolerant cloud architecture using Auto Scaling Groups and Elastic Load Balancing. The system automatically adjusted resources based on workload and ensured continuous service availability by distributing traffic across multiple instances.
