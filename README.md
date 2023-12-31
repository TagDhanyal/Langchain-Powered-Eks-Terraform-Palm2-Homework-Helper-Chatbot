# Homework Helper Project Overview
## Project Description [![Push to ECR and Deploy to EKS](https://github.com/TagDhanyal/Langchain-Powered-Eks-Terraform-Palm2-Homework-Helper-Chatbot/actions/workflows/cd.yml/badge.svg)](https://github.com/TagDhanyal/Langchain-Powered-Eks-Terraform-Palm2-Homework-Helper-Chatbot/actions/workflows/cd.yml)
Welcome to the Homework Helper project! This application is designed to assist users with their homework questions by providing an interactive chatbot. Users can ask the chatbot anything related to their schoolwork, and it will provide helpful responses.

## Site Status
**Notice**: The Homework Helper website is currently offline due to cost considerations. I appreciate your interest and apologize for any inconvenience. If you'd like to see the site back online or have any questions, please feel free to reach out to me directly.

## Live Website
Explore the live [Homework Helper website](http://acd43e5ba4e3c4f5eaba7005e08faa42-1234218430.us-east-1.elb.amazonaws.com/) 
![Screenshot](screenshot.png)

## Technology Stack
The project utilizes the following technologies:

- **Streamlit:** A Python library for creating web applications with minimal effort.
- **PaLM (GenerativeAI):** Google's GenerativeAI powers the language model for the chatbot.
- **AWS (Amazon Web Services):**
  - **SSM (Systems Manager):** Used for securely storing and retrieving sensitive information.
  - **EKS (Elastic Kubernetes Service):** Orchestrates containerized applications using Kubernetes.
  - **ECR (Elastic Container Registry):** Stores Docker container images.
- **GitHub Actions:** Enables automated continuous deployment.

## Project Structure
The project is organized into key components:

### App Code (Python)
The main application code written in Python using Streamlit and GenerativeAI.

### Infrastructure as Code (Terraform)
Terraform scripts for provisioning AWS resources, including EKS and associated components.

### GitHub Actions Workflow (CI/CD)
Automated continuous deployment to ECR and EKS upon pushing to the master branch.

### EKS Manifests (Kubernetes)
Deployment and service manifests for running the application on EKS.

## EKS Cluster Configuration
The EKS cluster is configured with OIDC (OpenID Connect) for identity federation. This enhances security and enables integration with other AWS services.

### Files and Descriptions:
- **deployment.yaml:** Kubernetes manifest for the application deployment.
- **public-lb.yaml:** Manifest for a public LoadBalancer service.
- **private-lb.yaml:** Manifest for a private LoadBalancer service.
- **cluster-autoscaler.yaml:** Configuration for the Kubernetes Cluster Autoscaler.

## Terraform Configuration
The Terraform scripts automate the setup of the AWS infrastructure, including EKS, IAM roles, and SSM parameter store.

### Files and Descriptions:
- **ecr.tf:** Elastic Container Registry configuration.
- **eks.tf:** Defines the EKS cluster, node groups, and associated IAM roles.
- **iam-autoscaler.tf:** IAM roles for Autoscaler.
- **iam-oidc.tf:** IAM roles for OpenID Connect (OIDC) configuration.
- **iam-test.tf:** IAM roles for testing.
- **igw.tf:** Internet Gateway configuration.
- **nat.tf:** Network Address Translation (NAT) configuration.
- **node.tf:** Node group configuration.
- **outputs.tf:** Output variables definition.
- **provider.tf:** AWS provider configuration.
- **routes.tf:** Route configuration.
- **subnets.tf:** Subnet configuration.
- **vpc.tf:** Virtual Private Cloud (VPC) configuration.

### Security Highlights:
- **Internal Private Load Balancer (LB):** Ensures that sensitive components are only accessible within the internal network.
- **EKS Cluster with OIDC (OpenID Connect):** Enhances security and enables identity federation with other AWS services.
- **SSM Parameter Store:** Securely stores and retrieves sensitive information.

## To-Do for Version 2

- [   ] Implement user authentication for personalized assistance.
- [   ] Enhance the chatbot's capabilities and knowledge base.
- [   ] Integrate additional AI models or services for improved responses.
- [   ] Implement user feedback mechanisms for continuous improvement.
- [   ] Add a feature to allow users to upload images for mathematical problem solving.
