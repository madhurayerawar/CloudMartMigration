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
Step 1: Install Docker on EC2  
Step 2: Create Docker image for CloudMart  
Step 3: Cluster setup on AWS Elastic Kubernetes Services (EKS)  
Step 4: Frontend and Backend Deployment on Kubernetes by creating an ECR repository and upload docker image to it  

🔥 Key Accomplishments:
- Containerized CloudMart using Docker, ensuring a portable and consistent environment and registering it on Amazon ECR (Elastic Container Registry).
- Deployed and orchestrated Docker containers on Amazon EKS (Elastic Kubernetes Service) for high availability and seamless scalability.
- Troubleshot challenges along the way, gaining a deeper understanding of Kubernetes networking, scaling strategies, and deployment best practices.

🌟 The Best Part?
Watching the CloudMart website come to life on an Amazon EKS cluster, running smoothly and efficiently!

### Day 3 Building CI/CD Pipeline using AWS Codebuild
In modern software development, Continuous Integration and Continuous Deployment (CI/CD) pipelines are the backbone of rapid, reliable, and automated deployments. They ensure seamless code integration, rigorous testing, and efficient delivery, reducing manual intervention and accelerating time to market.
Set up a CI/CD pipeline using 𝗔𝗪𝗦 𝗖𝗼𝗱𝗲𝗕𝘂𝗶𝗹𝗱, a fully managed build service that compiles source code, runs automated tests, and generates deployable artifacts—all without the overhead of managing infrastructure.

#### 𝗖𝗜/𝗖𝗗 𝗣𝗶𝗽𝗲𝗹𝗶𝗻𝗲 𝗜𝗺𝗽𝗹𝗲𝗺𝗲𝗻𝘁𝗮𝘁𝗶𝗼𝗻 𝗳𝗼𝗿 𝗖𝗹𝗼𝘂𝗱𝗠𝗮𝗿𝘁
⚡ The CloudMart code resides in GitHub, where AWS CodeBuild fetches the source code for building and deployment.
1. Create New Pipeline
2. Configure AWS CodeBuild to build Docker image
  2.a Create a Build Project and connect to your git repo
  2.b Add AmazonElasticContainerRegistryPublicFullAccess permission to ECR in the service role.
3. Configure AWS CodeBuild for Application Deployment
     3.a Create a Deployment Project which underneath performs kubectl commands used to deploy and configure EKS cluster
4. Test the CI/CD Pipeline by commiting some changes onto git repo and trigger pipeline
   

