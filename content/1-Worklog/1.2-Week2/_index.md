---
title: "Week 2 Worklog"
date: "2025-09-15"
weight: 2
chapter: false
pre: " <b> 1.2. </b> "
---


### 🎯 Week 2 Objectives

* Begin using AWS services in real practice.  
* Learn how to manage and control created AWS resources.  
* Understand the basic operations of EC2, IAM, and Cost Management.

---

### 📝 Tasks Performed During the Week

| Day | Tasks | Start Date | Completion Date | References |
| --- | ------ | ----------- | ---------------- | ---------- |
| 2 | - Study **AWS Identity & Access Management (IAM)**.<br> - Practice creating **Users**, **Groups**, **Policies**, and multiple **IAM Roles**.<br> - Apply the principle of Least Privilege for permission management. | 15/09/2025 | 15/09/2025 | FCJ training materials |
| 3 | - Launch the first **Amazon Linux EC2 instance**.<br> - Create key pairs and learn how to connect using SSH.<br> - Configure the security group to allow SSH (port 22). | 16/09/2025 | 17/09/2025 | https://cloudjourney.awsstudygroup.com/ |
| 4 | - Continue configuring EC2 connectivity (key checking, port verification, IP access, and permissions).<br> - Set up **AWS Cost Budget** and monitor service usage.<br> - Explore Billing Dashboard and Cost Explorer for cost tracking. | 17/09/2025 | 17/09/2025 | https://cloudjourney.awsstudygroup.com/ |
| 5 | - Troubleshoot SSH connection issues (incorrect key permissions, blocked security group, outdated IP…).<br> - Create and assign an **Elastic IP (EIP)** to the EC2 instance.<br> - Verify the instance’s accessibility after attaching EIP. | 18/09/2025 | 18/09/2025 | https://cloudjourney.awsstudygroup.com/ |

---

### ✅ Week 2 Achievements

* **IAM Practices Completed:**  
  - Created Users and Groups following basic IAM structure.  
  - Created and attached Policies for specific permission levels.  
  - Built multiple IAM Roles (EC2 Role, S3 Access Role, etc.) to understand how EC2 assumes a role.  
  - Applied **Least Privilege** when assigning permissions.

* **EC2 Instance Deployment & Management:**  
  - Successfully launched an EC2 instance and connected via SSH.  
  - Understood Security Group structure and how inbound/outbound rules work.  
  - Resolved common connection issues, including:  
    - Incorrect key file permissions (400/600).  
    - Using the wrong public IP.  
    - Port 22 not opened.  
    - Instance deployed in the wrong region.  
  - Allocated and managed an **Elastic IP**, understanding the difference between a Public IP and EIP.

* **AWS Cost Management:**  
  - Created **Cost Budgets** to receive alerts when spending reaches defined thresholds.  
  - Monitored spending via Billing Dashboard and Cost Explorer.  
  - Gained a better understanding of how AWS charges for EC2 (On-demand, EIP idle charges, storage costs, etc.).

* **Improved AWS Operational Skills:**  
  - Became more comfortable navigating the AWS Console.  
  - Practiced using AWS CLI to check EC2 instances, IAM Users, and IAM Roles.  
  - Understood the full workflow for provisioning, configuring, monitoring, and troubleshooting AWS resources.

---

### 📝 Self-Assessment & Reflection (Week 2)

* Gained solid foundational skills with IAM and EC2.  
* Able to read and troubleshoot SSH errors independently.  
* Able to monitor and control cloud usage to avoid unnecessary costs.  
* Still need to improve speed and proficiency when using the CLI and deepen understanding of EC2 networking.

---

### 📅 Plan for Next Week (Week 3)

* Study **VPC**, Subnets, Route Tables, and NAT Gateways.  
* Create a custom VPC and deploy EC2 instances inside it.  
* Work with S3: create buckets, set bucket policies, and access via CLI.  
* Practice creating snapshots, AMIs, and managing storage.  
* Begin learning the deployment model of a basic 2-tier architecture on AWS.

