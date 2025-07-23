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
