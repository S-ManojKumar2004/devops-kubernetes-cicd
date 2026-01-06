# DevOps CI/CD Project – Docker & Kubernetes

This project demonstrates hands-on practice with Docker containerization and Kubernetes deployment using Minikube.  
A simple HTML web application is containerized, deployed to a Kubernetes cluster, and accessed through a browser.  
The project also includes an automated CI/CD pipeline implemented using GitHub Actions.

---

## Project Summary

- Developed a basic HTML web application
- Containerized the application using Docker
- Deployed the application using Kubernetes Deployment and Service
- Exposed the application locally using a NodePort Service
- Implemented CI/CD automation using GitHub Actions
- Verified application availability through browser access

---

## Tools Used

- Docker
- Kubernetes
- Minikube
- GitHub Actions
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
├── .github/
│ └── workflows/
│ └── deploy.yml


---

## How the Application Was Deployed

### Step 1: Start Minikube
```bash
minikube start
Step 2: Build Docker Image
docker build -t manoj-nginx .


Step 3: Deploy to Kubernetes
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml

Step 4: Verify Deployment
kubectl get pods
kubectl get svc

Step 5: Access the Application
minikube service nginx-service

Application URL (Local)
http://192.168.49.2:30007


CI/CD Configuration
.github/workflows/deploy.yml


Sample Output

Hello World
Deployed using Docker & Kubernetes
CI/CD Project by Manoj

github-actions-success.png

<img width="1655" height="554" alt="image" src="https://github.com/user-attachments/assets/23e01cc2-9a83-41fa-9704-8af8717da6ec" />

dockerhub-image.png

<img width="810" height="222" alt="image" src="https://github.com/user-attachments/assets/1ef3cdeb-7694-4800-932a-2d7ef5513644" />


 Docker Image Local Verification
<img width="1047" height="74" alt="image" src="https://github.com/user-attachments/assets/e0f0eaca-57da-46d5-9fb1-56792201859b" />
tag v1 


 Kubernetes Deployment YAML (Proof of config)
<img width="1045" height="495" alt="image" src="https://github.com/user-attachments/assets/29c0763e-7ebf-442b-9936-1410bfa3d64f" />

image: manojkumar2026/hello-nginx:v1
replicas
containerPort

Kubernetes Service YAML
<img width="940" height="300" alt="image" src="https://github.com/user-attachments/assets/70fe9617-5eda-406c-91ab-5bde004f0031" />
type: NodePort
nodePort: 30007

Pods Running (Live Proof)

<img width="884" height="94" alt="image" src="https://github.com/user-attachments/assets/135a53ae-1e32-4780-9e11-5d8c1273b218" />

minikube get svc
<img width="916" height="134" alt="image" src="https://github.com/user-attachments/assets/0060ef7d-d7e7-4150-b042-2e24bc497caf" />


Access Application :

minikube service hello-service


create output :
<img width="1072" height="149" alt="image" src="https://github.com/user-attachments/assets/998de3c5-7fc1-4cf4-a7ed-956349338e4e" />


http://192.168.49.2:30007
<img width="1095" height="264" alt="image" src="https://github.com/user-attachments/assets/4d0db288-0343-4d5e-afa0-41624cfccbb9" />

 




























