# Orchestration Tools for Containers - Final Assignment

This repository contains the solutions for the ONPK-Final Assignment of the course "Orchestration Tools for Containers". The work demonstrates the deployment of a microservices-based application with a frontend, backend, and MongoDB, leveraging modern DevOps practices.

## Structure

The repository is organized into the following directories:

### 1. **Docker**
   - Contains Docker configurations and Dockerfiles for both the backend and frontend applications.
   - Subdirectories:
     - **BackEnd**: Dockerfile and related resources for the backend service.
     - **FrontEnd**: Dockerfile and related resources for the frontend service.

### 2. **Helm**
   - Contains Helm charts for deploying the frontend and backend services, along with MongoDB.
   - Supports environment customization via `values-onpkapp.yaml`.

### 3. **CI/CD**
   - Tekton pipelines for automating the build and deployment processes.
   - Includes secrets and RBAC configurations necessary for pipelines.
   - Demonstrates CI/CD best practices using Tekton and FluxCD.

### 4. **Terraform**
   - Infrastructure as Code (IaC) using Terraform to provision resources in Microsoft Azure.
   - Modules include Azure Kubernetes Service (AKS), Azure Container Registry (ACR), and Virtual Network.

## Objectives

The main objectives of the assignment are:
1. **Dockerization**: Containerizing frontend and backend applications.
2. **Helm Deployment**: Using Helm charts to automate Kubernetes deployments.
3. **CI/CD Pipelines**: Automating build and deployment using Tekton pipelines.
4. **Cloud Infrastructure**: Provisioning Azure infrastructure using Terraform.

## Key Features

- **Docker**: Efficient containerization of applications.
- **Helm Charts**: Modular, reusable configurations for Kubernetes deployments.
- **Tekton Pipelines**: CI/CD pipelines that automate Docker builds and Kubernetes deployments.
- **Terraform**: Scalable and reproducible cloud infrastructure.
- **DevOps Principles**: Emphasis on automation, high availability, and security.

## Getting Started

### Prerequisites

- Docker
- Kubernetes (Minikube or Azure AKS)
- Helm 3+
- Tekton Pipelines
- Terraform

### Steps

1. **Docker**: Navigate to the `Docker` directory, build the images for both backend and frontend, and push them to Docker Hub.
2. **Helm**: Use the Helm charts in the `Helm` directory to deploy the services.
3. **CI/CD**: Set up the Tekton pipelines for building and deploying your images.
4. **Terraform**: Deploy Azure infrastructure by running the Terraform scripts in the `Terraform` directory.

## Notes

- Make sure to configure `values.yaml` files for Helm deployments.
- Update credentials in the secrets files for Tekton pipelines.
- Verify the MongoDB initialization scripts before deployment.
- Document your changes and configurations in the relevant directories.

## Contact

For any questions or clarifications, please reach out via the course communication channels