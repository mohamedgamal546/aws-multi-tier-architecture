# AWS Hybrid Web Application Architecture (On-Premises Access)

## 📌 Project Overview

This project demonstrates the design of a secure, highly available, scalable, and fault-tolerant web application architecture on AWS.

The solution enables users from a company's on-premises network to access the application over the internet while complying with strict security requirements. Access to the application is restricted to two whitelisted public IP addresses configured on the company's on-premises firewall.

The architecture follows AWS best practices for security, availability, scalability, and network isolation.

---

## 🏗️ Architecture Design

The solution is deployed within a single AWS Region across multiple Availability Zones.

### User Access

* Users access the application from the corporate on-premises network
* Traffic traverses the internet through the corporate firewall
* Access is permitted only from two whitelisted public IP addresses

### Application Tier

* Application hosted on Amazon EC2 instances
* EC2 instances distributed across multiple Availability Zones
* Application layer designed for scalability and fault tolerance

### Database Tier

* Database design is outside the scope of this project

---

## 🌐 Networking Design

### VPC

* Custom Amazon VPC
* Multi-AZ deployment for high availability

### Public Subnets

* Application Load Balancer (ALB)

### Private Subnets

* EC2 application instances

### Internet Connectivity

* Internet Gateway for client access
* NAT Gateway for outbound software updates

---

## ⚖️ High Availability & Scalability

### Application Load Balancer

* Distributes traffic across multiple EC2 instances
* Performs health checks
* Eliminates single points of failure

### Auto Scaling Group

* Automatic scaling based on workload demand
* Improves availability and resilience
* Replaces unhealthy instances automatically

---

## 🔐 Security Design

### IP Whitelisting

Access to the application is restricted to:

* Whitelisted Public IP Address #1
* Whitelisted Public IP Address #2

### Security Groups

* ALB accepts traffic only from approved public IP addresses
* EC2 instances accept traffic only from the ALB Security Group

### Application Isolation

* EC2 instances are not directly accessible from the internet
* All client requests must pass through the Application Load Balancer

---

## 🔄 Architecture Flow

Corporate Users

↓

On-Premises Firewall

↓

Whitelisted Public IP Addresses

↓

Application Load Balancer

↓

EC2 Auto Scaling Group

---

## 🎯 Key Features

* Hybrid Connectivity Architecture
* IP Whitelisting Security Controls
* Highly Available Web Tier
* Auto Scaling Infrastructure
* Multi-AZ Deployment
* Application Load Balancing
* Fault Tolerant Design
* Secure Traffic Management

---

## 🧠 Skills Demonstrated

* AWS Architecture Design
* Hybrid Networking
* VPC Design
* Security Groups
* IP Whitelisting
* Application Load Balancer
* Auto Scaling
* High Availability Design
* Fault Tolerance
* Cloud Security Best Practices
