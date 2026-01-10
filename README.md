## DevOps CI/CD Project – Docker, Kubernetes & Cloud

This project demonstrates an **end-to-end DevOps CI/CD pipeline** using  
**Docker, Kubernetes (Minikube), AWS, Terraform, Helm, Prometheus, Grafana, and GitHub Actions**.

A simple **HTML web application served via Nginx** is containerized, pushed to **Docker Hub**, deployed into a **Kubernetes cluster**, and exposed through a browser.  
The entire infrastructure provisioning, build, and deployment process is automated following DevOps best practices.

---

##  Project Overview

This project was created to gain **hands-on, real-world DevOps experience** in:

- Containerizing applications using **Docker & Nginx**
- Writing and managing **Kubernetes YAML manifests**
- Deploying applications using **Kubernetes Deployments & Services**
- Automating CI/CD pipelines using **GitHub Actions**
- Managing Docker images using **Docker Hub**
- Provisioning cloud infrastructure using **Terraform**
- Understanding **AWS fundamentals** (EC2, networking concepts)
- Packaging Kubernetes applications using **Helm**
- Implementing monitoring and observability using **Prometheus & Grafana**
- Local Kubernetes testing using **Minikube**

---

 Tools & Technologies Used

 

 **Containerization**
- Docker
- Docker Hub
- Nginx (Web Server)



 **Kubernetes & Orchestration**
- Kubernetes
- Minikube
- Kubernetes YAML (Deployment, Service)
- Helm (Kubernetes package manager)



###  CI/CD & Automation
- GitHub Actions
- GitHub


###  Cloud & Infrastructure
- AWS
- Terraform (Infrastructure as Code)


###  Monitoring & Observability
- Prometheus
- Grafana


###  OS & Language
- Linux (Ubuntu)
- HTML

---

 
 --->         Project Folder Structure




devops-kubernetes-cicd/
├── devops-k8s-project/
│ ├── Dockerfile # Nginx-based Docker image
│ ├── index.html # Sample HTML web application
│ └── k8s/
│ ├── deployment.yaml # Kubernetes Deployment YAML
│ └── service.yaml # Kubernetes Service YAML
│
├── helm/
│ └── hello-nginx/ # Helm chart for Kubernetes deployment
│
├── terraform/
│ ├── main.tf # AWS infrastructure provisioning
│ ├── variables.tf
│ └── outputs.tf
│
├── monitoring/
│ ├── prometheus.yaml # Prometheus configuration
│ └── grafana-dashboard.json # Grafana dashboard
│
├── .github/
│ └── workflows/
│ └── deploy.yml # CI/CD pipeline using GitHub Actions
│
└── README.md




---

## Docker & Nginx Configuration

- Application is served using **Nginx**
- Docker image is built using a **Dockerfile**
- Image is pushed to **Docker Hub**
- Versioned images (v1, v2, latest) are used

Example Docker image:

manojkumar2026/hello-nginx:v1

---

##  Kubernetes Configuration (YAML)

- **Deployment YAML**
  - Replica management
  - Container port configuration
  - Docker image pulled from Docker Hub

- **Service YAML**
  - NodePort service
  - External access using Minikube

Example:
```yaml
kind: Deployment
kind: Service
type: NodePort


---

## Git Commands (Final)

```bash
git status
git add README.md
git commit -m "Updated README with Terraform, AWS, Nginx, Docker Hub, Helm, Prometheus and Grafana details"
git push origin main


 ***   secert managements 
       security Enhancements
       AWS EKS , Load Balancer
       Helm templates 
       Prometheus,Grafana    ***


##   AWS --         

         1. Project Overview
         2. AWS Account & Region
         3. Networking (VPC, Subnets, NAT)
         4. EKS Cluster
         5. Node Groups & EC2
         6. IAM & Security
         7. KMS Encryption
         8. Kubernetes Workloads
         9. Application Access
         10. CI/CD Pipeline
         11. Security Scan (Trivy)
         12. Final Summary

                                        
       






 




























