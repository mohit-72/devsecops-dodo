# 🔐 Ledger API - Production Ready DevSecOps Deployment

![Python](https://img.shields.io/badge/Python-3.12-blue?style=for-the-badge&logo=python)
![Flask](https://img.shields.io/badge/Flask-Framework-black?style=for-the-badge&logo=flask)
![Docker](https://img.shields.io/badge/Docker-Containerized-2496ED?style=for-the-badge&logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-Kind-326CE5?style=for-the-badge&logo=kubernetes)
![DevSecOps](https://img.shields.io/badge/DevSecOps-Secure-success?style=for-the-badge)
![RBAC](https://img.shields.io/badge/RBAC-Enabled-orange?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)

---

# 📌 Overview

This project demonstrates a **production-style DevSecOps deployment** of a Flask-based Ledger API on Kubernetes.

The application has been containerized using Docker and deployed on a Kubernetes (Kind) cluster while implementing multiple Kubernetes security best practices including:

- Kubernetes Secrets
- ConfigMaps
- RBAC
- Service Accounts
- Security Context
- Resource Requests & Limits
- Readiness & Liveness Probes
- Kubernetes Service
- Ingress

The goal was not only to deploy the application but to make it production-ready following DevSecOps principles.

---

# ✨ Features

- Dockerized Flask Application
- Kubernetes Deployment
- Replica-based High Availability
- Kubernetes Service
- Kubernetes Ingress
- ConfigMap Integration
- Secret Management
- RBAC Authorization
- Dedicated Service Account
- Non-root Container Execution
- Read-only Root Filesystem
- Disabled Privilege Escalation
- Readiness Probe
- Liveness Probe
- Resource Requests & Limits
- REST API Validation

---

# 🏗 Architecture

```text
                        +----------------------+
                        |       Client         |
                        +----------+-----------+
                                   |
                                   |
                           Kubernetes Ingress
                                   |
                            ClusterIP Service
                                   |
          +------------------------+------------------------+
          |                        |                        |
    Ledger Pod 1             Ledger Pod 2             Ledger Pod 3
          |                        |                        |
          +------------------------+------------------------+
                                   |
                 +-----------------+------------------+
                 |                                    |
         Kubernetes Secret                    ConfigMap
                 |                                    |
                 +---------- Service Account ----------+
                                |
                               RBAC
```

---

# 🛠 Technology Stack

| Category | Technology |
|----------|------------|
| Language | Python 3.12 |
| Framework | Flask |
| Containerization | Docker |
| Orchestration | Kubernetes (Kind) |
| Networking | Service, Ingress |
| Security | Secret, RBAC, Service Account |
| Configuration | ConfigMap |
| Version Control | Git |
| CI/CD | GitHub Actions |

---

# 📂 Project Structure

```text
ledger-api-assignment
│
├── app
│   ├── app.py
│   ├── Dockerfile
│   └── requirements.txt
│
├── deploy
│   ├── namespace.yaml
│   ├── deployment.yaml
│   ├── service.yaml
│   ├── ingress.yaml
│   ├── configmap.yaml
│   ├── secret.yaml
│   ├── serviceaccount.yaml
│   └── rbac.yaml
│
├── screenshots
│   ├── 01-pods.png
│   ├── 02-deployment.png
│   ├── 03-service.png
│   ├── 04-secret.png
│   ├── 05-serviceaccount.png
│   ├── 06-rbac.png
│   ├── 07-configmap.png
│   ├── 08-ingress.png
│   ├── 09-health-api.png
│   ├── 10-transactions-api.png
│   └── 11-tokenize-api.png
│
├── .github
│   └── workflows
│       └── build.yml
│
├── .gitignore
└── README.md
```

---

# 🚀 Docker Build

```bash
cd app

docker build -t ledger-api:secure-v2 .
```

---

# ☸️ Load Image into Kind

```bash
kind load docker-image ledger-api:secure-v2 --name dodo-devsecops
```

---

# 🚀 Deploy to Kubernetes

```bash
kubectl apply -f deploy/namespace.yaml
kubectl apply -f deploy/secret.yaml
kubectl apply -f deploy/configmap.yaml
kubectl apply -f deploy/serviceaccount.yaml
kubectl apply -f deploy/rbac.yaml
kubectl apply -f deploy/service.yaml
kubectl apply -f deploy/ingress.yaml
kubectl apply -f deploy/deployment.yaml
```

---

# ✅ Kubernetes Verification

### Pods

```bash
kubectl get pods -n payments
```

### Deployment

```bash
kubectl get deployment -n payments
```

### Service

```bash
kubectl get svc -n payments
```

### Secret

```bash
kubectl get secret -n payments
```

### Service Account

```bash
kubectl get serviceaccount -n payments
```

### RBAC

```bash
kubectl get role,rolebinding -n payments
```

### ConfigMap

```bash
kubectl get configmap -n payments
```

### Ingress

```bash
kubectl get ingress -n payments
```

---

# 🌐 API Validation

### Health Endpoint

```bash
curl http://localhost:8081/health
```

Response

```json
{
  "status":"ok"
}
```

---

### Transactions Endpoint

```bash
curl http://localhost:8081/transactions
```

---

### Tokenization Endpoint

```powershell
Invoke-RestMethod -Uri "http://localhost:8081/tokenize" -Method POST -ContentType "application/json" -Body '{"pan":"4242424242424242"}'
```

Example Response

```json
{
    "last4":"4242",
    "token":"tok_477bba133c182267fe5f0869"
}
```

---

# 🛡 Security Hardening

The deployment follows Kubernetes security best practices.

- Kubernetes Secret for sensitive credentials
- ConfigMap for application configuration
- Dedicated Service Account
- RBAC (Least Privilege Access)
- Namespace Isolation
- Non-root Container Execution
- Read-only Root Filesystem
- Disabled Privilege Escalation
- Resource Requests & Limits
- Readiness Probe
- Liveness Probe
- Kubernetes Ingress

---

# 📸 Project Screenshots

## Kubernetes Resources

### Pods

![](screenshots/01-pods.png)

---

### Deployment

![](screenshots/02-deployment.png)

---

### Service

![](screenshots/03-service.png)

---

### Secret

![](screenshots/04-secret.png)

---

### Service Account

![](screenshots/05-serviceaccount.png)

---

### RBAC

![](screenshots/06-rbac.png)

---

### ConfigMap

![](screenshots/07-configmap.png)

---

### Ingress

![](screenshots/08-ingress.png)

---

## API Validation

### Health API

![](screenshots/09-health-api.png)

---

### Transactions API

![](screenshots/10-transactions-api.png)

---

### Tokenization API

![](screenshots/11-tokenize-api.png)

---

# 🎯 Project Outcome

Successfully deployed and secured the Ledger API on Kubernetes using production-inspired DevSecOps practices.

Implemented:

- Docker
- Kubernetes
- RBAC
- Secrets
- ConfigMaps
- Service Accounts
- Ingress
- Health Checks
- Resource Limits
- Security Context

The application is fully operational and all Kubernetes resources were successfully validated.

---

# 🚀 Future Improvements

- GitHub Actions CI/CD
- Trivy Image Scanning
- Checkov Manifest Scanning
- Prometheus Monitoring
- Grafana Dashboard
- Helm Chart
- Horizontal Pod Autoscaler
- Network Policies

---

# 👨‍💻 Author

## Mohit Yadav

**Cloud & DevOps Engineer**

### Skills

- Microsoft Azure
- Kubernetes
- Docker
- Terraform
- Linux
- GitHub Actions
- Python
- Flask
- DevSecOps
- RBAC
- Ingress
- Secrets
- CI/CD

---

# ⭐ If you found this project useful, don't forget to star the repository.