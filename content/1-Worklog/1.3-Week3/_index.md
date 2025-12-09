---
title: "Week 3 Worklog"
date: "2025-09-22"
weight: 3
chapter: 1
pre: " <b> 1.3. </b> "

---

## 🎯 Week 3 Objectives

- Fully understand and review all processes from Weeks 1 and 2.  
- Practice rebuilding core AWS infrastructure components: **VPC**, **EC2**, **EIP**, **NAT Gateway**.  
- Strengthen skills in managing networking resources and monitoring AWS service usage.

---

## 🗂 Tasks to Complete This Week

| Day | Tasks | Start Date | End Date | Reference |
| --- | ----- | ---------- | -------- | -------- |
| **Monday** | - Review AWS concepts from Weeks 1 & 2.<br>- Revisit core terminology: Region, AZ, VPC, EC2, IAM. | 22/09/2025 | 22/09/2025 | Internal notes |
| **Tuesday** | - Study AWS **Networking services**: VPC, Subnet, Internet Gateway, NAT Gateway, Route Tables.<br>- Learn best practices for designing basic VPC architecture. | 23/09/2025 | 23/09/2025 | cloudjourney.awsstudygroup.com |
| **Wednesday** | - Create a new **VPC**, Subnets (public/private), Internet Gateway, NAT Gateway.<br>- Configure **Security Groups**, **Network ACLs**, and Route Tables. | 24/09/2025 | 24/09/2025 | cloudjourney.awsstudygroup.com |
| **Thursday** | - Launch **EC2 instance** inside VPC.<br>- Attach **Elastic IP (EIP)** and test SSH connectivity.<br>- Create and mount **EBS volume**. | 25/09/2025 | 25/09/2025 | cloudjourney.awsstudygroup.com |
| **Friday** | - Audit resources (EC2, VPC, EIP, NAT Gateway).<br>- Delete unused resources to reduce cost.<br>- Monitor budget using **AWS Cost Explorer & Budgets**. | 26/09/2025 | 26/09/2025 | cloudjourney.awsstudygroup.com |

---

## ✅ Results Achieved in Week 3

### 1. Strengthened Knowledge from Previous Weeks
- Fully reviewed and reinforced concepts from Week 1 & 2.  
- Understood roles of IAM, EC2, VPC in AWS architecture.  

### 2. Deep Understanding of AWS Networking
- Built a complete **custom VPC** from scratch.  
- Configured:
  - Public & private subnets  
  - Route Tables  
  - Internet Gateway & NAT Gateway  
  - Security Groups & Network ACLs  
- Ensured secure and efficient connectivity across components.

### 3. Successful EC2 Deployment & Configuration
- Launched EC2 instance inside custom VPC.  
- Connected successfully using SSH.  
- Assigned a persistent **Elastic IP (EIP)**.  
- Created and mounted an **EBS volume**, including:
  - Partitioning  
  - Formatting  
  - Mounting  
  - Persisting via `/etc/fstab`  

### 4. Resource Review & Cost Control
- Reviewed all deployed AWS resources.  
- Deleted unused VPC components, NAT Gateway, EIP, EC2 to avoid extra charges.  
- Learned monitoring through:
  - AWS Budgets  
  - AWS Cost Explorer  

### 5. AWS CLI + Console Practice
- Operated AWS using both:
  - AWS Management Console  
  - AWS CLI  
- Performed CLI tasks:
  - VPC creation  
  - Subnet creation  
  - EC2 launch  
  - EBS operations  
  - Security Group configuration  

### 6. Overall Skills Improvement
- Improved cloud infrastructure deployment skills.  
- Understood real-world AWS networking operations.  
- Prepared for upcoming topics: ALB, Auto Scaling, RDS, CI/CD, etc.

---
