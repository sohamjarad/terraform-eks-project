# 🚀 Terraform AWS EKS Infrastructure

## 📌 Project Overview

This project provisions a complete Amazon EKS (Elastic Kubernetes Service) infrastructure on AWS using Terraform. It automates the creation of networking, security, and Kubernetes resources following Infrastructure as Code (IaC) best practices.

The infrastructure is designed to host containerized microservices applications and integrates seamlessly with Kubernetes deployments.

---

## 🏗️ Architecture

```
                    Internet
                        │
                        ▼
              AWS Application Load Balancer
                        │
         ┌──────────────┴──────────────┐
         ▼                             ▼
      Public Subnet                Public Subnet
         │                             │
         └────────── Internet Gateway ─┘
                        │
                 Amazon VPC
                        │
        ┌───────────────┴───────────────┐
        ▼                               ▼
  Private Subnet                  Private Subnet
        │                               │
        ▼                               ▼
      EKS Worker Nodes (EC2 Instances)
                │
                ▼
        Kubernetes Pods
```

---

## ☁️ AWS Services Used

- Amazon EKS
- Amazon EC2
- Amazon VPC
- Internet Gateway
- NAT Gateway
- Route Tables
- IAM
- Amazon S3
- DynamoDB
- Elastic IP

---

## 🛠️ Tech Stack

- Terraform
- AWS
- Kubernetes
- Git
- GitHub

---

## 📂 Project Structure

```
.
├── backend/
├── modules/
│   ├── eks/
│   └── vpc/
├── main.tf
├── variables.tf
├── outputs.tf
├── README.md
└── .gitignore
```

---

## 🚀 Deployment

Initialize Terraform

```bash
terraform init
```

Review the execution plan

```bash
terraform plan
```

Deploy infrastructure

```bash
terraform apply
```

Configure kubectl

```bash
aws eks update-kubeconfig --region us-east-1 --name my-eks-cluster
```

Verify cluster

```bash
kubectl get nodes
```

---

## 💰 Destroy Infrastructure

To avoid unnecessary AWS charges:

```bash
terraform destroy
```

---

## 📚 Skills Demonstrated

- Infrastructure as Code (Terraform)
- AWS Networking
- Amazon EKS Deployment
- Kubernetes Cluster Provisioning
- IAM Roles and Policies
- Remote Terraform State
- Terraform Modules
- Git Version Control
- Cloud Infrastructure Automation

---

## 📸 Screenshots

> Add screenshots of:

- Terraform Apply
- EKS Cluster
- kubectl get nodes
- AWS Console
- Kubernetes Pods

---

## 👨‍💻 Author

**Soham Jarad**

GitHub: https://github.com/sohamjarad
