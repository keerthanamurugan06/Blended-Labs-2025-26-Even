# Lab 5 – Build a Database Server (AWS)

## Author

* **Name**: KEERTHANA M
* **Register Number**: 212225040185
* **Date of Submission**: 21-11-26

---

## Objective

The objective of this experiment is to understand how to deploy and configure a database server in AWS. This lab focuses on launching an EC2 instance, installing a database management system (DBMS), configuring basic database settings, creating a sample database, and validating connectivity to the database server.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* An existing VPC and EC2 knowledge (from previous labs)
* Basic knowledge of Linux commands and SQL

---

## Tools Used

* AWS Management Console
* Amazon EC2
* Security Groups
* SSH Client (Terminal / PuTTY)
* MySQL / MariaDB / PostgreSQL (any one)

---

## Tasks Performed

### Task 1: Launch EC2 Instance for Database Server

Launch a new EC2 instance using Amazon Linux 2 AMI. Select an appropriate instance type and configure key pair and security group.

---

### Task 2: Configure Security Group for Database Access

Modify the security group to allow:

* SSH (Port 22) for remote access
* Database port (e.g., MySQL – 3306 or PostgreSQL – 5432)

---

### Task 3: Connect to EC2 Instance

Connect to the EC2 instance using SSH from your local machine.

---

### Task 4: Install Database Server

Install a database server software such as MySQL, MariaDB, or PostgreSQL on the EC2 instance using package manager commands.

---

### Task 5: Start and Configure Database Service

Start the database service and configure basic settings such as root password and user privileges.

---

### Task 6: Create a Sample Database

Create a sample database and a table inside it. Insert a few records into the table.

---

### Task 7: Test Database Connectivity

Test the database server by connecting to it locally or remotely and performing basic SQL queries.

---

## Workflow (Student Explanation)

1. Create RDS Security Group: Create DB Security Group and allow MySQL/Aurora traffic on port 3306 from Web Security Group.

2. Create DB Subnet Group: Create DB-Subnet-Group in Lab VPC using subnets 10.0.1.0/24 and 10.0.3.0/24 across two Availability Zones.

3. Create RDS Database: Launch a MySQL Multi-AZ DB instance named lab-db with username main, password lab-password, and database name lab.

4. Connect Web Application: Copy the RDS endpoint and connect the web application using the database name, username, and password. Test adding, editing, and deleting contacts.

5. Submit and Verify: Submit the lab, check the Grades panel and Submission Report, and then end the lab.

---

## Output Screenshots (Attach 3)

### Screenshot 1: EC2 Instance for Database Server

<img width="1257" height="552" alt="image" src="https://github.com/user-attachments/assets/7b7feb71-1ad2-4d34-a029-12e397b4013a" />


---

### Screenshot 2: Database Service Running
<img width="1262" height="557" alt="image" src="https://github.com/user-attachments/assets/3c96d7e2-cb46-4957-bacb-891c93075f40" />


<img width="1915" height="907" alt="image" src="https://github.com/user-attachments/assets/93b23f30-d310-4853-9bae-6e763dcc384e" />

---

### Screenshot 3: Sample Database and Table
<img width="1130" height="590" alt="image" src="https://github.com/user-attachments/assets/d2eb946f-49fb-43ac-90fa-427924479357" />


<img width="1903" height="903" alt="image" src="https://github.com/user-attachments/assets/9db6433a-5c3f-4911-89ac-26983f7c5b1a" />


---

## Result

This experiment demonstrated how to build a database server in AWS using an EC2 instance. By installing and configuring a DBMS, creating a sample database, and testing connectivity, the fundamentals of hosting and managing a cloud-based database server were underst
