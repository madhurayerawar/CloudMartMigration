# CloudMartMigration
CloudMart: AI-Driven E-Commerce Platform with MultiCloud & DevOps

## Project Overview
CloudMart is a scalable, AI-enhanced e-commerce solution built using multi-cloud infrastructure, DevOps best practices, and automation. This project demonstrates how AI-powered recommendations, seamless cloud provisioning, and automated CI/CD pipelines can enhance modern applications.

![CloudMart_SystemDesign_final](https://github.com/user-attachments/assets/c9d298ae-412e-4830-8efa-a6f4751ab909)


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

![Day 2Pushing docker build](https://github.com/user-attachments/assets/ba178cb5-b73d-4927-bb5c-74592e30b0ab)
![Day 2 -Front and Back end Imapge pushed on ECR](https://github.com/user-attachments/assets/1bfb3430-4b01-4d02-af3a-f7c7c3105439)
![Day 2 website suceessfully loaded](https://github.com/user-attachments/assets/ddb2d460-09b6-4ec1-82eb-2ec122bc0edb)

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
   
   ![Day 3 - Build Pipeline Created](https://github.com/user-attachments/assets/3600b752-d0f9-4f31-a4a7-c150fdea2be5)
   ![day 3 auto deploy started](https://github.com/user-attachments/assets/45d08671-0d8d-470e-a385-f49892d4021e)

### Day 4 Adding OpenAI powered assisstant

Implemented AI assistant to CloudMart for customer enquiries.
𝗔𝗺𝗮𝘇𝗼𝗻 𝗕𝗲𝗱𝗿𝗼𝗰𝗸 simplifies AI adoption by providing seamless access to 𝗳𝗼𝘂𝗻𝗱𝗮𝘁𝗶𝗼𝗻 𝗺𝗼𝗱𝗲𝗹𝘀 𝗳𝗿𝗼𝗺 𝘁𝗼𝗽 𝗔𝗜 𝗽𝗿𝗼𝘃𝗶𝗱𝗲𝗿𝘀, allowing businesses to build and scale generative AI applications without managing underlying infrastructure.  
𝗖𝗹𝗮𝘂𝗱𝗲 𝟯 𝗦𝗼𝗻𝗻𝗲𝘁, by Anthropic, is a powerful AI model known for its 𝗳𝗮𝘀𝘁 𝗿𝗲𝘀𝗽𝗼𝗻𝘀𝗲 𝘁𝗶𝗺𝗲𝘀, 𝗻𝘂𝗮𝗻𝗰𝗲𝗱 𝘂𝗻𝗱𝗲𝗿𝘀𝘁𝗮𝗻𝗱𝗶𝗻𝗴, 𝗮𝗻𝗱 𝗮𝗱𝘃𝗮𝗻𝗰𝗲𝗱 𝗿𝗲𝗮𝘀𝗼𝗻𝗶𝗻𝗴 𝗰𝗮𝗽𝗮𝗯𝗶𝗹𝗶𝘁𝗶𝗲𝘀, making it ideal for customer interactions, recommendations, and data analysis.  
𝗢𝗽𝗲𝗻𝗔𝗜 𝗚𝗣𝗧-𝟰𝗼 takes AI assistance to the next level with 𝗺𝘂𝗹𝘁𝗶-𝗺𝗼𝗱𝗮𝗹 𝗰𝗮𝗽𝗮𝗯𝗶𝗹𝗶𝘁𝗶𝗲𝘀, 𝗿𝗲𝗮𝗹-𝘁𝗶𝗺𝗲 𝗿𝗲𝘀𝗽𝗼𝗻𝘀𝗲𝘀, 𝗮𝗻𝗱 𝗲𝗻𝗵𝗮𝗻𝗰𝗲𝗱 𝗮𝗰𝗰𝘂𝗿𝗮𝗰𝘆, offering businesses an intelligent, adaptable, and highly conversational AI-powered assistant.  

##### 𝗔𝗺𝗮𝘇𝗼𝗻 𝗕𝗲𝗱𝗿𝗼𝗰𝗸 𝗔𝗴𝗲𝗻𝘁 𝗦𝗲𝘁𝘂𝗽:
1. 𝗣𝗿𝗼𝘃𝗶𝘀𝗶𝗼𝗻𝗲𝗱 𝗶𝗻𝗳𝗿𝗮𝘀𝘁𝗿𝘂𝗰𝘁𝘂𝗿𝗲 using Terraform to automate IAM roles, policies, Bedrock Agent permissions, and Lambda function ARNs.
2. 𝗖𝗼𝗻𝗳𝗶𝗴𝘂𝗿𝗲𝗱 𝗔𝗺𝗮𝘇𝗼𝗻 𝗕𝗲𝗱𝗿𝗼𝗰𝗸 𝗔𝗴𝗲𝗻𝘁:
      - Requested access to the Claude 3 Sonnet Model.
      - Created an AI Agent and selected Claude 3 Sonnet as the base model.
      - Designed a structured set of 𝗶𝗻𝘀𝘁𝗿𝘂𝗰𝘁𝗶𝗼𝗻𝘀 to guide the agent’s responses and workflow.
3. 𝗦𝗲𝘁 𝘂𝗽 𝗜𝗔𝗠 𝗽𝗲𝗿𝗺𝗶𝘀𝘀𝗶𝗼𝗻𝘀 for the Bedrock Agent to invoke Lambda functions and the 𝗖𝗹𝗮𝘂𝗱𝗲 𝟯 𝗦𝗼𝗻𝗻𝗲𝘁 𝗺𝗼𝗱𝗲𝗹.
4. 𝗖𝗿𝗲𝗮𝘁𝗲𝗱 𝗮𝗻 𝗔𝗰𝘁𝗶𝗼𝗻 𝗚𝗿𝗼𝘂𝗽, defining API schemas and linking the Lambda function as the executor.
5. 𝗧𝗲𝘀𝘁𝗲𝗱 𝘁𝗵𝗲 𝗔𝗜 𝗔𝗴𝗲𝗻𝘁 to ensure it retrieves data from the API and provides accurate product recommendations.

##### 𝗢𝗽𝗲𝗻𝗔𝗜 𝗔𝘀𝘀𝗶𝘀𝘁𝗮𝗻𝘁 𝗳𝗼𝗿 𝗖𝘂𝘀𝘁𝗼𝗺𝗲𝗿 𝗦𝘂𝗽𝗽𝗼𝗿𝘁:
1. 𝗖𝗿𝗲𝗮𝘁𝗲𝗱 𝗮 𝗚𝗣𝗧-𝟰𝗼 𝗮𝘀𝘀𝗶𝘀𝘁𝗮𝗻𝘁 for CloudMart’s customer support.
2. Defined its role to handle 𝗰𝘂𝘀𝘁𝗼𝗺𝗲𝗿 𝗶𝗻𝗾𝘂𝗶𝗿𝗶𝗲𝘀, 𝗼𝗿𝗱𝗲𝗿 𝗶𝘀𝘀𝘂𝗲𝘀, 𝗮𝗻𝗱 𝗴𝗲𝗻𝗲𝗿𝗮𝗹 𝗮𝘀𝘀𝗶𝘀𝘁𝗮𝗻𝗰𝗲 with friendly and professional responses.
3. Enabled the 𝗖𝗼𝗱𝗲 𝗜𝗻𝘁𝗲𝗿𝗽𝗿𝗲𝘁𝗲𝗿 capability for troubleshooting technical issues.

##### 𝗙𝗶𝗻𝗮𝗹 𝗗𝗲𝗽𝗹𝗼𝘆𝗺𝗲𝗻𝘁:
1. Integrated the 𝗮𝘀𝘀𝗶𝘀𝘁𝗮𝗻𝘁 𝗜𝗗𝘀 𝗮𝗻𝗱 𝗮𝗰𝗰𝗲𝘀𝘀 𝗸𝗲𝘆𝘀 into the CloudMart backend.
2. Deployed updates to the 𝗞𝘂𝗯𝗲𝗿𝗻𝗲𝘁𝗲𝘀 𝗖𝗹𝘂𝘀𝘁𝗲𝗿 using 𝘬𝘶𝘣𝘦𝘤𝘵𝘭 𝘢𝘱𝘱𝘭𝘺 -𝘧 𝘤𝘭𝘰𝘶𝘥𝘮𝘢𝘳𝘵-𝘣𝘢𝘤𝘬𝘦𝘯𝘥.𝘺𝘢𝘮𝘭

The 𝗔𝗜 𝗮𝘀𝘀𝗶𝘀𝘁𝗮𝗻𝘁𝘀 𝗮𝗿𝗲 𝗻𝗼𝘄 𝗹𝗶𝘃𝗲, responding politely and efficiently! 
![day 4 open AI assistant configured](https://github.com/user-attachments/assets/d06be7e1-4602-43f2-a300-2bc8a5cd9a26)
![Day 4 Order Cancelled](https://github.com/user-attachments/assets/59ef930d-675c-4a86-939a-cdc98060b42f)


