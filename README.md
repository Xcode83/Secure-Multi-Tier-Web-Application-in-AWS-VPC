# Secure-Multi-Tier-Web-Application-in-AWS-VPC
Secure Multi-Tier Web App Deployment in AWS Using Terraform

Tech Stack: Terraform • AWS VPC • EC2 • RDS MySQL • ALB • Bastion Host • CloudWatch

📌 Overview

This project builds a secure 3-tier AWS architecture using Terraform — designed for production-grade web applications.
The setup includes a public tier, application tier, and database tier, along with monitoring and secure admin access.

🎯 Features

🏛️ Fully automated VPC provisioning using Terraform

🔐 Public Subnet → ALB + Bastion Host

🔒 Private Subnet → EC2 App Servers

🗄️ DB Subnet → RDS MySQL (Secure, not publicly accessible)

🛡️ Security Groups + NACL hardening

🧩 Parameterized Terraform modules

📊 CloudWatch monitoring + alarms

🚀 AutoScaling-ready architecture

🛠 Architecture Overview

Public Subnets

Application Load Balancer

Bastion Host (SSH access via Key Pair)

Private App Subnets

EC2 instances running the web application

Private DB Subnets

RDS MySQL with Multi-AZ support

📂 Project Structure
/aws-multi-tier-terraform
│── main.tf
│── variables.tf
│── outputs.tf
│── modules/
│     ├── vpc/
│     ├── ec2/
│     ├── rds/
│     └── security-groups/
│── README.md

🔧 Deployment Steps

Install Terraform

Configure AWS credentials

Run:

terraform init
terraform plan
terraform apply


App becomes reachable through ALB DNS

Admin accesses servers only via Bastion

🛡 Security Highlights

Private subnets have no internet exposure

Bastion uses restricted IP whitelist

DB accessible only from App Layer SG

Encryption at rest + in-transit enabled

🔧 Future Enhancements (Planned)

Add Auto Scaling Group

Add Terraform Cloud CI/CD pipeline

Add SSM Session Manager (replace SSH)

📄 Status

📌 Project repo created — code upload in progress.
