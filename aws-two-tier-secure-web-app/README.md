# AWS Two-Tier Secure Web Application

## Overview

This project implements a secure and highly available two-tier web application on AWS.

## Architecture

Client
|
HTTPS
|
Application Load Balancer
|
EC2 Web/App Tier
|
Amazon RDS MySQL


## Components

- VPC
- Public Subnets
- Private Subnets
- Application Load Balancer
- EC2 Auto Scaling Group
- Amazon RDS MySQL Multi-AZ
- NAT Gateway
- AWS Certificate Manager


## Security

- EC2 instances are not publicly accessible
- RDS is private only
- Security Groups restrict traffic flow
- SSL termination handled by ALB


## High Availability

- ALB deployed across multiple AZs
- EC2 instances distributed across AZs
- RDS Multi-AZ failover
