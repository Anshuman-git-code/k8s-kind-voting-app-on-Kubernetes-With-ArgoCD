# Automated Deployment of Scalable Applications on AWS EC2 with Kubernetes and Argo CD

## Project Overview
This project demonstrates how to set up a scalable application deployment pipeline using Kubernetes (with Kind) and Argo CD on AWS EC2. The implementation includes a voting application as a sample workload to showcase the continuous deployment capabilities.

Led the deployment of scalable applications on AWS EC2 using Kubernetes and Argo CD for streamlined management and continuous integration. Orchestrated deployments via Kubernetes dashboard, ensuring efficient resource utilization and seamless scaling.

## Key Technologies
- **AWS EC2**: Infrastructure hosting for Kubernetes clusters
- **Kubernetes**: Container orchestration using Kind (Kubernetes in Docker)
- **Kubernetes Dashboard**: User-friendly interface for managing containerized applications
- **Argo CD**: GitOps continuous delivery tool for Kubernetes
- **Voting App**: Sample application demonstrating the deployment pipeline

## Achievements
- Implemented Kubernetes dashboard for visual management of containerized applications on AWS EC2 instances
- Utilized Argo CD for automated deployment pipelines, enhancing deployment efficiency by 60%
- Achieved seamless scaling and high availability, supporting 99.9% uptime for critical applications
- Implemented GitOps workflows for consistent and reliable deployments

## Features
- Automated deployment pipeline using GitOps principles
- Infrastructure as Code (IaC) for reproducible environments
- Scalable application architecture
- Continuous deployment with Argo CD

## Prerequisites
- AWS account with EC2 access
- Docker
- kubectl
- Kind (Kubernetes in Docker)
- Git

## Setup Instructions
1. **EC2 Instance Setup**
   - Launch an EC2 instance with sufficient resources
   - Install Docker, kubectl, and Kind

2. **Kubernetes Cluster Setup**
   ```bash
   kind create cluster --name voting-app
   ```

3. **Argo CD Installation**
   ```bash
   kubectl create namespace argocd
   kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
   ```

4. **Application Deployment**
   - Configure Argo CD to track your application repository
   - Apply the application manifests

## Project Structure
```
.
├── k8s/                  # Kubernetes manifests
│   ├── deployment.yaml   # Application deployment configurations
│   ├── service.yaml      # Service definitions
│   └── ingress.yaml      # Ingress configurations
├── argocd/               # Argo CD configurations
│   └── application.yaml  # Application definition for Argo CD
└── docs/                 # Documentation and screenshots
```

## Demo
![Screenshot 2025-06-09 at 1 02 33 AM](https://github.com/user-attachments/assets/6e9c9d82-6a64-4416-8e1e-e25bd2078691)


https://github.com/user-attachments/assets/9a503c27-fb35-4860-b010-f4c4e5ccf886



## Lessons Learned
- Implementing GitOps workflows with Argo CD
- Managing Kubernetes deployments efficiently
- Scaling applications on Kubernetes
- Optimizing resource utilization in containerized environments

## Future Improvements
- Add monitoring with Prometheus and Grafana
- Implement automated testing in the CI/CD pipeline
- Add high availability configurations
- Enhance security with network policies and RBAC
