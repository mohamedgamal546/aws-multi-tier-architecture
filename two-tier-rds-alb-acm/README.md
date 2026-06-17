# AWS Two-Tier Web Application Architecture (ALB + RDS MySQL)

## 📌 Project Overview

This project demonstrates the design of a secure, highly available, and scalable two-tier web application architecture on AWS.

The architecture uses Amazon EC2 instances for the Web/Application tier and Amazon RDS for MySQL as the Database tier following AWS best practices for security, networking, and availability.


---

## 🏗️ Architecture Design

The solution is designed within a single AWS Region using multiple Availability Zones.

### Application Tier

- Amazon EC2 instances host the web/application layer
- EC2 instances are deployed in private subnets
- Application traffic is received only through an Elastic Load Balancer (ALB)


### Database Tier

- Amazon RDS for MySQL deployed in private subnets
- Database is not publicly accessible
- Database access is allowed only from the application tier


---

## 🌐 Networking Design

### VPC

- Custom VPC architecture
- High availability design across multiple Availability Zones


### Subnet Design

Minimum subnet design is used:

- Public subnets:
  - Application Load Balancer


- Private subnets:
  - EC2 application instances
  - Amazon RDS MySQL database


### Routing

- Application tier and database tier use separate route tables
- No shared routing table between tiers


### Internet Access

Private resources access the internet only for updates through:

- NAT Gateway


---

## ⚖️ Load Balancing & Availability

### Application Load Balancer

ALB provides:

- Traffic distribution across EC2 instances
- Health checks
- High availability


### Auto Scaling

EC2 instances are managed using Auto Scaling Group:

- Automatic scaling
- Fault tolerance
- Improved availability


---

## 🔐 Security Design

### Network Security

- EC2 instances are not directly accessible from the internet
- RDS database has no public access
- Security Groups control communication between layers


### Application Security

Traffic flow:
