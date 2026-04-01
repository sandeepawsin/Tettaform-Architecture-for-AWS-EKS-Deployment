<img width="1440" height="1524" alt="image" src="https://github.com/user-attachments/assets/a84e734b-17df-4f2e-973a-2951a8c9601f" /># Tettaform-Architecture-for-AWS-EKS-Deployment

<img width="705" height="754" alt="Screenshot 2026-03-30 at 8 10 23 PM" src="https://github.com/user-attachments/assets/136292c7-e6a7-4669-9ac6-b0d4a9ce257d" />

Project strecture

# 🚀 EKS Production Platform (AWS + Kubernetes + GitOps)

## 📌 Overview

This project demonstrates a **production-grade Kubernetes platform** built on AWS using:

- **Amazon EKS** for container orchestration
- **Terraform** for Infrastructure as Code
- **GitHub Actions** for CI/CD automation
- **ArgoCD (GitOps)** for continuous delivery
- **Prometheus + Grafana** for observability

The platform simulates real-world production environments with **scalability, reliability, and automation best practices**.

---

## 🏗️ Architecture

The system follows a modern GitOps-based architecture:

1. Developers push code to GitHub
2. CI pipeline builds Docker image and pushes to AWS ECR
3. ArgoCD syncs Kubernetes manifests from GitHub
4. Application is deployed automatically to EKS
5. Monitoring and alerting handled via Prometheus & Grafana

---

## ⚙️ Tech Stack

### ☁️ Cloud
- AWS (EKS, ECR, VPC, IAM)

### 📦 Containerization
- Docker
- Kubernetes (EKS)

### 🔁 CI/CD
- GitHub Actions

### 🔄 GitOps
- ArgoCD

### 📊 Monitoring
- Prometheus
- Grafana
- Alertmanager

### 🏗️ Infrastructure
- Terraform

---

## 📁 Project Structure

eks-production-platform/
│
├── terraform/ # Infrastructure as Code
├── kubernetes/ # Kubernetes manifests
├── helm/ # Helm charts
├── argocd/ # ArgoCD applications
├── .github/workflows/ # CI/CD pipelines
└── README.md


---

## 🚀 Features

- ✅ Infrastructure provisioning using Terraform
- ✅ Kubernetes cluster setup using EKS
- ✅ GitOps-based deployment using ArgoCD
- ✅ Automated CI/CD pipeline
- ✅ Container image management using AWS ECR
- ✅ Observability with Prometheus & Grafana
- ✅ Horizontal Pod Autoscaling (HPA)
- ✅ Production-ready architecture design

---

## 🔄 CI/CD Workflow

1. Code pushed to GitHub
2. GitHub Actions pipeline triggers:
   - Build Docker image
   - Security scan (optional)
   - Push image to AWS ECR
3. ArgoCD detects manifest changes
4. Automatic deployment to Kubernetes

---

## 📊 Observability

- **Prometheus** collects metrics from Kubernetes cluster
- **Grafana** dashboards visualize system performance
- **Alertmanager** triggers alerts for:
  - High CPU usage
  - Pod restarts
  - Node failures

---

## ⚡ Auto Scaling

- **Horizontal Pod Autoscaler (HPA)** scales application pods based on CPU usage
- **Cluster Autoscaler** adjusts node capacity dynamically

---

## 🔐 Security Best Practices

- IAM roles and least privilege access
- Kubernetes RBAC for access control
- Secrets management using Kubernetes/AWS Secrets Manager

---

## 🛠️ Setup Instructions

### 1. Clone Repository
git clone https://github.com/sandeepawsin/terraform-architecture-for-aws-eks.git

cd eks-production-platform


---

### 2. Provision Infrastructure
cd terraform
terraform init
terraform apply

cd terraform
terraform init
terraform apply


---

### 3. Configure kubectl


aws eks update-kubeconfig --region <region> --name <cluster-name>
kubectl get nodes


---

### 4. Install ArgoCD


kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml


---

### 5. Deploy Application via ArgoCD

Apply ArgoCD application manifest:


kubectl apply -f argocd/applications.yaml


---

### 6. Install Monitoring Stack


helm repo add prometheus-community https://prometheus-community.github.io/helm-charts

helm install monitoring prometheus-community/kube-prometheus-stack


---

## 📸 Screenshots (Add these)

- ArgoCD dashboard
- Grafana dashboards
- CI/CD pipeline execution
- Kubernetes pods/services

---

## 🎯 Use Cases

- Production-grade Kubernetes deployment
- DevOps/SRE learning and demonstration
- GitOps workflow implementation
- Cloud-native architecture reference

---

## 🚀 Future Enhancements

- Add Loki for centralized logging
- Integrate Trivy for security scanning
- Implement service mesh (Istio)
- Add multi-environment (dev/stage/prod)
- Implement blue-green/canary deployments

---

## 👨‍💻 Author

Sandeep Kumar Reddy  
Senior DevOps / SRE / Platform Engineer  

---

## ⭐ Key Highlights

- Reduced MTTR using observability stack
- Enabled automated deployments using GitOps
- Designed scalable and highly available architecture
- Implemented production-ready DevOps best practices

