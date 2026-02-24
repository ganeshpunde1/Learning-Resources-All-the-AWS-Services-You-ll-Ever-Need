# AWS Learning Roadmap – >> 

## Introduction to the AWS Learning Approach

* Amazon Web Services (AWS) offers 200+ services, which can feel overwhelming for beginners.
* It is not necessary to learn all services at once; focusing on 15–20 core services covers about 95% of real-world applications.
* Many learners waste months trying to learn everything, which often leads to confusion during interviews.
* The goal is to become AWS-literate in a realistic way for internships, beginner, intermediate, or advanced roles.
* This guide breaks AWS into seven core buckets with a practical, project-based learning path.
* Emphasis: learn by building, not memorizing.
* Strong fundamentals in coding and networking are essential.
* Some services can safely be ignored at the beginning.

---

## Learning Resources and Methodology

* Use AWS Skill Builder and official AWS training programs for hands-on practice.
* Focus on building projects instead of rote memorization.
* Coding skills help automate and manage AWS resources efficiently.
* Follow guided labs, documentation, and real-world implementation.

---

## Bucket 1: Foundation and Security

### Core Foundations

* SDLC (Software Development Life Cycle)
* Cloud deployment models: Private, Public, Hybrid, Multi-cloud
* Cloud service models: IaaS, PaaS, SaaS
* AWS Regions and Availability Zones (data centers and connectivity)
* Create an AWS account as your Day 1 action.

### AWS Account Setup and Billing Controls

* Create an account at aws.com.
* Use the Free Tier and learning credits when available.
* Enable MFA (Multi-Factor Authentication) using Google Authenticator or similar apps.
* Set billing alerts and budget alarms to control expenses.
* Optionally create an IAM user for learning instead of using the root account.

### AWS Organizations and Account Management

* Enterprises use AWS Organizations to manage multiple accounts.
* Separate accounts for dev, staging, and production are a best practice.
* AWS Control Tower helps with governance and security but is not required for beginners.
* One account is sufficient for learning.

### Identity and Access Management (IAM)

IAM controls permissions inside your AWS account. Every action requires explicit permission.

Key Components:

1. Users – Individual identities
2. Groups – Collections of users with shared permissions
3. Roles – Assigned to services or applications
4. Policies – JSON documents defining permissions

Example:
An EC2 instance accessing an S3 bucket via an IAM role with S3 permissions.

### Secrets and Configuration Management

* AWS Secrets Manager: Secure storage for passwords, API keys, and credentials (supports rotation, but has a cost).
* AWS Systems Manager Parameter Store: Free alternative for configuration data and simple secrets.
* Best Practice: Never hardcode secrets in code.

### IAM Best Practices

* Create an IAM admin user (for learning purposes).
* Use roles instead of long-term access keys.
* Clearly understand the difference between users and roles (common interview topic).
* Mastering IAM builds a strong security foundation.

---

## Bucket 2: Compute and Container Services

Compute is essential for running applications.

Focus on these five core services:

1. EC2 (Elastic Compute Cloud) – Virtual servers, pay-as-you-go, Linux/Windows support
2. Lambda – Serverless compute, auto-scaling, pay per execution
3. ECS (Elastic Container Service) – Run Docker containers
4. Fargate – Serverless containers (no infrastructure management)
5. EKS (Elastic Kubernetes Service) – Managed Kubernetes (advanced use)

Additional Concepts:

* Spot Instances (cost savings up to ~70%)
* Auto Scaling
* AWS Batch
* Savings Plans and Compute Optimizer

### Coding Requirements for Compute

* AWS CLI proficiency
* Basic Bash scripting and Linux commands (SSH)
* Writing Lambda functions (Python, Node.js, etc.)
* Understanding Docker and container orchestration (ECS/EKS)

---

## Bucket 3: Storage and Databases

### Storage Types Overview

| Storage Type     | Description                           | Use Cases                      |
| ---------------- | ------------------------------------- | ------------------------------ |
| Object Storage   | Stores files as objects with metadata | Backups, images, archives      |
| Block Storage    | Virtual disks attached to compute     | OS drives, application data    |
| File Storage     | Shared network file systems           | Multiple servers sharing files |
| Database Storage | Structured and NoSQL databases        | Application data storage       |

### Core AWS Storage Services

| Service  | Type           | Description                            | Notes                                   |
| -------- | -------------- | -------------------------------------- | --------------------------------------- |
| S3       | Object Storage | Durable and scalable object storage    | Buckets, versioning, lifecycle policies |
| EBS      | Block Storage  | Persistent storage for EC2             | Data survives instance termination      |
| EFS      | File Storage   | Scalable shared file system            | Mountable across multiple EC2 instances |
| RDS      | Relational DB  | Managed SQL databases                  | Requires basic SQL knowledge            |
| DynamoDB | NoSQL DB       | Serverless key-value/document database | High scalability and low latency        |

Additional Services:

* ElastiCache (Redis, Memcached) – In-memory caching
* Aurora – High-performance AWS relational database

### Storage Decision Guide

* Files (images/videos) → S3
* Block storage for EC2 → EBS
* Shared file system → EFS
* Relational queries → RDS
* Scalable NoSQL → DynamoDB
* Caching → ElastiCache

---

## Bucket 4: Networking and Content Delivery

Basic networking knowledge is sufficient.

### Core Components

1. VPC (Virtual Private Cloud)

   * Subnets (public/private)
   * Route tables
   * Internet Gateway & NAT Gateway
   * Security Groups (firewall rules)
2. Load Balancers

   * Application Load Balancer (HTTP/HTTPS)
   * Network Load Balancer (TCP/UDP)
3. Route 53 – DNS management and domain routing
4. CloudFront – CDN for global content caching
5. API Gateway – API management, authentication, and rate limiting

Key Concept: Understand traffic flow between public and private subnets.

---

## Bucket 5: DevOps and Automation

Automate infrastructure instead of manual console operations.

### Key Services

1. CloudFormation – Infrastructure as Code using YAML
2. AWS CDK – Infrastructure as Code using Python/TypeScript
3. CodePipeline – CI/CD orchestration
4. CodeBuild – Build and compile code
5. CodeDeploy – Automated deployment to EC2/ECS/EKS
6. EventBridge – Event-driven architecture and event routing

Benefits:

* Version control
* Repeatability
* Faster deployments
* Improved reliability

---

## Bucket 6: AI and Machine Learning (2026 Focus)

AI/ML is a major differentiator in modern cloud roles.

### Core AI Workload Patterns

1. Managed AI Services

   * Amazon Bedrock – Access foundation models via API
2. Custom Model Development

   * SageMaker – Build, train, and deploy ML models
3. AI Coding Assistance

   * CodeWhisperer – AI-powered coding assistant

Additional AI Services:

* Textract – Document text extraction
* Rekognition – Image/video analysis
* Comprehend – NLP processing

These services enable AI-powered applications without deep ML expertise.

---

## Bucket 7: Monitoring and Cost Management

### Essential Services

1. CloudWatch – Metrics, logs, alarms, and dashboards
2. Cost Explorer & Budgets – Spending analysis and budget alerts
3. CloudTrail – Audit logs for API calls and user activity

Best Practices:

* Enable budget alarms early
* Monitor usage regularly
* Activate CloudTrail for security and auditing

---

## Seven Portfolio Projects to Build AWS Literacy

Practical experience is mandatory for interview readiness.

1. Three-Tier Web Application

   * VPC, Load Balancer, EC2, RDS
2. Serverless REST API

   * API Gateway + Lambda + DynamoDB
3. CI/CD Pipeline

   * CodePipeline + CodeBuild + Deployment
4. Event-Driven File Processing System

   * S3 + Lambda + EventBridge + SNS
5. AI-Based Document Analysis

   * S3 + Lambda + Textract + Comprehend
6. Infrastructure as Code Project

   * Full stack using AWS CDK
7. Advanced AI Chatbot

   * Bedrock + API Gateway + Lambda + DynamoDB + CloudFront

---

## Summary and Final Advice

* Focus on seven core AWS buckets instead of all 200+ services.
* Learn by building, breaking, and fixing real projects.
* Use official AWS learning resources and hands-on labs.
* Avoid overwhelm by prioritizing core services.
* Progress step-by-step with practical implementation.

### Key Takeaway

To become AWS-literate and job-ready, master a focused set of core services, build real-world projects, and leverage automation and infrastructure as code. Do not try to learn everything at once—build progressively with hands-on experience.

---

## Core Buckets and Key Services Overview

| Bucket # | Focus Area                   | Key Services / Concepts                                         | Coding Requirement        | Notes                                    |
| -------- | ---------------------------- | --------------------------------------------------------------- | ------------------------- | ---------------------------------------- |
| 1        | Foundation & Security        | IAM, Policies, Secrets Manager, VPC                             | JSON, basic networking    | Critical for security and access control |
| 2        | Compute & Containers         | EC2, Lambda, ECS, Fargate, EKS                                  | Bash, Docker, CLI         | Core compute services to prioritize      |
| 3        | Storage & Databases          | S3, EBS, EFS, RDS, DynamoDB, ElastiCache                        | SQL, NoSQL, scripting     | Understand storage types and use cases   |
| 4        | Networking & CDN             | VPC, Subnets, Load Balancers, Route 53, CloudFront, API Gateway | Basic networking concepts | Focus on availability and security       |
| 5        | DevOps & Automation          | CloudFormation, CDK, CodePipeline, CodeBuild, EventBridge       | YAML, Python/TypeScript   | Enables automation and scalability       |
| 6        | AI & Machine Learning        | Bedrock, SageMaker, CodeWhisperer, Textract, Rekognition        | API calls (Python/JS)     | High-demand skill area                   |
| 7        | Monitoring & Cost Management | CloudWatch, Cost Explorer, Budgets, CloudTrail                  | Minimal coding            | Essential for cost and security control  |
