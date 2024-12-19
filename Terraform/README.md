
# ONPK Final Project - Kubernetes Infrastructure

## Overview
This project sets up a Kubernetes cluster in Azure using Terraform, integrates CI/CD pipelines with Tekton, and deploys applications with Helm and FluxCD.

## Components
1. **Terraform Infrastructure**:
   - Azure Virtual Network (VNet)
   - Azure Kubernetes Service (AKS)
   - Azure Container Registry (ACR)

2. **Tekton Pipelines**:
   - CI pipeline for building and pushing Docker images.
   - CD pipeline for deploying applications to the AKS cluster.

3. **FluxCD**:
   - Automates deployment of Helm charts using GitOps.

## Instructions
1. Clone the repository and navigate to the `terraform` folder.
2. Initialize Terraform: `terraform init`.
3. Apply the configuration: `terraform apply`.
4. Deploy Tekton pipelines:
   - Navigate to `tekton_pipelines` and apply the CI and CD pipelines.
   - `kubectl apply -f ci-pipeline-build-push.yaml`
   - `kubectl apply -f cd-pipeline-deployment.yaml`

5. Use FluxCD for continuous deployment.

## Notes
- Ensure Azure CLI is installed and authenticated.
- Adjust variables in the `terraform` folder to fit your environment.

Enjoy your automated Kubernetes deployment!
