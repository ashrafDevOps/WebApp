# Node.js Dockerized Application - Hello Eyego

## Overview
This is a simple Node.js application that responds with "Hello Eyego" on the root endpoint `/`.  
The application is containerized using Docker and deployed on AWS Elastic Kubernetes Service (EKS) with automated build and deployment pipelines powered by GitHub Actions.

## Features
- Node.js Express server with a simple API endpoint `/`
- Dockerfile to create a lightweight Docker image
- AWS ECR to store container images
- Kubernetes manifests (`deployment.yaml` and `service.yaml`) for deployment and exposure
- CI/CD pipeline with GitHub Actions to build, push, and deploy automatically on each code push

## Getting Started

### Application Endpoint
- Visit the public Load Balancer URL (http://a11601044052e4b7a92a4be4946f9387-303704185.us-east-1.elb.amazonaws.com/) to see the greeting message:




##### Migration Guide: From AWS EKS to Google GKE / Alibaba Cloud Kubernetes 

### Overview 

This document outlines the essential steps and best practices for migrating your Kubernetes workloads from Amazon Elastic Kubernetes Service (EKS) to either Google Kubernetes Engine (GKE) or Alibaba Cloud Kubernetes. It covers environment assessment, resource migration, container image registry adaptation, and CI/CD pipeline adjustments. 

### 1. Environment Assessment 

Review existing Kubernetes components: Deployments, Services, Ingresses,  

Identify environment-specific configurations and dependencies. 

Understand differences between AWS EKS, Google GKE, and Alibaba Kubernetes services regarding networking, storage, and load balancing. 

##### 2. Resource Export and Adaptation 

Export current Kubernetes manifests (kubectl get all -o yaml), focusing on critical workloads. 

Modify manifests to align with the target environment: 

Update StorageClasses to use Google Persistent Disk or Alibaba Cloud Disk. 

Adjust Ingress and LoadBalancer configurations. 

Modify network settings as required. 

Update container image references: 

Retag images for Google Container Registry (GCR) or Alibaba Container Registry. 

 #### 3. Container Image Migration 

Pull Docker images from AWS ECR. 

Retag images for target registry. 

Push images to Google Container Registry or Alibaba Cloud Container Registry. 

 ##### 4. Cluster Setup on Target Cloud 

Create Kubernetes clusters on Google Cloud or Alibaba Cloud. 

Configure local kubectl context to point to new clusters. 

##### 5. Deployment on Target Cluster 

Apply updated manifests using kubectl apply. 

Validate resource creation and pod status. 

Monitor logs and troubleshoot as needed. 

##### 6. CI/CD Pipeline Update 

Adapt GitHub Actions workflows or migrate to Google Cloud Build / Alibaba Cloud Build. 

Update image build-and-push steps to new container registries. 

Modify deployment steps to target new Kubernetes clusters. 

### Conclusion 

Migrating Kubernetes workloads involves careful planning, manifest adaptation, image registry updates, and pipeline changes. Thorough testing ensures smooth transition and minimizes downtime. 

For further assistance or tailored migration plans, contact your DevOps team or cloud provider support. 

 
