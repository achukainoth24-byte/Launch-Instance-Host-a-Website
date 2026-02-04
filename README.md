# Launch-Instance-Host-a-Website
This project demonstrates how to launch an AWS EC2 instance and host a static website using the Apache web server. it is a beginner-friendly, step by step lab designed for AWS fresher. 
# AWS Fresher Projects – Complete Step-by-Step Hands-On Labs

This repository contains **all essential AWS beginner projects** required for **freshers and entry-level cloud roles**.  
Each lab is simple, practical, and aligned with interview expectations.

---

## What You Will Learn
- Amazon EC2
- Amazon S3
- IAM Role
- VPC Networking
- Application Load Balancer
- SQS
- CloudWatch
- Linux & Apache
- AWS Free Tier Hands-On

---

## Overall Architecture Concept
Users access applications through **Public IP / Load Balancer**, services communicate securely using **IAM roles**, and infrastructure is monitored using **CloudWatch**.

---

## PROJECT 1: EC2 – Launch Instance & Host a Simple Website

### Objective
Launch an EC2 instance and host a static website using Apache Web Server.

### Services Used
EC2, Security Group, Key Pair

### Steps
1. Login to AWS Console  
2. EC2 → Launch Instance  
3. Choose **Amazon Linux 2**  
4. Instance type → **t2.micro (Free Tier)**  
5. Create Key Pair (.pem)  
6. Security Group:
   - SSH (22) → My IP  
   - HTTP (80) → Anywhere  
7. Launch instance  
8. Connect using **EC2 Instance Connect**

### Commands
```bash
sudo yum update -y
sudo yum install httpd -y
sudo systemctl start httpd
sudo systemctl enable httpd
cd /var/www/html
echo "Hello from AWS EC2 Web Server" | sudo tee index.html
