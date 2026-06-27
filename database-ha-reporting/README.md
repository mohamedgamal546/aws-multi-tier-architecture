AWS Highly Available Database Architecture (RDS Multi-AZ + Read Replica)

📌 Project Overview

This project demonstrates the design of a highly available, fault-tolerant, and secure database architecture for a production multi-tier web application on AWS.

The solution is designed to support both transactional application workloads and reporting workloads while ensuring that reporting queries do not impact the performance of the primary production database.

The architecture leverages fully managed Amazon RDS features to minimize operational overhead while providing high availability, security, and scalability.

⸻

🏗️ Architecture Design

The solution is deployed within a single AWS Region across multiple Availability Zones.

Primary Database

* Amazon RDS for MySQL
* Multi-AZ deployment
* Automatic failover
* Handles all application read/write operations

Reporting Database

* Amazon RDS Read Replica
* Dedicated read-only database
* Handles reporting queries and complex table joins
* Prevents reporting workloads from impacting production performance

⸻

🌐 Database Connectivity

Application Traffic

* EC2 application servers connect to the primary Amazon RDS instance
* All read/write operations are processed by the primary database

Reporting Traffic

* Reporting tools connect exclusively to the Amazon RDS Read Replica
* Reporting workloads are isolated from production traffic

⸻

⚖️ High Availability & Performance

Multi-AZ Deployment

* Automatic failover
* Standby database in a separate Availability Zone
* High availability and fault tolerance

Read Replica

* Offloads reporting queries
* Improves database performance
* Supports read scalability

⸻

🔐 Security Design

Encryption in Transit

* SSL/TLS encryption between the application and Amazon RDS

Network Security

* Database deployed in private subnets
* No public database access
* Security Groups allow database access only from the application tier

Managed Database Service

* Automated backups
* Automatic software patching
* Reduced operational overhead

⸻

🔄 Architecture Flow

Application

↓

Amazon RDS Primary (Multi-AZ)

↓

Amazon RDS Read Replica

↓

Reporting Tool

⸻

🎯 Key Features

* Amazon RDS Multi-AZ Deployment
* Read Replica for Reporting
* Automatic Failover
* High Availability
* Fault Tolerance
* SSL/TLS Encryption
* Performance Optimization
* Managed Database Operations

⸻

🧠 Skills Demonstrated

* Amazon RDS
* Multi-AZ Deployment
* Read Replicas
* Database High Availability
* Fault Tolerance
* Database Security
* SSL/TLS Encryption
* Performance Optimization
* AWS Architecture Design
