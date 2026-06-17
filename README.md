# ☁️ AWS Cloud Architecture Portfolio

## 📌 Overview

A collection of AWS cloud architecture projects demonstrating secure,
highly available, scalable, and production-style infrastructure designs.

The projects are designed following AWS Well-Architected Framework principles:

- Security
- Reliability
- Performance Efficiency
- Cost Optimization
- Operational Excellence

---

# 🏗️ Projects

# 1️⃣ Secure Two-Tier Architecture (EC2 Based)

## 📌 Overview

Designed a secure two-tier web application architecture deployed
across multiple Availability Zones.

The architecture focuses on network isolation, secure access control,
and high availability.

## 🏛️ Architecture

User Traffic

↓
Application Tier (EC2)

↓
Database Tier (Private EC2)

## ☁️ AWS Services

- Amazon VPC
- EC2
- Internet Gateway
- NAT Gateway
- Route Tables
- Security Groups
- Network ACLs
- VPC Endpoint
- Amazon S3

## 🔐 Security

- Private subnet isolation
- Restricted inbound traffic
- Least privilege Security Groups
- No direct database exposure

## 📈 Availability

- Multi-AZ deployment
- Fault tolerant network design
- Secure outbound updates
---

# 2️⃣ Secure Two-Tier Web Application (ALB + RDS)

## 📌 Overview

Production-style two-tier architecture using EC2 for the application
layer and Amazon RDS MySQL as the database layer.

## 🏛️ Architecture

Client

↓

Application Load Balancer (HTTPS)

↓
EC2 Auto Scaling Group

↓
Amazon RDS MySQL Multi-AZ

## ☁️ AWS Services

- VPC
- Application Load Balancer
- EC2
- Auto Scaling
- Amazon RDS
- NAT Gateway
- AWS Certificate Manager
- Security Groups

## 🔐 Security

- HTTPS encryption using ACM
- SSL termination at ALB
- Private application/database layers
- Security Group based communication


## 📈 High Availability

- ALB across multiple AZs
- EC2 Auto Scaling
- RDS Multi-AZ failover

---

# 3️⃣ Production Multi-Tier AWS Architecture

## 📌 Overview

Enterprise-style scalable AWS architecture designed for production workloads.

## ☁️ AWS Services

- Route 53
- CloudFront
- ALB
- Auto Scaling
- EC2
- RDS Multi-AZ
- SQS
- IAM
- KMS

## 🚀 Features

- High availability
- Scalability
- Decoupled architecture
- Secure access management
- Encryption at rest

---

# 🧠 Skills Demonstrated

- AWS Architecture Design
- VPC Networking
- Subnet Design
- Routing
- Load Balancing
- Auto Scaling
- Database Architecture
- IAM Security
- Cloud Security
- High Availability

---

# 👨‍💻 Author

Mohamed Gamal Nasser
