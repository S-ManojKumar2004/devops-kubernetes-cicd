
# DevOps CI/CD Project – Docker, Kubernetes & Cloud

This project demonstrates an **end-to-end DevOps CI/CD pipeline** using
**Docker, Kubernetes (Minikube & AWS EKS), Terraform, Helm, Prometheus, Grafana, and GitHub Actions**.

A simple **HTML web application served via Nginx** is containerized, pushed to **Docker Hub**, deployed into a **Kubernetes cluster**, and exposed through a browser using a **LoadBalancer**.
The entire **infrastructure provisioning, build, security scanning, deployment, monitoring, and alerting** process is fully automated following **DevOps best practices**.

---

## Project Overview

This project was created to gain **hands-on, real-world DevOps experience** in:

* Containerizing applications using **Docker & Nginx**
* Writing and managing **Kubernetes YAML manifests**
* Deploying applications using **Kubernetes Deployments & Services**
* Automating CI/CD pipelines using **GitHub Actions**
* Managing Docker images using **Docker Hub**
* Provisioning cloud infrastructure using **Terraform**
* Understanding **AWS fundamentals** (EKS, EC2, VPC, Networking)
* Packaging Kubernetes applications using **Helm**
* Implementing **monitoring & observability** using Prometheus & Grafana
* Implementing **alerting & incident detection**
* Performing **security scanning using Trivy**
* Local Kubernetes testing using **Minikube**

---

##  Tools & Technologies Used

###  Containerization

* Docker
* Docker Hub
* Nginx (Web Server)

###  Kubernetes & Orchestration

* Kubernetes
* Minikube (local testing)
* AWS EKS (production)
* Kubernetes YAML (Deployment, Service)
* Helm (Kubernetes package manager)

### CI/CD & Automation

* GitHub Actions
* GitHub

### Cloud & Infrastructure

* AWS
* Terraform (Infrastructure as Code)

###  Monitoring & Observability

* Prometheus
* Grafana
* Alertmanager

### Security

* Trivy (Container image vulnerability scanning)
* Kubernetes Secrets
* GitHub Secrets
* IAM Roles & Policies

###  OS & Language

* Linux (Ubuntu)
* HTML

---

## Project Folder Structure

```
devops-kubernetes-cicd/
├── devops-d8s-project/
│   ├── Dockerfile                 # Nginx-based Docker image
│   ├── index.html                 # Sample HTML web application
│   └── k8s/
│       ├── deployment.yaml        # Kubernetes Deployment YAML
│       └── service.yaml           # Kubernetes Service YAML
│
├── helm/
│   └── hello-nginx/               # Helm chart for Kubernetes deployment
│
├── terraform/
│   ├── main.tf                    # AWS infrastructure provisioning
│   ├── variables.tf
│   └── outputs.tf
│
├── monitoring/
│   ├── prometheus.yaml            # Prometheus configuration
│   └── grafana-dashboard.json     # Grafana dashboard
│
├── .github/
│   └── workflows/
│       └── deploy.yml             # CI/CD pipeline using GitHub Actions
│
└── README.md
```

---

##  Docker & Nginx Configuration

* Application is served using **Nginx**
* Docker image is built using a **Dockerfile**
* Image is pushed to **Docker Hub**
* Versioned images are maintained (`v1`, `v2`, `latest`)

**Example Docker Image**

```
manojkumar2026/hello-nginx:v1
```

---

##  Kubernetes Configuration (YAML)

### Deployment

* Replica management
* Rolling updates
* Container port configuration
* Docker image pulled from Docker Hub

### Service

* Type: `NodePort` (Minikube)
* Type: `LoadBalancer` (AWS EKS)
* External access enabled

```yaml
kind: Deployment
kind: Service
type: NodePort
```

---

##  CI/CD Pipeline (GitHub Actions)

The CI/CD pipeline performs the following steps automatically:

1. Triggered on push to `main` branch
2. Build Docker image
3. Scan image using **Trivy**
4. Push image to **Docker Hub**
5. Deploy application to Kubernetes using `kubectl`

---

##  Secrets Management

Sensitive information is stored securely using **GitHub Repository Secrets**:

* `AWS_ACCESS_KEY_ID`
* `AWS_SECRET_ACCESS_KEY`
* `AWS_DEFAULT_REGION`
* `DOCKERHUB_USERNAME`
* `DOCKERHUB_TOKEN`
* `KUBECONFIG`

Secrets are **never hard-coded** in source files.

---

##  AWS Architecture (Terraform)

Terraform provisions and manages:

1. AWS Account & Region
2. Networking (VPC, Subnets, NAT Gateway)
3. EKS Cluster
4. Managed Node Groups (EC2)
5. IAM Roles & Policies
6. KMS Encryption
7. Kubernetes Workloads
8. Application Access via Load Balancer
9. CI/CD Integration
10. Security Scan (Trivy)

---

##  Monitoring & Alerting (Prometheus + Grafana)

### Monitoring

* Prometheus installed using **Helm**
* Grafana dashboards configured for:

  * Kubernetes Cluster
  * Nodes
  * Pods

### Alerting – High CPU Usage

* **Condition:** CPU usage > 80%
* **Scope:** Kubernetes Pods
* **Evaluation Interval:** Every 1 minute
* **Status:** Active (Normal state)

### Prometheus Target Health

All Prometheus scrape targets are **UP**:

* Grafana metrics endpoint: UP
* Alertmanager endpoints: UP
* Kubernetes API server: UP (2/2)

This confirms **ServiceMonitors are correctly configured** and metrics are actively scraped.

---

##  Observability – Prometheus TSDB

Prometheus is actively storing metrics in its **Time Series Database (TSDB)**.

TSDB Status confirms:

* 56,000+ active time series
* Metrics from nodes, pods, and system components
* Healthy head block with recent timestamps

This proves **real-time metrics collection is working correctly**

**Proof:** Screenshots attached in repository

---

## Security Enhancements

* Trivy vulnerability scanning integrated in CI/CD
* IAM least-privilege access
* Kubernetes Secrets for sensitive data
* Encrypted EKS secrets using KMS

---

## Git Commands (Final)

```bash
git status
git add README.md
git commit -m "Updated README with Terraform, AWS, Nginx, Docker Hub, Helm, Prometheus and Grafana details"
git push origin main
```

## URL(LInK) & Screenshots :

 --> GitHub Repository                   ---           https://github.com/S-ManojKumar2004/devops-kubernetes-cicd
      <img width="1835" height="593" alt="image" src="https://github.com/user-attachments/assets/f557410c-1bbe-4b89-b159-3516005b2af7" />


 --> Live Application URL               ---            http://aaefac5c099ad425ba0e7ec58a1a7cb5-1780549736.us-east-1.elb.amazonaws.com/
       <img width="1013" height="344" alt="image" src="https://github.com/user-attachments/assets/22135e06-b1bc-4685-bfa3-b70653e29297" />



--> Alternate Kubernetes Service URL     ---           http://a1e43ac63d851406486856a530ecc0b6-1851606792.us-east-1.elb.amazonaws.com/
     <img width="1845" height="295" alt="image" src="https://github.com/user-attachments/assets/8a0ad9b4-1316-4115-a852-23365c8beda7" />



--> CI/CD Pipeline                     ---            https://github.com/S-ManojKumar2004/devops-kubernetes-cicd/actions
     <img width="1656" height="997" alt="image" src="https://github.com/user-attachments/assets/aaa68555-0508-46db-902c-a917d390138f" />



 -->  Docker Image                      ---          https://hub.docker.com/r/manojkumar2026/nginx-app
      <img width="1838" height="650" alt="image" src="https://github.com/user-attachments/assets/b6480c70-a70c-4b9e-81a2-079632110d55" />




