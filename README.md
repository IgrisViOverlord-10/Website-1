# 🚀 Static Website Deployment on AWS EC2 using Nginx & Git

## 📌 Overview

This project demonstrates the deployment of a static website on an Ubuntu-based Amazon EC2 instance using Nginx as the web server.
The primary objective was to implement a version-controlled deployment workflow while understanding core AWS infrastructure components and Linux server management.
This setup represents a foundational single-tier web architecture.

---

## 🏗 Architecture Components

• Amazon EC2 (Ubuntu 22.04 LTS)  
• Default VPC with Internet Gateway  
• Public Subnet  
• Security Group (SSH 22, HTTP 80)  
• Nginx Web Server  
• Git-based source control  

### Request Flow

Client → Internet → Security Group → EC2 Instance → Nginx → `/var/www/html/index.html`

---

## ⚙️ Deployment Workflow

### 1️⃣ Infrastructure Provisioning
- Launched EC2 instance (t2.micro)
- Configured inbound rules for SSH and HTTP
- Verified public IP accessibility

### 2️⃣ Server Configuration
- Updated package repository
- Installed Nginx and Git
- Enabled and managed Nginx using systemctl

### 3️⃣ Version-Controlled Deployment
- Created GitHub repository
- Cloned repository directly onto EC2
- Deployed application files to `/var/www/html`
- Restarted Nginx service to serve updated content

This approach ensures repeatable deployments and structured code management.

---

## 🔍 Alternative Deployment Methods Evaluated

To compare operational flexibility, the following approaches were tested:

• Secure file transfer using SCP  
• Remote template retrieval using wget  
• Direct server-side editing using nano  

Each method provided insight into deployment trade-offs between speed, control, and maintainability.

---

## 🔐 Security Considerations

• Principle of least privilege applied at security group level  
• Public access restricted to required ports only  
• Default Nginx directory permissions validated  

---

## 📚 Technical Skills Demonstrated

• EC2 provisioning and networking fundamentals  
• Linux command-line operations  
• Nginx configuration and service management  
• Git-based deployment workflow  
• Static web hosting architecture  

---
