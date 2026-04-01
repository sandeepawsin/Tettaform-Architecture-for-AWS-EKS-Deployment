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

