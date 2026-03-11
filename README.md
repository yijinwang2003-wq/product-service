# Product Service
Release version 1.0.0
REST API service responsible for managing the product catalog in the e-commerce platform.

## Tech Stack
- Python
- Docker
- Jenkins
- Kubernetes

## Project Structure
src/ application source code
tests/ automated tests
config/ configuration files
Dockerfile container build file
Jenkinsfile CI/CD pipeline


## How to Run

Build docker image: docker build -t product-service .
Run container: docker run -p 5000:5000 product-service

## Git Workflow

This repository follows the **Git Flow branching strategy**:

- main → production-ready code
- develop → integration branch
- feature/* → new feature development
- release/* → preparing production release
- hotfix/* → urgent production fixes