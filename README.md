# DevOps CI/CD Project – Docker & Kubernetes

This project was created to practice Docker containerization and Kubernetes deployment using Minikube.
A simple HTML application is containerized and deployed to a Kubernetes cluster and accessed through a browser.

---

## Project Summary

- Created a basic HTML web application
- Built a Docker image for the application
- Deployed the application using Kubernetes Deployment
- Exposed the application using a NodePort Service
- Verified the deployment through browser access

---

## Tools Used

- Docker
- Kubernetes
- Minikube
- HTML
- GitHub
- Linux (Ubuntu)

---

## Folder Structure

devops-kubernetes-cicd/
├── devops-d8s-project/
│ ├── Dockerfile
│ ├── index.html
│ └── k8s/
│ ├── deployment.yaml
│ └── service.yaml
├── .github/workflows/
│ └── ci.yml

---


## How the Application Was Deployed

### Step 1: Start Minikube
```bash
minikube start

docker build -t manoj-nginx .

kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

kubectl get pods
kubectl get svc


minikube service nginx-service


http://<minikube-ip>:<nodeport>      http://192.168.49.2:30007



Hello World
Deployed using Docker & Kubernetes
CI/CD Project by Manoj


What I Learned

How to containerize an application using Docker

How Kubernetes Deployments and Services work

How to expose applications using NodePort

Basic understanding of CI/CD workflow concepts

<img width="996" height="89" alt="image" src="https://github.com/user-attachments/assets/f2b6204a-15fc-4008-a385-932cf637ab0d" />
<img width="1000" height="106" alt="image" src="https://github.com/user-attachments/assets/cb9011fc-8fa7-4aed-81f2-4c49ad5d3ab1" />
<img width="1224" height="112" alt="image" src="https://github.com/user-attachments/assets/fff859cc-4b6d-4d66-b677-fc607a4ee44b" />
<img width="1269" height="103" alt="image" src="https://github.com/user-attachments/assets/00b84994-cc2e-4eef-9ea2-f989464fbaf4" />
<img width="680" height="309" alt="image" src="https://github.com/user-attachments/assets/a61b1b08-2a6a-42a2-81f3-4b2380d1d03c" />














