<div align="center">

# Multi-Cloud Engineering & Operations Portfolio

**Production Architectures, DevSecOps Automation, and Azure Cloud Operations**

[![AWS SAA-C03](https://img.shields.io/badge/AWS-Certified_Solutions_Architect_Associate-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://www.credly.com/)
[![Azure Operations](https://img.shields.io/badge/Azure-Cloud_Operations_Engineer-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-AKS_%26_EKS-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![ITSM Integration](https://img.shields.io/badge/ITSM-ServiceNow_Automation-81B5A1?style=for-the-badge&logo=servicenow&logoColor=white)](https://www.servicenow.com/)

[Curriculum Vitae (PDF)](./01-credentials/docs/CV_VoTaMinhQuan_CloudOps.pdf) • [Credly Certification Badge](https://www.credly.com/) • [GitHub Repositories](https://github.com/QuanVT29)

</div>

---

## Table of Contents
1. [Introduction & Verified Credentials](#1-introduction--verified-credentials)
2. [Amazon Web Services (AWS) & DevSecOps Platform](#2-amazon-web-services-aws--devsecops-platform)
   - [Core Technical Knowledge](#21-core-aws--devsecops-competencies)
   - [Production Projects & Workload Migration Labs](#22-production-projects--migration-labs)
3. [Microsoft Azure & Cloud Operations ](#3-microsoft-azure--cloud-operations-day-2-ops)
   - [Core Architectural & Operational Knowledge](#31-azure-core-pillars--cloud-ops-competencies)
   - [Flagship Project: Cloud-Native Observability & Auto-Remediation System](#32-flagship-project-cloud-native-observability--auto-remediation-system)
   - [Technical Runbooks & Lab Reports](#33-technical-runbooks--lab-reports)

---

## 1. Introduction & Verified Credentials


I am an **Information Assurance undergraduate at FPT University** and a certified AWS Solutions Architect (SAA-C03) specializing in **Cloud Infrastructure, DevSecOps, and Cloud Operations**.

Bridging a strong foundation in network security, Linux systems hardening, and cloud engineering, my hands-on experience focuses on architecting multi-cloud environments (AWS & Azure) via **Terraform**, orchestrating microservices on **Kubernetes (EKS & AKS)**, and building closed-loop observability and automated incident remediation workflows.

* **Education:** Bachelor of Information Assurance, FPT University (Da Nang) | **GPA: 3.5 / 4.0** (Expected: Jan 2028)
* **Language Proficiency:** English — Full Professional Proficiency (**IELTS 7.0 level**)
* **Core Competencies:** Multi-Cloud Infrastructure (AWS & Azure), Infrastructure as Code (Terraform), DevSecOps CI/CD Pipelines, Container Security, Linux Administration, and ITSM Runbook Automation.

### Verified Credentials & Certifications

| Credential / Certification | Issuing Organization | Scope / Verification |
| :--- | :--- | :--- |
| **AWS Certified Solutions Architect – Associate (SAA-C03)** | Amazon Web Services | [Verify via Credly ↗](https://www.credly.com/) |
| **Foundations of Cybersecurity** | Google | Information Security Principles, Threat Assessment |
| **Introduction to Networks** | Cisco Networking Academy | Routing, VLANs, Subnetting, TCP/IP Layer Diagnostics |
| **GenAI in Cloud** | FPT Software | Cloud AI Integration & Productivity Automation |
| **Microsoft Azure (AZ-900 & AZ-104 Focus Track)** | Microsoft Learning | RBAC, VNet/NSG, AKS Operations, Log Analytics & KQL |

---


<br>


## 2. Amazon Web Services (AWS) & DevSecOps Platform

### 2.1. Core AWS & DevSecOps Competencies
* **Compute & Container Platforms**: Amazon EKS, EC2, Auto Scaling Groups (ASG), AWS Lambda.
* **Software-Defined Networking & Security**: Multi-AZ VPC architecture, Public/Private Subnets, Internet/NAT Gateways, Application Load Balancers (ALB), Route 53, IAM Roles for Service Accounts (IRSA), Security Groups, and NACLs.
* **Data Layer & Storage**: Amazon RDS (PostgreSQL/MySQL), Amazon S3, Elastic Block Store (EBS), Elastic File System (EFS).
* **Infrastructure as Code (IaC) & Automation**: Modular Terraform architectures with remote state management and locking.
* **DevSecOps & Shift-Left Security**: Automated CI/CD pipelines via GitHub Actions, container image vulnerability scanning using Trivy, and IaC misconfiguration audits using Checkov.
* **Cloud Migration Disciplines**: Workload assessment, heterogeneous database schema conversion, and minimal-downtime replication via AWS Database Migration Service (DMS) and AWS Schema Conversion Tool (SCT).

---

### 2.2. Production Projects & Migration Labs

#### [`aws-eks-devsecops-todo-app`](https://github.com/votaquann/aws-eks-devsecops-todo-app)
* **What it does**: A production-grade DevSecOps pipeline deploying a containerized microservice onto a managed Amazon EKS cluster. The platform integrates shift-left security directly into GitHub Actions, automatically halting builds upon detecting High/Critical vulnerabilities via Trivy (container scans) or Checkov (Terraform static code analysis). Deployment is managed via custom Helm charts ensuring rolling updates, zero downtime, and zero plain-text secrets in the repository.
* **Stack**: Amazon EKS, Terraform, Helm, Docker, GitHub Actions, Trivy, Checkov.

#### [`aws-enterprise-3tier-platform`](https://github.com/votaquann/aws-enterprise-3tier-platform)
* **What it does**: An enterprise-grade, highly available 3-tier web architecture across multiple Availability Zones on AWS. The design features a public-facing Application Load Balancer, an auto-scaling compute tier hosted in private subnets, and an isolated database tier running Amazon RDS PostgreSQL with automated failover. The entire infrastructure is 100% codified via modular, reusable Terraform scripts following AWS Well-Architected Framework principles.
* **Stack**: AWS VPC, EC2 Auto Scaling, ALB, RDS PostgreSQL, Terraform Modules, CloudWatch.

#### [`Enterprise Database & VM Migration to AWS (Labs Report)`](./02-aws-devsecops/docs/enterprise-migration-labs-report.pdf)
* **What it does**: Technical execution and reporting of two enterprise migration labs performed during internship tenure:
  1. *VMware vSphere VM to AWS EC2*: Virtual disk image preparation, driver injection, volume conversion, and networking realignment.
  2. *Heterogeneous Database Migration*: Full-cycle migration of an on-premises relational database (Dockerized Oracle/MySQL) to Amazon RDS PostgreSQL using AWS SCT for schema translation and AWS DMS for initial data load and continuous replication (CDC) with zero data loss.
* **Deliverable**: Comprehensive migration procedure, schema conversion logs, cutover checklist, and data integrity verification report.

#### [`gitops-k8s-local-observability`](https://github.com/votaquann/gitops-k8s-local-observability)
* **What it does**: A localized Kubernetes platform implementing declarative GitOps synchronization and the Golden Signals observability stack. Workloads are monitored using Prometheus and visualized via custom Grafana dashboards, with Alertmanager routing threshold-based notifications for high CPU/RAM utilization and service degradation.
* **Stack**: Kubernetes, GitOps Engine, Helm, Prometheus, Grafana, Alertmanager.

---

<br>




## 3. Microsoft Azure & Cloud Operations 

### 3.1. Core Architectural & Operational Knowledge

#### Core Cloud-Native Administration (AZ-104 Focus)
* **Identity & Governance**: Azure Active Directory (Microsoft Entra ID), Role-Based Access Control (RBAC) at Management Group, Subscription, and Resource Group scopes; Managed Identities (System-Assigned & User-Assigned) for secretless automation.
* **Virtual Networking & Security**: Azure VNet architecture, Public/Private subnet partitioning, Network Security Groups (NSGs) with stateful rule definitions, Application Security Groups (ASGs).
* **Compute & Storage Operations**: Azure Kubernetes Service (AKS) lifecycle management, private cluster architecture, system/user node pool administration; Azure Blob Storage for cold diagnostic data and Azure File Shares (SMB/NFS) for container persistent volumes.
* **Centralized Telemetry**: Log Analytics Workspace (LAW) provisioning and diagnostic settings collection across VMs, AKS clusters, Azure SQL, and networking components.



---

### 3.2. Flagship Project: Cloud-Native Observability & Auto-Remediation System

#### [`azure-observability-auto-remediation`](https://github.com/votaquann/azure-observability-auto-remediation)











---

### 3.3. Technical Runbooks & Lab Reports

The following technical documents and operational runbooks are maintained within this repository for direct review:

| Document Title | Scope & Purpose | Direct Link |
| :--- | :--- | :--- |
| **Azure Auto-Remediation Architecture Guide** | Detailed architecture specifications, Terraform state mapping, and Logic App webhook JSON payloads. | [`View PDF ↗`](./03-azure-cloudops/docs/azure-observability-remediation-report.pdf) |
| **KQL Production Incident Playbook** | Curated collection of KQL queries for triaging Kubernetes crashes, database slow queries, and HTTP 5xx spikes. | [`View PDF ↗`](./03-azure-cloudops/docs/kql-rca-playbook.pdf) |
| **Enterprise Cloud Migration Report** | Detailed documentation of VM and database migrations from local hypervisors to AWS infrastructure. | [`View PDF ↗`](./02-aws-devsecops/docs/enterprise-migration-labs-report.pdf) |
| **AZ-104 Core Architecture Reference** | Consolidated study and implementation guide for Azure RBAC, VNet/NSG, AKS Storage, and Monitoring. | [`View PDF ↗`](./03-azure-cloudops/docs/az104-core-foundations.pdf) |

---

<div align="center">

<br>

**Portfolio Maintained by Võ Tá Minh Quân**  
*Cloud Operations & Devops Engineer • Information Assurance*  
*Da Nang City, Vietnam*

</div>
