# 🚀 Enterprise DevSecOps Assignment

<div align="center">

# 🔐 Production-Grade DevSecOps Implementation

### Kubernetes • Secure CI/CD • GitOps • Istio Service Mesh • Zero Trust • Offensive Security

![GitHub](https://img.shields.io/github/license/mohit-72/devsecops-dodo?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/mohit-72/devsecops-dodo?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/mohit-72/devsecops-dodo?style=for-the-badge)
![GitHub stars](https://img.shields.io/github/stars/mohit-72/devsecops-dodo?style=for-the-badge)

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=githubactions&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge)
![Istio](https://img.shields.io/badge/Istio-466BB0?style=for-the-badge)
![DevSecOps](https://img.shields.io/badge/DevSecOps-Secure-success?style=for-the-badge)

</div>

---

# 📌 About This Repository

This repository contains my complete solution for an **Enterprise DevSecOps Assignment**, demonstrating how modern cloud-native applications can be built, secured, delivered, and validated using production-inspired DevSecOps practices.

The project goes beyond simply deploying an application. It implements secure software delivery, GitOps, Zero Trust networking, service-to-service authentication, infrastructure hardening, and security testing.

The repository is organized into multiple tasks, with each task focusing on a different stage of the secure software delivery lifecycle.

---

# 🎯 Objectives

This project demonstrates practical implementation of:

- Secure Kubernetes Deployments
- Infrastructure Hardening
- Docker Best Practices
- Secure CI/CD Pipelines
- GitHub Actions Automation
- GitOps using ArgoCD
- Container Image Security
- Secret Detection
- Static Code Analysis
- Vulnerability Scanning
- Image Signing
- Istio Service Mesh
- Zero Trust Security
- Mutual TLS (mTLS)
- Identity-Based Authorization
- Kubernetes Network Policies
- Attack Surface Reconnaissance
- Web Application Penetration Testing

---

# 🏆 Key Highlights

| Area | Implementation |
|------|----------------|
| 🐳 Containers | Dockerized Flask Application |
| ☸ Kubernetes | Production-inspired Deployment |
| 🔒 Security | RBAC, Secrets, ConfigMaps, Service Accounts |
| ⚡ CI/CD | GitHub Actions |
| 🛡 Security Scanning | Gitleaks, Semgrep, Trivy |
| ✍ Image Signing | Cosign |
| 🚀 GitOps | ArgoCD |
| 🌐 Service Mesh | Istio |
| 🔐 Zero Trust | STRICT mTLS + AuthorizationPolicy |
| 🌍 Networking | Kubernetes Network Policies |
| 🎯 Offensive Security | Recon + Penetration Testing |

---

# 🏗 High-Level Architecture

```text
                               Developer
                                   │
                                   │ Git Push
                                   ▼
                         GitHub Repository
                                   │
                                   ▼
                        GitHub Actions Pipeline
                                   │
        ┌──────────────────────────┼──────────────────────────┐
        │                          │                          │
        │                          │                          │
   Gitleaks                   Semgrep                     Trivy
 Secret Scan               Static Analysis        Vulnerability Scan
        │                          │                          │
        └──────────────────────────┼──────────────────────────┘
                                   │
                          Docker Image Build
                                   │
                                   ▼
                           Cosign Image Signing
                                   │
                                   ▼
                      GitHub Container Registry
                                   │
                                   ▼
                              ArgoCD GitOps
                                   │
                                   ▼
                         Kubernetes Cluster (Kind)
                                   │
                  ┌────────────────┴────────────────┐
                  │                                 │
                  ▼                                 ▼
          Istio Service Mesh              Kubernetes Security
                  │                                 │
          STRICT Mutual TLS                RBAC / Secrets
                  │                         ConfigMaps
                  │                         NetworkPolicy
                  ▼
             Flask Ledger API
```

---

# 📂 Repository Structure

```text
DevSecOps-Dodo
│
├── task-1-deploy-harden
│   ├── app/
│   ├── deploy/
│   ├── screenshots/
│   └── README.md
│
├── task-2-secure-cicd
│   ├── .github/
│   ├── manifests/
│   ├── screenshots/
│   └── README.md
│
├── task-3-service-mesh-zero-trust
│   ├── manifests/
│   ├── screenshots/
│   └── README.md
│
├── task-4-recon-pentest
│   ├── reports/
│   ├── screenshots/
│   └── README.md
│
└── README.md
```

---

# 📋 Assignment Overview

This repository is divided into four major tasks representing different stages of a modern DevSecOps workflow.

| Task | Focus |
|------|-------|
| Task 1 | Production-Ready Kubernetes Deployment |
| Task 2 | Secure CI/CD Pipeline & GitOps |
| Task 3 | Istio Service Mesh & Zero Trust |
| Task 4 | Reconnaissance & Penetration Testing |

---

> 📖 Continue with **Part 2**, where we'll document **Task 1 (Deploy & Harden)** and **Task 2 (Secure CI/CD)** in detail.

# 🔐 Task 1 — Production-Ready Kubernetes Deployment

## 📖 Overview

The objective of Task 1 was to deploy a production-inspired Flask-based Ledger API on Kubernetes while following modern DevSecOps security best practices.

Instead of simply deploying containers, the application was hardened using Kubernetes-native security controls including RBAC, Secrets, ConfigMaps, Service Accounts, Security Contexts, and Health Probes.

This deployment demonstrates how cloud-native applications should be deployed securely in production environments.

---

## 🎯 Objectives

- Deploy the application on Kubernetes
- Implement least-privilege access
- Secure sensitive data
- Improve application availability
- Follow Kubernetes security best practices
- Prepare workloads for production

---

## ✅ Implemented Features

| Feature | Status |
|----------|--------|
| Dockerized Application | ✅ |
| Kubernetes Deployment | ✅ |
| Namespace Isolation | ✅ |
| ConfigMaps | ✅ |
| Kubernetes Secrets | ✅ |
| RBAC | ✅ |
| Dedicated Service Account | ✅ |
| Security Context | ✅ |
| Readiness Probe | ✅ |
| Liveness Probe | ✅ |
| Resource Requests & Limits | ✅ |
| ClusterIP Service | ✅ |
| Kubernetes Ingress | ✅ |

---

## 🔒 Security Hardening

The deployment follows multiple Kubernetes security best practices.

### Identity & Access Management

- Dedicated Service Account
- Role-Based Access Control (RBAC)
- Least Privilege Principle

### Secret Management

Sensitive application values are stored using Kubernetes Secrets instead of hardcoded credentials.

Examples include:

- Database Passwords
- API Tokens
- Application Secrets

### Configuration Management

Application configuration is separated using ConfigMaps.

Benefits:

- Easy configuration changes
- Better maintainability
- Environment separation

### Container Security

Implemented security best practices:

- Non-root container execution
- Read-only root filesystem
- Privilege escalation disabled
- Dropped unnecessary Linux capabilities

### High Availability

- Replica-based deployment
- Readiness Probe
- Liveness Probe
- Automatic restart on failure

---

## 📊 Task 1 Architecture

```text
                    Internet
                        │
                        ▼
                Kubernetes Ingress
                        │
                        ▼
                ClusterIP Service
                        │
          ┌─────────────┼─────────────┐
          │             │             │
          ▼             ▼             ▼
     Ledger Pod     Ledger Pod     Ledger Pod
          │             │             │
          └─────────────┼─────────────┘
                        │
          ┌─────────────┴──────────────┐
          │                            │
     ConfigMap                  Kubernetes Secret
          │                            │
          └─────────────┬──────────────┘
                        │
                 Service Account
                        │
                      RBAC
```

---

# 🚀 Task 2 — Secure CI/CD Pipeline & GitOps

## 📖 Overview

Task 2 focuses on building a secure software delivery pipeline using GitHub Actions and GitOps principles.

Every code change is automatically validated through multiple security gates before deployment.

This ensures that only trusted and secure artifacts reach the Kubernetes cluster.

---

## 🎯 Objectives

- Automate CI/CD
- Detect secrets before deployment
- Perform Static Code Analysis
- Scan Docker images
- Sign container images
- Deploy using GitOps

---

## 🔄 CI/CD Pipeline

```text
Developer
     │
 Git Push
     │
     ▼
GitHub Repository
     │
     ▼
GitHub Actions
     │
 ┌───┴─────────────────────────────┐
 │                                 │
 │  Gitleaks                       │
 │  Semgrep                        │
 │  Docker Build                   │
 │  Trivy Scan                     │
 │  Cosign Sign                    │
 └───────────────┬─────────────────┘
                 │
                 ▼
       GitHub Container Registry
                 │
                 ▼
              ArgoCD
                 │
                 ▼
         Kubernetes Cluster
```

---

## 🔒 Security Controls

### 🛡 Gitleaks

Automatically scans the repository for accidentally committed secrets.

Examples:

- API Keys
- Passwords
- AWS Keys
- Tokens
- Private Credentials

---

### 🛡 Semgrep

Performs Static Application Security Testing (SAST).

Detects:

- Insecure coding practices
- Dangerous functions
- Security misconfigurations
- Known vulnerability patterns

---

### 🛡 Trivy

Scans Docker images for vulnerabilities.

Checks include:

- Critical vulnerabilities
- High vulnerabilities
- OS packages
- Application dependencies

---

### 🛡 Cosign

Container image signing ensures:

- Image authenticity
- Image integrity
- Trusted software supply chain

---

### 🚀 ArgoCD

GitOps deployment ensures:

- Desired state reconciliation
- Automatic synchronization
- Version-controlled infrastructure
- Reliable Kubernetes deployments

---

## 📊 Task 2 Pipeline Summary

| Stage | Tool |
|--------|------|
| Source Control | GitHub |
| CI/CD | GitHub Actions |
| Secret Detection | Gitleaks |
| Static Analysis | Semgrep |
| Image Scan | Trivy |
| Image Signing | Cosign |
| Registry | GitHub Container Registry |
| GitOps | ArgoCD |
| Deployment | Kubernetes |

---

## 🎯 Task 2 Outcome

Successfully implemented a secure CI/CD pipeline that:

- Detects leaked secrets before deployment
- Performs static application security testing
- Scans container images for vulnerabilities
- Signs container images for integrity
- Automatically deploys through GitOps
- Keeps Kubernetes synchronized with Git

# 🛡 Task 3 — Service Mesh & Zero Trust (Istio)

## 📖 Overview

Task 3 extends the Kubernetes deployment by introducing a production-grade **Service Mesh** using **Istio**.

Rather than relying solely on Kubernetes networking, Istio provides secure service-to-service communication, workload identity, traffic encryption, and policy-based authorization.

The objective was to implement a **Zero Trust Architecture**, where no workload is trusted by default and every request must be authenticated and authorized.

---

# 🎯 Objectives

- Install Istio Service Mesh
- Enable automatic sidecar injection
- Enforce STRICT Mutual TLS
- Implement identity-based Authorization Policies
- Apply Kubernetes Network Policies
- Demonstrate Zero Trust networking

---

# ✅ Implemented Features

| Feature | Status |
|----------|--------|
| Istio Installation | ✅ |
| Sidecar Injection | ✅ |
| STRICT mTLS | ✅ |
| PeerAuthentication | ✅ |
| AuthorizationPolicy | ✅ |
| NetworkPolicy | ✅ |
| SPIFFE Workload Identity | ✅ |
| Zero Trust Communication | ✅ |

---

# 🏗 Zero Trust Architecture

```text
                  Client
                     │
                     ▼
             Istio Ingress Gateway
                     │
                     ▼
          +-----------------------+
          |     Envoy Proxy       |
          +-----------------------+
                     │
              Mutual TLS (mTLS)
                     │
          +-----------------------+
          |     Envoy Proxy       |
          +-----------------------+
                     │
                Ledger API
                     │
                     ▼
        Authorization Policy Check
                     │
          SPIFFE Workload Identity
                     │
                     ▼
         Kubernetes Network Policy
```

---

# 🔐 Mutual TLS (mTLS)

Mutual TLS ensures that:

- Every service has its own certificate
- Services authenticate each other
- Communication is encrypted
- Plaintext traffic is rejected

Implemented using:

- PeerAuthentication
- Istio CA
- Envoy Sidecars

Configuration:

```yaml
apiVersion: security.istio.io/v1

kind: PeerAuthentication

spec:
  mtls:
    mode: STRICT
```

---

# 🛡 AuthorizationPolicy

Authorization is enforced using **workload identity** instead of IP addresses.

Benefits:

- Identity-based security
- Zero Trust enforcement
- Fine-grained access control
- Better auditability

Implemented:

- Default deny
- Explicit allow
- Namespace-based authorization
- Service Account validation

---

# 🔑 SPIFFE Workload Identity

Each workload inside the mesh receives a unique SPIFFE identity.

Example:

```
spiffe://cluster.local/ns/payments/sa/ledger-api
```

Advantages:

- Unique workload identity
- Certificate-based authentication
- Strong identity verification
- No dependency on IP addresses

---

# 🌐 Kubernetes Network Policy

Network Policies provide another layer of security by restricting pod-to-pod communication.

Implemented:

- Default deny
- Explicit allow rules
- Namespace isolation
- Pod selector restrictions

---

# 🏛 Defense in Depth

| Layer | Responsibility |
|--------|----------------|
| Kubernetes RBAC | API Authorization |
| NetworkPolicy | Network Segmentation |
| Istio mTLS | Encryption |
| AuthorizationPolicy | Identity-Based Authorization |
| Service Accounts | Workload Identity |
| SPIFFE | Secure Identity |

---

# 🎯 Task 3 Outcome

Successfully implemented a Zero Trust architecture using Istio.

Security capabilities achieved:

- Encrypted service-to-service communication
- Automatic workload certificates
- Mutual authentication
- Identity-based authorization
- Defense-in-depth networking
- Kubernetes + Istio layered security

---

# 🎯 Task 4 — Reconnaissance & Penetration Testing

## 📖 Overview

Task 4 focuses on understanding the application's external attack surface from an attacker's perspective while following strict Rules of Engagement.

The task is divided into:

- Passive Reconnaissance
- Authorized Web Application Penetration Testing

---

# 🔍 Part A — Passive Reconnaissance

Public information was collected using OSINT techniques without interacting aggressively with production systems.

Tools used:

- crt.sh
- subfinder
- amass
- assetfinder
- httpx
- whatweb
- testssl.sh

Information gathered:

- Public subdomains
- DNS records
- TLS configuration
- HTTP response headers
- Web technologies
- Attack surface inventory

Deliverables:

- External Asset Inventory
- Technology Fingerprinting
- Risk Observations
- Attack Surface Report

---

# ⚔ Part B — Authorized Penetration Testing

The designated vulnerable target was assessed using industry-standard security testing techniques.

Testing Areas:

- Broken Access Control
- SQL Injection
- Cross-Site Scripting (XSS)
- Server Side Request Forgery (SSRF)
- Security Misconfiguration
- Authentication Weaknesses
- Secrets Exposure

---

# 🧰 Security Testing Tools

| Tool | Purpose |
|------|---------|
| Burp Suite Community | Manual Testing |
| OWASP ZAP | DAST |
| Nuclei | Template-Based Scanning |
| ffuf | Content Discovery |
| SQLMap | SQL Injection Testing |

---

# 📑 Reporting Methodology

Each finding includes:

- Executive Summary
- CVSS v3.1 Score
- Severity
- Affected Endpoint
- Proof of Concept
- Impact
- Remediation
- References

---

# 🎯 Offensive Security Outcome

The assessment demonstrates an understanding of:

- Passive Reconnaissance
- Web Application Security
- Vulnerability Assessment
- OWASP Top 10
- Risk Prioritization
- Responsible Disclosure
- Security Reporting

---

# 🛠 Technology Stack

## Cloud Native

- Kubernetes
- Kind
- Docker
- Istio
- ArgoCD

---

## DevSecOps

- GitHub Actions
- Git
- GitHub
- Gitleaks
- Semgrep
- Trivy
- Cosign

---

## Programming

- Python
- Flask
- YAML
- Bash
- PowerShell

---

## Security

- RBAC
- Service Accounts
- Kubernetes Secrets
- ConfigMaps
- Network Policies
- Istio Authorization Policies
- Mutual TLS
- SPIFFE Identity
- Zero Trust Architecture

---

## Offensive Security

- Burp Suite Community
- OWASP ZAP
- Nuclei
- SQLMap
- ffuf
- httpx
- WhatWeb
- crt.sh
- subfinder
- amass
- assetfinder
- testssl.sh

---

# 📊 Skills Demonstrated

This project demonstrates hands-on experience with:

### ☸ Kubernetes

- Deployments
- Services
- Ingress
- Namespaces
- ConfigMaps
- Secrets
- RBAC
- Service Accounts
- Security Context
- Resource Management

---

### 🚀 DevSecOps

- Secure CI/CD
- GitHub Actions
- GitOps
- Container Security
- Infrastructure Hardening
- Secret Management

---

### 🔐 Cloud Security

- Zero Trust
- Service Mesh
- mTLS
- AuthorizationPolicy
- NetworkPolicy
- Identity-Based Security
- Defense in Depth

---

### ⚔ Offensive Security

- Attack Surface Mapping
- Passive Reconnaissance
- Web Application Testing
- OWASP Top 10
- Vulnerability Assessment
- Professional Security Reporting

---

# 📸 Screenshots

> Replace the image paths with your own screenshots.

## Task 1

- Kubernetes Pods
- Deployments
- Services
- Secrets
- ConfigMaps
- RBAC
- Ingress
- Health Endpoint

---

## Task 2

- GitHub Actions Pipeline
- Gitleaks Scan
- Semgrep Scan
- Trivy Scan
- Cosign Signing
- ArgoCD Dashboard
- Successful Deployment

---

## Task 3

- Istio Installation
- Sidecar Injection
- PeerAuthentication
- AuthorizationPolicy
- NetworkPolicy
- mTLS Verification
- Running Pods (2/2 Containers)

---

## Task 4

- Attack Surface Report
- Technology Fingerprinting
- Burp Suite
- ZAP Report
- CVSS Findings
- Final Report

---

# 🚀 Quick Start

Clone the repository

```bash
git clone https://github.com/mohit-72/devsecops-dodo.git

cd devsecops-dodo
```

---

Read task documentation

```text
task-1-deploy-harden/

task-2-secure-cicd/

task-3-service-mesh-zero-trust/

task-4-recon-pentest/
```

Each task contains its own documentation, manifests, configuration files, screenshots, and implementation details.

---

# 🎯 Project Outcomes

By completing this project, the following production-inspired capabilities were successfully implemented:

- ✔ Secure Kubernetes Deployment
- ✔ Infrastructure Hardening
- ✔ Docker Best Practices
- ✔ Least Privilege RBAC
- ✔ Secure Secret Management
- ✔ Production Health Checks
- ✔ GitHub Actions CI/CD
- ✔ Secret Detection
- ✔ Static Code Analysis
- ✔ Vulnerability Scanning
- ✔ Container Image Signing
- ✔ GitOps Continuous Delivery
- ✔ Istio Service Mesh
- ✔ Mutual TLS
- ✔ Zero Trust Networking
- ✔ Identity-Based Authorization
- ✔ Kubernetes Network Policies
- ✔ Reconnaissance
- ✔ Penetration Testing
- ✔ Professional Security Reporting

---

# 📚 Key Learnings

Throughout this assignment I gained practical experience in:

- Cloud Native Security
- Kubernetes Administration
- DevSecOps Automation
- GitOps Workflows
- Software Supply Chain Security
- Secure CI/CD Pipelines
- Service Mesh Architecture
- Zero Trust Networking
- Security Testing
- Threat-Driven Thinking

---

# 🚀 Future Improvements

The project can be extended with:

- Helm Charts
- Kustomize
- Prometheus
- Grafana
- Loki
- Tempo
- Falco Runtime Security
- Kyverno Policies
- OPA Gatekeeper
- External Secrets Operator
- HashiCorp Vault
- SLSA Provenance
- SBOM Generation
- Canary Deployments
- Blue-Green Deployments
- Horizontal Pod Autoscaler

---

# 👨‍💻 About the Author

## Mohit Yadav

Cloud & DevSecOps Engineer

Passionate about building secure, automated, and cloud-native infrastructure using modern DevSecOps practices.

### Technical Skills

- Kubernetes
- Docker
- Terraform
- Microsoft Azure
- GitHub Actions
- ArgoCD
- Istio
- DevSecOps
- GitOps
- Linux
- Python
- Bash
- PowerShell

---

# 🤝 Connect

If you have feedback, suggestions, or would like to discuss DevOps, Cloud, Kubernetes, or DevSecOps, feel free to connect through GitHub.

---

# ⭐ Support

If you found this repository useful, consider giving it a ⭐ on GitHub.

It motivates me to continue building production-grade cloud and DevSecOps projects.

---

<div align="center">

## 🚀 Build Secure. Automate Everything. Trust Nothing.

**Cloud • Kubernetes • DevSecOps • GitOps • Security**

Made with ❤️ by **Mohit Yadav**

</div>