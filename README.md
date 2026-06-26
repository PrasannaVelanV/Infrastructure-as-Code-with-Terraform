# AWS 3-Tier Architecture using Terraform

![Terraform](https://img.shields.io/badge/Terraform-IaC-blueviolet?logo=terraform)
![AWS](https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Linux-E95420?logo=ubuntu)
![Apache](https://img.shields.io/badge/Apache-Web_Server-D22128?logo=apache)

## 📖 Project Overview

This project demonstrates the implementation of a complete **AWS 3-Tier Architecture** using **Terraform** as an **Infrastructure as Code (IaC)** tool.

The infrastructure automates the provisioning and management of AWS resources, including networking, compute, storage, database, and security components. Terraform enables consistent, reusable, scalable, and efficient cloud deployments.

---

## 🏗️ Architecture Diagram


![AWS 3-Tier Architecture](https://raw.githubusercontent.com/PrasannaVelanV/Infrastructure-as-Code-with-Terraform/main/Architecure%20Diagram%20-%20Infrastructure%20as%20Code%20with%20Terraform%20or%20CloudFormation.png)
---

## 🚀 Architecture Components

### Networking Layer
- Custom Virtual Private Cloud (VPC)
- Public Subnet
- Private Subnet
- Internet Gateway (IGW)
- Public and Private Route Tables
- Security Groups

### Presentation Layer (Web Tier)
- Ubuntu EC2 Instance
- Apache Web Server
- Custom HTML Website
- Public access through HTTP and SSH

### Database Layer
- Amazon RDS MySQL Instance
- Deployed inside a Private Subnet
- Database access restricted through Security Groups

### Storage Layer
- Amazon S3 Bucket
- IAM Role for secure S3 access from EC2

---

## 🛠️ AWS Services Used

| Service | Purpose |
|----------|---------|
| Amazon VPC | Provides isolated networking environment |
| Amazon EC2 | Hosts the web application |
| Amazon RDS | Stores application data |
| Amazon S3 | Object storage service |
| AWS IAM | Secure access management |
| Security Groups | Controls network traffic |
| Internet Gateway | Enables internet connectivity |
| Route Tables | Manages routing within VPC |
| Terraform | Automates infrastructure provisioning |

---

## ✨ Features

- Automated infrastructure deployment using Terraform
- Custom VPC with public and private subnets
- EC2 instance deployment with Apache Web Server
- Custom HTML website hosting
- Amazon RDS MySQL database deployment
- Amazon S3 integration using IAM Roles
- Secure communication using Security Groups
- Complete Infrastructure as Code implementation

---

## 📂 Project Structure

```bash
Infrastructure-as-Code-with-Terraform/
│
├── Screenshots/
│
├── aws-3tier-terraform-project/
│   ├── main.tf
│   ├── provider.tf
│   ├── variables.tf
│   ├── terraform.tfvars
│   ├── outputs.tf
│   ├── terraform.tfstate
│   ├── terraform.tfstate.backup
│   └── .terraform.lock.hcl
├── Infrastructure-as-Code-with-Terraform.pdf
└── README.md
```

---

## 🔐 Security Implementation

- EC2 instance deployed in a Public Subnet.
- RDS database deployed in a Private Subnet.
- HTTP (Port 80) enabled for web access.
- SSH (Port 22) enabled for administration.
- MySQL access (Port 3306) restricted to the EC2 Security Group only.
- IAM Roles are used to provide secure access to Amazon S3.

---

## ⚙️ Prerequisites

Before deploying the infrastructure, ensure the following tools are installed:

- AWS Account
- AWS CLI
- Terraform
- Git

Verify installations:

```bash
aws --version
terraform --version
git --version
```

---

## 🚀 Deployment Steps

### Clone the Repository

```bash
git clone https://github.com/PrasannaVelanV/Infrastructure-as-Code-with-Terraform.git
```

```bash
cd Infrastructure-as-Code-with-Terraform/aws-3tier-terraform-project
```

### Initialize Terraform

```bash
terraform init
```

### Validate Configuration

```bash
terraform validate
```

### Review Execution Plan

```bash
terraform plan
```

### Deploy Infrastructure

```bash
terraform apply
```

Type:

```bash
yes
```

---

## 📤 Terraform Outputs

After successful deployment, Terraform displays outputs such as:

- EC2 Public IP Address
- RDS Endpoint
- S3 Bucket Name

---

## 🧰 Common Terraform Commands

```bash
terraform init
terraform fmt
terraform validate
terraform plan
terraform apply
terraform destroy
```

---

## 🎯 Skills Demonstrated

- Infrastructure as Code (IaC)
- Terraform
- AWS Networking
- Amazon EC2
- Amazon RDS
- Amazon S3
- IAM Roles and Policies
- Cloud Security
- Infrastructure Automation
- Cloud Architecture Design

---

## 🔮 Future Enhancements

- Add Application Load Balancer (ALB)
- Implement Auto Scaling Group (ASG)
- Configure Remote Backend using S3
- Integrate GitHub Actions CI/CD Pipeline
- Enable CloudWatch Monitoring
- Modularize Terraform code

---

## 🧹 Clean Up

To avoid unnecessary AWS charges, destroy all created resources when no longer needed.

```bash
terraform destroy
```

---

## 👨‍💻 Author

### Prasanna Velan

- GitHub: https://github.com/PrasannaVelanV
- LinkedIn: [www.linkedin.com/in/prasannavelanv](https://www.linkedin.com/in/prasanna-velan-v/)
- Portfolio: [https://github.com/PrasannaVelanV](https://prasannavelanv.netlify.app/)

---

## ⭐ Support

If you found this project helpful, please give this repository a ⭐ on GitHub.
