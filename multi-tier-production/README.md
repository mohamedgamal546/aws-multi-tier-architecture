# AWS Multi-Tier Architecture (Highly Available & Scalable)

## 📌 Overview

This project presents a production-style design for a highly available, secure, and scalable multi-tier web application on AWS. The architecture follows best practices for networking, security, performance optimization, and hybrid connectivity.

---

## 🧱 Architecture Design

### 🌐 Networking

- **VPC:** `10.0.0.0/16`

- **Public Subnets:**
  - `10.0.10.0/24` (AZ-A)
  - `10.0.20.0/24` (AZ-B)

- **Private Subnets:**
  - `10.0.100.0/24` (AZ-A)
  - `10.0.200.0/24` (AZ-B)

- Internet Gateway for public access
- NAT Gateway for outbound internet access from private subnets


---

## ⚖️ High Availability & Scalability

- Application Load Balancer (ALB) distributes traffic across:
  - EC2 instances in multiple Availability Zones

- Auto Scaling Group ensures:
  - High availability
  - Automatic scaling based on demand


---

## 🖥️ Compute Layer

- EC2 instances (EBS-backed) deployed across two AZs
- Instances handle both Web & Application tiers
- IAM Roles attached to EC2 for secure access to AWS services


---

## 🗄️ Database Layer

- Amazon RDS deployed in Multi-AZ configuration:
  - Primary instance (AZ-A)
  - Standby instance (AZ-B) for failover

- Data encryption enabled using AWS KMS


---

## 🔄 Decoupling Layer

- Amazon SQS used to decouple application components

**Flow:**
