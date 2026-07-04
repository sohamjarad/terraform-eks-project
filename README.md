# 🚀 Terraform AWS EKS Infrastructure

![Terraform](https://img.shields.io/badge/Terraform-1.6+-623CE4?style=for-the-badge&logo=terraform)
![AWS](https://img.shields.io/badge/AWS-EKS-FF9900?style=for-the-badge&logo=amazonaws)
![Kubernetes](https://img.shields.io/badge/Kubernetes-1.30-326CE5?style=for-the-badge&logo=kubernetes)
![GitHub](https://img.shields.io/badge/GitHub-Version_Control-181717?style=for-the-badge&logo=github)

---

# 📌 Project Overview

This project provisions a complete **Amazon EKS (Elastic Kubernetes Service)** infrastructure on AWS using **Terraform** following Infrastructure as Code (IaC) principles.

The infrastructure is designed to deploy and manage containerized applications on Kubernetes while providing a secure, scalable, and highly available networking environment.

The project demonstrates real-world DevOps practices including Infrastructure as Code, Kubernetes orchestration, AWS networking, remote Terraform state management, and infrastructure automation.

---

# ✨ Features

- Infrastructure as Code using Terraform
- Modular Terraform Architecture
- Amazon EKS Cluster Deployment
- Custom Amazon VPC
- Public & Private Subnets
- Internet Gateway
- NAT Gateway
- Route Tables
- Elastic IP
- IAM Roles & Policies
- Remote Terraform Backend using S3
- Terraform State Locking using DynamoDB
- Kubernetes Cluster Provisioning
- Scalable Node Group Configuration

---

# ☁️ AWS Services Used

- Amazon EKS
- Amazon EC2
- Amazon VPC
- Internet Gateway
- NAT Gateway
- Route Tables
- Elastic IP
- IAM
- Amazon S3
- Amazon DynamoDB

---

# 🛠 Tech Stack

- Terraform
- AWS
- Amazon EKS
- Kubernetes
- Git
- GitHub

---

# 🏗 Architecture

```
                           Internet
                               │
                               ▼
                     Internet Gateway
                               │
        ┌──────────────────────┼──────────────────────┐
        │                                             │
        ▼                                             ▼
 Public Subnet (AZ-1)                         Public Subnet (AZ-2)
        │                                             │
        ▼                                             ▼
     NAT Gateway                               NAT Gateway
        │                                             │
        └───────────────┬─────────────────────────────┘
                        ▼
                    Private Subnets
                        │
                        ▼
                  Amazon EKS Cluster
                        │
              EKS Managed Node Group
                        │
                        ▼
                Kubernetes Workloads

---------------------------------------------------------

Terraform Backend

Terraform
      │
      ▼
Amazon S3 (State File)

      │
      ▼
Amazon DynamoDB (State Lock)
```

---

# 📂 Repository Structure

```
terraform-eks-project
│
├── backend
│
├── modules
│   ├── eks
│   │     ├── main.tf
│   │     ├── variables.tf
│   │     └── outputs.tf
│   │
│   └── vpc
│         ├── main.tf
│         ├── variables.tf
│         └── outputs.tf
│
├── main.tf
├── variables.tf
├── outputs.tf
├── .gitignore
└── README.md
```

---

# 🚀 Deployment

## Clone Repository

```bash
git clone https://github.com/sohamjarad/terraform-eks-project.git
cd terraform-eks-project
```

---

## Initialize Terraform

```bash
terraform init
```

---

## Validate Configuration

```bash
terraform validate
```

---

## Review Execution Plan

```bash
terraform plan
```

---

## Deploy Infrastructure

```bash
terraform apply
```

Type

```
yes
```

when prompted.

---

## Configure kubectl

```bash
aws eks update-kubeconfig --region us-east-1 --name my-eks-cluster
```

---

## Verify Cluster

```bash
kubectl get nodes
```

Expected Output

```
NAME                           STATUS
ip-10-0-x-xx.ec2.internal      Ready
```

---

# 💰 Destroy Infrastructure

To avoid unnecessary AWS charges:

```bash
terraform destroy
```

---

# 🔒 Remote Backend

Terraform remote backend is configured using:

- Amazon S3 for Terraform State
- Amazon DynamoDB for State Locking

This prevents state corruption during collaborative deployments.

---

# 📈 Skills Demonstrated

- Infrastructure as Code (Terraform)
- AWS Cloud Infrastructure
- Amazon EKS
- Kubernetes
- AWS Networking
- VPC Design
- Public & Private Subnets
- Route Tables
- NAT Gateway
- Internet Gateway
- IAM Roles & Policies
- Remote Terraform Backend
- Terraform Modules
- State Management
- Cloud Automation
- Git Version Control

---

# 🎯 Learning Outcomes

Through this project I gained hands-on experience in:

- Designing AWS infrastructure using Terraform
- Building reusable Terraform modules
- Provisioning Amazon EKS clusters
- Configuring secure VPC networking
- Managing Kubernetes infrastructure
- Using remote Terraform state with S3 and DynamoDB
- Automating cloud infrastructure deployments
- Following Infrastructure as Code best practices

---

# 📋 Prerequisites

Before running this project ensure you have:

- AWS Account
- AWS CLI
- Terraform
- kubectl
- Git

---

# 📌 Future Improvements

- GitHub Actions CI/CD Pipeline
- Argo CD GitOps Deployment
- AWS Load Balancer Controller
- Route53 Integration
- Custom Domain Mapping
- Monitoring using Prometheus & Grafana
- Logging with CloudWatch

---

# 👨‍💻 Author

**Soham Jarad**

**GitHub:** https://github.com/sohamjarad

---

# ⭐ If you found this project useful, consider giving it a Star!
