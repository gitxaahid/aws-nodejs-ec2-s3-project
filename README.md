# AWS EC2 & S3 Integration Project: Node.js Web App Deployment


## 📌 Project Overview
Deployed a Node.js web application on AWS EC2 with static image assets hosted on Amazon S3. The application displays a personalized achievement certificate with dynamic content integration between EC2 and S3.

## 🛠️ Technical Components
- **AWS Services**:
  - EC2 (Ubuntu)
  - S3 (Static Image Hosting)
  - VPC (Custom Network)
  - IAM (Systems Manager Access)
- **Stack**:
  - Node.js
  - Express Framework
  - Linux Shell

## 📋 Step-by-Step Implementation

### 1. Infrastructure Setup
```bash
# Create a custom VPC with:
- Public subnet
- Internet Gateway
- Route tables
- Security Group (HTTP: 80 access)

2. EC2 Configuration
Launch Instance:

AMI: Ubuntu Server 22.04 LTS

Instance Type: t2.micro

IAM Role: AmazonSSMManagedInstanceCore

Install Dependencies:

bash
sudo apt update
sudo apt install -y nodejs npm
node -v && npm -v  # Verify installations
3. S3 Bucket Setup
bash
# Created bucket: projectzbucket
- Uploaded 3 images (public read access)
- Retrieved object URLs:
  https://projectzbucket.s3.eu-north-1.amazonaws.com/img1.jfif
  https://projectzbucket.s3.eu-north-1.amazonaws.com/images2.png
  https://projectzbucket.s3.eu-north-1.amazonaws.com/images3.jfif
4. Application Deployment
File Structure:

/project-files
├── app.js
└── completion.html
Modified Files:

Updated completion.html:

html
<!-- Personalization -->
Hi <strong>Mohammad Zahid</strong>, 

<!-- S3 Image Integration -->
<img src="https://projectzbucket.s3.eu-north-1.amazonaws.com/img1.jfif">
Run Application:

bash
node app.js  # Runs on port 80
