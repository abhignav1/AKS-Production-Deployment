# AKS Production Deployment

A production grade Azure Kubernetes Service (AKS) 
deployment built using Terraform for infrastructure 
provisioning, Kubernetes for container orchestration, 
and Azure DevOps for fully automated CI/CD pipeline 
automation. This project demonstrates end to end 
DevOps practices from infrastructure setup to 
production deployment.

## What this project does

Provisions and manages a fully automated AKS cluster 
on Microsoft Azure — from infrastructure setup to 
container deployment — using Infrastructure as Code 
and automated pipelines. The project eliminates manual 
infrastructure management by defining everything as 
code — meaning environments can be reproduced 
identically every single time with zero manual 
configuration.

## Tech stack

- **Terraform** — provisions AKS cluster, networking, 
  and storage on Azure using Infrastructure as Code
- **Kubernetes** — manages containerized application 
  deployments, scaling, and service availability
- **Azure DevOps Pipeline** — automates the full build 
  and deployment workflow from code push to production
- **Azure Storage** — stores Terraform state remotely 
  so the entire team shares the same infrastructure state
- **Terraform Modules** — reusable infrastructure 
  components for clean and maintainable IaC

## Project structure

- `main.tf` — core AKS cluster infrastructure 
  definition including node pools and networking
- `variables.tf` — all configurable input variables 
  keeping the code environment agnostic
- `storage.tf` — Azure storage account for remote 
  Terraform state management
- `terraform.tfvars` — environment specific variable 
  values for the deployment
- `modules/` — reusable Terraform modules for 
  modular infrastructure management
- `k8s-deployment.yaml` — Kubernetes deployment 
  manifest defining pods, replicas, and container specs
- `k8-service.yaml` — Kubernetes service manifest 
  for exposing the application and managing traffic
- `azure-pipeline.yaml` — Azure DevOps CI/CD pipeline 
  definition automating build and deployment stages

## How it works

1. **Infrastructure provisioning** — Terraform reads 
   the configuration files and provisions the AKS 
   cluster on Azure including networking, node pools, 
   and storage
2. **State management** — Terraform state is stored 
   remotely in Azure Storage so all team members work 
   from the same infrastructure state
3. **Pipeline trigger** — Azure DevOps pipeline 
   triggers automatically on every code push
4. **Build stage** — pipeline builds the Docker image 
   and runs automated tests
5. **Deploy stage** — validated image is deployed to 
   AKS using Kubernetes deployment manifests
6. **Service exposure** — Kubernetes service manages 
   traffic routing and load balancing to running pods
7. **Scaling** — Kubernetes automatically scales pods 
   based on demand without manual intervention

## Key DevOps practices demonstrated

- **Infrastructure as Code** — all infrastructure 
  defined in Terraform, version controlled, and 
  reproducible
- **Remote state management** — team wide shared 
  Terraform state prevents conflicts and drift
- **Automated deployments** — zero manual steps from 
  code push to production deployment
- **Modular infrastructure** — reusable Terraform 
  modules for clean and maintainable code
- **Container orchestration** — Kubernetes manages 
  availability, scaling, and self healing automatically

## Background

This project is based on real world experience 
managing Azure cloud infrastructure and Kubernetes 
container orchestration at Tata Consultancy Services — 
working on a large automotive enterprise client where 
containerizing microservices at scale required a 
reliable, fully automated deployment pipeline. As the 
number of microservices grew, moving from manual 
deployments to a Terraform provisioned AKS cluster 
with automated CI/CD became essential for maintaining 
reliability and release efficiency.
