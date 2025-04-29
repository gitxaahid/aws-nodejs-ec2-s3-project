# aws-nodejs-ec2-s3-project
Deployed a Node.js app on EC2 with S3 static content and VPC networking.
# 🚀 Node.js Web App Deployment using AWS EC2, S3, and VPC

## 📌 Project Overview

This project demonstrates how to deploy a Node.js application on an **Amazon EC2 instance**, serve static content from **Amazon S3**, and securely manage the infrastructure using **VPC (Virtual Private Cloud)** and **IAM roles**. The goal was to simulate a real-world cloud deployment environment with proper networking and access control.

---

## 🧰 Technologies & AWS Services Used

- **Amazon EC2** – Host the Node.js server on a Linux instance
- **Amazon S3** – Store public images for use in the app
- **Amazon VPC** – Set up a dedicated network with private/public subnet configuration
- **AWS IAM** – Attach roles and policies to allow EC2 to use Systems Manager securely
- **AWS Systems Manager** – SSH-less connection to EC2
- **Linux (Ubuntu)** – OS used to configure and run the app
- **Node.js + Express** – Server-side environment for the application

---

## 🧑‍💻 Steps Performed

### 1. ✅ EC2 Instance Setup
- Launched EC2 using Ubuntu AMI inside a **custom VPC**
- Attached **IAM role** with Systems Manager policies
- Configured **Security Groups** to allow SSH (for testing), HTTP traffic
- Connected to EC2 using **AWS Systems Manager (Session Manager)**

### 2. 🧠 Install Node.js & npm
```bash
sudo apt update
sudo apt install nodejs npm -y
node -v
npm -v
