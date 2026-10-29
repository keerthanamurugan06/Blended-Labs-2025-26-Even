# Build Your VPC and Launch a Web Server (AWS) 

## Author

* **Name**: M KEERTHANA
* **Register Number**:212225040185
* **Date of Submission**:29-10-2026

---

## Objective

The objective of this experiment is to understand how to design and configure a basic network infrastructure in AWS using a Virtual Private Cloud (VPC). This lab focuses on creating a VPC with a public subnet, configuring an Internet Gateway and route table, launching an EC2 instance, and hosting a simple web server that can be accessed over the internet.

---

## Prerequisites

* Basic understanding of cloud computing concepts
* AWS account or AWS Academy Lab access
* Web browser with internet connectivity

---

## Tools Used

* AWS Management Console
* Amazon VPC
* Amazon EC2
* Internet Gateway
* Route Table
* Security Groups

---

## Tasks Performed

### Task 1: Create a VPC

Create a new Virtual Private Cloud (VPC) with a private IP address range. The VPC acts as a logically isolated network in AWS where all other resources will be deployed.

Students should create a VPC with an appropriate CIDR block (for example, 10.0.0.0/16) and assign a meaningful name.


### Task 2: Create a Public Subnet

Create a subnet inside the VPC to host public resources. Enable auto-assign public IPv4 so that instances launched in this subnet receive a public IP address.

The subnet should use a smaller CIDR range (for example, 10.0.1.0/24).


### Task 3: Create and Attach Internet Gateway

Create an Internet Gateway (IGW) and attach it to the VPC. This allows communication between resources in the VPC and the internet.


### Task 4: Configure Route Table

Create a route table and add a default route (0.0.0.0/0) pointing to the Internet Gateway. Associate this route table with the public subnet.

This step ensures that traffic from the subnet can reach the internet.


### Task 5: Create Security Group

Create a security group to act as a virtual firewall for the EC2 instance. Configure inbound rules to allow:

SSH on port 22

HTTP on port 80


### Task 6: Launch EC2 Instance

Launch an EC2 instance inside the public subnet using Amazon Linux 2 AMI and a suitable instance type (t2.micro).

Attach the previously created security group and key pair.


### Task 7: Configure Web Server

Install and start a web server (Apache HTTPD) on the EC2 instance using user data or manual commands.

Create a simple HTML page and verify that it can be accessed from a web browser using the public IP address of the instance.---

## Workflow (Student Explanation)

1. Created a VPC named `lab-vpc` with a public subnet, a private subnet, an Internet Gateway, a NAT Gateway, and route tables.

2. Created two additional subnets, `lab-subnet-public2` and `lab-subnet-private2`, in a second Availability Zone and associated them with the appropriate route tables.

3. Created a security group named `Web Security Group` and configured an inbound HTTP rule to allow web traffic on port 80.

4. Launched an EC2 instance named `Web Server 1` using Amazon Linux 2023 and the `t2.micro` instance type. Configured the public subnet, enabled the public IP address, selected the security group, and added a user data script to install Apache and the web application.

5. Verified that the EC2 instance was running and accessed the web application through its public DNS address. Confirmed that the webpage displayed the AWS logo and instance metadata.
---

## Output Screenshots (Attach 3)

### Screenshot 1: VPC and Subnet Details

<img width="1598" height="696" alt="image" src="https://github.com/user-attachments/assets/da452be9-63f4-4ed4-bc1d-3490a5a4aa82" />


---

### Screenshot 2: EC2 Instance Running

<img width="1920" height="1080" alt="Screenshot 2026-10-29 175631" src="https://github.com/user-attachments/assets/ea9046c3-a51b-4a3e-9c25-288ee92f2ffb" />


---

### Screenshot 3: Web Server Output in Browser

<img width="1920" height="1080" alt="Screenshot 2026-10-29 175621" src="https://github.com/user-attachments/assets/d03072a1-33ca-49bc-9db3-503e8ee21945" />


---

## Result 

This experiment successfully demonstrated the creation of a custom VPC and deployment of a public-facing web server in AWS. By configuring networking components such as subnets, route tables, and security groups, and by launching an EC2 instance with a web server, the basic architecture of a cloud-hosted application was understood.
