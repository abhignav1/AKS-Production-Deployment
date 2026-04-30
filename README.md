# AKS Production Deployment

A production grade Azure Kubernetes Service deployment 
built using Terraform for infrastructure provisioning 
and Azure DevOps for CI/CD pipeline automation.

## What this project does

Provisions and manages a fully automated AKS cluster 
on Microsoft Azure — from infrastructure setup to 
container deployment — using Infrastructure as Code 
and automated pipelines.

## Tech stack

- **Terraform** — provisions AKS cluster, networking 
  and storage on Azure
- **Kubernetes** — manages containerized application 
  deployments and services  
- **Azure DevOps Pipeline** — automates build and 
  deployment workflow
- **Azure Storage** — remote Terraform state management

## Project structure

- `main.tf` — AKS cluster and core infrastructure
- `variables.tf` — configurable input variables
- `storage.tf` — Azure storage for Terraform state
- `modules/` — reusable Terraform modules
- `k8s-deployment.yaml` — Kubernetes deployment config
- `k8-service.yaml` — Kubernetes service config
- `azure-pipeline.yaml` — CI/CD pipeline definition

## Background

Based on real world experience managing Azure cloud 
infrastructure and Kubernetes container orchestration 
at TCS — where containerizing microservices at scale 
required a reliable automated deployment pipeline.
