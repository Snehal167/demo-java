🚀 Java Student Management System – AWS 3-Tier Deployment

!AWS !Java !MySQL !Architecture

📌 Project Overview

This project demonstrates the deployment of a Java-based Student Management System using AWS cloud infrastructure.

The application allows users to register, view, edit, and delete student records. It uses a MySQL database hosted on Amazon RDS and a Java application deployed on an Amazon EC2 instance.

The infrastructure was configured using a custom AWS VPC with public and private subnets, an Internet Gateway, and a NAT Gateway.

Project successfully deployed and tested on AWS.

🏗️ AWS Infrastructure Architecture
VPC Configuration
Component	Configuration
VPC Name	three-tier-vpc
VPC CIDR	10.0.0.0/16
AWS Region	us-east-1 (N. Virginia)
Public Subnet	10.0.0.0/20
Private Subnet 1	10.0.16.0/20
Private Subnet 2	10.0.32.0/20
Internet Gateway	my-ig
NAT Gateway	nat-gtw
Private Route Table	private-rt
AWS Services Used
Amazon VPC
Amazon EC2
Amazon RDS
Internet Gateway
NAT Gateway
Route Tables
Public and Private Subnets
💻 Technologies Used
Java
MySQL
SQL
Linux
AWS EC2
AWS RDS
AWS VPC
Web Browser
🔄 Project Implementation Steps
Step 1: Create Custom VPC

Created a custom VPC named three-tier-vpc.

IPv4 CIDR: 10.0.0.0/16
AWS Region: us-east-1
Step 2: Create Subnets

Created three subnets across different Availability Zones.

Subnet Name	Availability Zone	CIDR
public-subnet	us-east-1a	10.0.0.0/20
private1-subnet	us-east-1b	10.0.16.0/20
private2-subnet	us-east-1c	10.0.32.0/20
Step 3: Configure Internet Gateway
Created an Internet Gateway named my-ig.
Attached it to the custom VPC.
Configured internet routing for the public subnet.
Step 4: Configure NAT Gateway
Created a NAT Gateway named nat-gtw.
Placed it in the public subnet.
Configured outbound internet access for private subnet resources.
Step 5: Configure Route Tables
Created and configured route tables.
Associated the required subnets.
Configured local VPC routing.
Configured internet routing through the Internet Gateway and NAT Gateway.
Step 6: Launch EC2 Instances

Launched EC2 instances for the application and database setup.

Private 1 EC2: Java application deployment.
Private 2 EC2: Database setup and MySQL operations.

Connected to the instances and performed the required configurations.

Step 7: Create MySQL Database

Installed/accessed MySQL and created the application database.

Database name:

studentapp

SQL commands:

sql
CREATE DATABASE studentapp;

USE studentapp;

Step 8: Create Students Table

Created the students table using the following SQL schema:

sql
CREATE TABLE IF NOT EXISTS students (
    student_id INT NOT NULL AUTO_INCREMENT,
    student_name VARCHAR(100) NOT NULL,
    student_addr VARCHAR(100) NOT NULL,
    student_age VARCHAR(3) NOT NULL,
    student_qual VARCHAR(20) NOT NULL,
    student_percent VARCHAR(10) NOT NULL,
    student_year_passed VARCHAR(10) NOT NULL,
    PRIMARY KEY (student_id)
);


Copied the schema.sql file to the database setup server and executed it in MySQL.

Verified successful database and table creation.

Step 9: Configure Amazon RDS Connectivity
Obtained the Amazon RDS MySQL endpoint.
Configured the Java application's database connection.
Added the RDS endpoint to the application configuration.
Connected the Java application with the MySQL database.
Step 10: Deploy Java Application
Connected to Private 1 EC2.
Configured the Java application.
Updated database connection settings.
Started the application.
Accessed the application through a web browser.
🎯 Final Application Output

<badge color="success">Successfully deployed</badge>

The Student Management System was successfully deployed and tested.

Application Features
Student Registration
View Student Records
Edit Student Details
Delete Student Records
Student Table Fields
Column	Description
student_id	Unique student ID
student_name	Student name
student_addr	Student address
student_age	Student age
student_qual	Student qualification
student_percent	Student percentage
student_year_passed	Passing year
Live Application
text
http://98.84.35.107/student


The application successfully displayed registered student records in the browser.

📚 Key Learnings
AWS VPC creation and configuration.
Public and private subnet networking.
Internet Gateway and NAT Gateway configuration.
Route table configuration and subnet association.
EC2 instance deployment and management.
MySQL database creation and table management.
SQL schema execution.
Amazon RDS endpoint configuration.
Java application and database connectivity.
Real-world cloud application deployment.
🔐 Security Best Practices
Keep database access restricted to the application security group.
Avoid exposing MySQL port 3306 publicly.
Restrict SSH access to trusted IP addresses.
Never upload database credentials or private keys to GitHub.
Use HTTPS for production deployments.
🏁 Conclusion

Successfully completed the deployment of a Java Student Management System using AWS cloud infrastructure.

This hands-on project provided practical experience with AWS networking, EC2, Amazon RDS, MySQL, Linux, and Java application deployment.

It demonstrates how a Java web application can communicate with a remote MySQL database using AWS cloud services.

Project: Java Student Management System

Architecture: AWS 3-Tier Deployment

Database: MySQL – studentapp

Table: students

Deployment Status: Successfully Completed ✅

Learning by building. Growing through cloud technology.



<img width="1366" height="768" alt="Screenshot (232)" src="https://github.com/user-attachments/assets/c8ca6838-edf5-4bcd-82ae-2bb6475c0794" />

<img width="1366" height="768" alt="Screenshot (233)" src="https://github.com/user-attachments/assets/1b859000-e43f-411a-9e46-8c5a9dde60e2" />

<img width="1366" height="768" alt="Screenshot (234)" src="https://github.com/user-attachments/assets/692c23c3-eef5-4195-81f0-99ea60b8de7c" />



