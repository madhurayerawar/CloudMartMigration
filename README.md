# CloudMartMigration
CloudMart: AI-Driven E-Commerce Platform with MultiCloud & DevOps

## Project Overview
CloudMart is a scalable, AI-enhanced e-commerce solution built using multi-cloud infrastructure, DevOps best practices, and automation. This project demonstrates how AI-powered recommendations, seamless cloud provisioning, and automated CI/CD pipelines can enhance modern applications.

## Project Breakdown

### Day 1 Utilized Terraform, AWS and automation using Claude (AI assistant) 
Infrastructure as Code (IaC) tools allow infrastructure management through config files instead of a graphical interface, ensuring consistency, safety, and repeatability. Terraform is HashiCorp's IaC tool that defines and manages infrastructure using human-readable config files. 
- Terraform files support Multi-Cloud (AWS, Azure, GCP etc.)
- Provides State Tracking of resource lifecycle - State File tracks
- Infrastructure changes
- Version Control integration for collaboration using GitHub, GitLabs
- Providers - They interact with Cloud Services via APIs
- Modules - Enable reusability and standardization

Terraform Workflow involves:
1. Scope - Define Infrastructure Requirements
2. Author - Write Configuration files
3. Initialize - Install required plugins
4. Plan - Preview changes before applying
5. Apply - Deploy Infrastructure in fraction of time

👉 New to Terraform? Don't worry we can leverage Claude a Large Language Model (LLM) trained to be helpful and harmless AI assistant. We talk to Claude using "Prompts". Prompts could be as simple as you are talking to your coworker.

#### Steps Performed
1. Leveraged AWS EC2 instance to install Terraform 
2. Generated Terraform code using Claude to create General Purpose S3 Bucket and DynamoDB Tables
3. Initialized Terraform using commands - terraform init
4. Reviewed the Terraform plan using command - terraform plan
5. Applied the configuration using the command - terraform apply

### Day 2 Mastering Containerization & Orchestration: CloudMart on Amazon EKS
-Step 1: Install Docker on EC2
-Step 2: Create Docker image for CloudMart
-Step 3: Cluster setup on AWS Elastic Kubernetes Services (EKS)
-Step 4: Frontend and Backend Deployment on Kubernetes by creating an ECR repository and upload docker image to it




