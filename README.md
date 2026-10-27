<div align="center">

# Multi-Cloud Engineering & Operations Portfolio

**Production Architectures, DevSecOps Automation, and Azure Cloud Operations**

[![AWS SAA-C03](https://img.shields.io/badge/AWS-Certified_Solutions_Architect_Associate-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://www.credly.com/)
[![Azure Operations](https://img.shields.io/badge/Azure-Cloud_Operations_Engineer-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-AKS_%26_EKS-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![ITSM Integration](https://img.shields.io/badge/ITSM-ServiceNow_Automation-81B5A1?style=for-the-badge&logo=servicenow&logoColor=white)](https://www.servicenow.com/)

[Curriculum Vitae (PDF)](./01-credentials/docs/CV_VoTaMinhQuan_CloudOps.pdf) • [Credly Certification Badge](https://www.credly.com/badges/1db6d09f-23c5-4364-99d0-10f5469515f9/public_url) • [GitHub Repositories](https://github.com/QuanVT29)

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
   - [Technical Runbooks & Documentation](#33-technical-runbooks-&-documentation)

---

## 1. Introduction & Verified Credentials


I am an **Information Assurance undergraduate at FPT University** and a certified AWS Solutions Architect (SAA-C03) specializing in **Cloud Infrastructure, DevSecOps, and Cloud Operations**.

Bridging a strong foundation in network security, Linux systems hardening, and cloud engineering, my hands-on experience focuses on architecting multi-cloud environments (AWS & Azure) via **Terraform**, orchestrating microservices on **Kubernetes (EKS & AKS)**, and building closed-loop observability and automated incident remediation workflows.

- **Education:** Bachelor of Information Assurance, FPT University (Da Nang) | **GPA: 3.5 / 4.0** (Expected: Jan 2028)
- **Language Proficiency:** English — Full Professional Proficiency (**IELTS 7.0 level**)
- **Core Competencies:** Multi-Cloud Infrastructure (AWS & Azure), Infrastructure as Code (Terraform), Kubernetes & Container Security (AKS/EKS), Observability & KQL Log Analytics, Linux System Hardening, and ITSM Runbook Automation (ServiceNow/Logic Apps).

### Verified Credentials & Certifications

| Credential / Certification | Issuing Organization | Scope / Verification |
| :--- | :--- | :--- |
| **AWS Certified Solutions Architect – Associate (SAA-C03)** | Amazon Web Services | [Verify via Credly ↗](https://www.credly.com/badges/1db6d09f-23c5-4364-99d0-10f5469515f9/public_url) |
| **Foundations of Cybersecurity** | Google | Information Security Principles, Threat Assessment |
| **Introduction to Networks** | Cisco Networking Academy | Routing, VLANs, Subnetting, TCP/IP Layer Diagnostics |
| **GenAI in Cloud** | FPT University | Cloud AI Integration & Productivity Automation |
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

#### [`aws-eks-devsecops-todo-app`](https://github.com/QuanVT29/aws-eks-devsecops-todo-app.git)

• **What it does**:

A production-grade DevSecOps pipeline deploying a full-stack containerized web application onto a multi-AZ AWS EKS cluster. The platform integrates automated shift-left security gates directly into GitHub Actions—halting builds on High/Critical vulnerabilities via Checkov (IaC), SonarQube (SAST), and Trivy (container scans). Features automated L7 traffic routing via AWS ALB, HPA auto-scaling, zero plain-text secrets, and continuous full-stack observability powered by Prometheus & Grafana.

• **Stack**:

AWS (EKS, VPC, ALB, ECR), Terraform, Kubernetes, Docker, GitHub Actions, Checkov, SonarQube, Trivy, Prometheus, Grafana, MongoDB Atlas.


<br>

#### [`aws-enterprise-3tier-platform`](https://github.com/QuanVT29/aws-enterprise-3tier-platform.git)

• **What it does**:

An enterprise-grade, highly resilient 3-tier AWS platform codified 100% via modular Terraform. It features ARM64 Graviton EC2 Auto Scaling, an Amazon RDS Multi-AZ PostgreSQL cluster, and an automated Multi-Region Active-Passive Disaster Recovery setup in Sydney (ap-southeast-2) via Route 53 DNS Failover (Verified RTO: 5m 22s, RPO < 15s). The platform embeds shift-left DevSecOps (GitHub Actions via IAM OIDC, Checkov, Trivy), zero-downtime CodeDeploy rollouts, full-stack CloudWatch/Canary observability, and defense-in-depth security (AWS WAF v2, KMS CMK envelope encryption, Secrets Manager auto-rotation) adhering to CIS AWS Benchmark standards.

• **Stack**:

AWS (VPC, EC2 Graviton, ALB, RDS Multi-AZ, Route 53, WAF v2, KMS, Secrets Manager, CloudWatch, Synthetics, CodeDeploy), Terraform, GitHub Actions (OIDC), Checkov, Trivy, Bash, PostgreSQL.

<br>

#### [`Enterprise Database & VM Migration to AWS (Labs Report)`](./aws_labs/migration/Migration_oracle_aws.pdf)

* **Technical execution and reporting of end-to-end enterprise workload and database migration labs:** 

i. Lift-and-Shift Server Migration (Rehost): Executed block-level, continuous data replication of an on-premises Linux VM (VMware) to AWS EC2 using AWS Application Migration Service (AWS MGN), ensuring near-zero downtime cutover and automated driver/hypervisor conversion.

ii. Homogeneous Replatform & Decoupling: Replatformed local MySQL to Amazon RDS for MySQL using AWS DMS (CDC via binary logs with SSL encryption); successfully decoupled a monolithic LAMP stack into a secured 2-Tier Cloud Architecture post-cutover.

iii. Heterogeneous Database Migration: Migrated an on-premises commercial RDBMS (Dockerized Oracle Database 23ai) to Amazon RDS for PostgreSQL. Leveraged AWS Schema Conversion Tool (SCT) for schema assessment and automated DDL conversion (handling proprietary data types: CLOB to TEXT, NUMBER to NUMERIC, DATE to TIMESTAMP), followed by AWS DMS for full-load data ingestion with zero data loss.

Deliverable: Comprehensive migration runbooks, SCT database assessment reports, cutover checklist, and post-migration data integrity verification reports via CLI/psql.

<br>

#### [`gitops-k8s-local-observability`](./aws_labs/gitops_project/Project_GitOps.pdf)

• **What it does**:

An end-to-end, localized Cloud-Native DevSecOps and GitOps platform running on Kubernetes (k3d/WSL2). It automates the full software delivery lifecycle: self-hosted code management and automated CI builds with rootless containerization, automated vulnerability scanning (Shift-Left security), and dual-repository declarative GitOps deployments across multi-environment namespaces (Staging/Production). The platform integrates a 3-tier Observability stack collecting Prometheus metrics across CI pipelines, GitOps synchronization drift, and application Golden Signals, visualized via custom Grafana dashboards.

• **Stack:**

Kubernetes (k3d/K3s), Gitea, Tekton Pipelines, Tekton Triggers, Kaniko, Trivy, Harbor OCI Registry, Argo CD, Kustomize, Helm, Prometheus, Grafana.


---

<br>




## 3. Microsoft Azure & Cloud Operations 

### 3.1. Core Architectural & Operational Knowledge

#### Module 1: Governance, Zero-Trust Identity & Cost Guardrails
* **Hierarchy & RBAC:** Enforced 4-tier scoping (`Management Group` $\rightarrow$ `Subscription` $\rightarrow$ `Resource Group` $\rightarrow$ `Resource`) with least-privilege roles (`Contributor`, `Reader`, `Monitoring Contributor`).
* **Secretless Identities:** Implemented User-Assigned Managed Identity and **AKS Workload Identity** for direct ARM API interaction without credentials.
* **Governance & Budget:** Applied Azure Policies restricting region deployment (`Southeast Asia`) and compute SKUs; enforced automated $5 email budget alerts.

#### Module 2: Secure Core Networking & Zero-Public PaaS
* **VNet Architecture:** Segmented CIDR `10.0.0.0/16` into `snet-aks` (`10.0.1.0/24`), `snet-data` (`10.0.2.0/24`), and `snet-mgmt` (`10.0.3.0/24`).
* **L4 Micro-segmentation:** Enforced NSG `DenyAllInbound` with strict IP-whitelisted SSH to a Jumpbox hardened via Application Security Groups (`asg-jumpbox`).
* **Private PaaS:** Configured Private Endpoints and Private DNS Zones for Storage and Azure SQL, isolating traffic strictly within private IPs (`10.0.2.x`).

#### Module 3: Storage, Secrets & Secretless Workloads
* **Storage Security:** Disabled public access; enforced lifecycle tiering (Hot $\rightarrow$ Cool after 7d $\rightarrow$ Archive after 30d) and time/IP-restricted SAS tokens.
* **Key Vault Hardening:** Enforced Azure RBAC authorization with `Soft-delete` and `Purge Protection`.
* **Secretless AKS:** Deployed Azure Key Vault Secrets Store CSI Driver (`SecretProviderClass`) to mount DB credentials directly into pods without hardcoded secrets.

#### Module 4: Container Platform & Stateful Workloads (AKS + Cache + DB)
* **AKS Cluster Operations:** Provisioned System (`Standard_B2s`) and User Node Pools; secured API Server via Authorized IP Ranges; integrated ACR via `AcrPull` Managed Identity.
* **Stateful Data Tier:** Provisioned **Azure Cache for Redis** (Basic C0) and **Azure SQL Database** (Serverless, Auto-Pause enabled).
* **3-Tier Deployment:** Packaged and deployed a microservice stack orchestrating full communication: `App` $\leftrightarrow$ `Redis Cache` $\leftrightarrow$ `Azure SQL`.

#### Module 5: Observability, Runbook Automation & ITSM Operations
* **Centralized LAW & KQL:** Streamed `KubeEvents`, `ContainerLogV2`, and `AppRequests` to Log Analytics (30-day retention); executed KQL queries isolating `OOMKilled`, `CrashLoopBackOff`, and HTTP 5xx spikes.
* **Application Insights & Tracing:** Mapped live dependency topology via Application Map to detect SQL/Redis latency bottlenecks and unhandled exceptions.
* **Severity Alerting (P1–P4):** Configured alert rules for HTTP 5xx > 10% (P1), DB latency > 2s (P2), and node resource saturation > 85% (P3).
* **Auto-Remediation (Runbooks):** Authored PowerShell Runbooks authenticated via Managed Identity to auto-restart failing pods upon receiving P1 alerts (MTTR < 60s).
* **ITSM Integration (ServiceNow via Logic Apps):** Built event-driven Logic Apps to parse Azure Monitor webhooks, auto-creating and resolving incident tickets in ServiceNow with KQL RCA data.



---

<br>



### 3.2. Flagship Project: Cloud-Native Observability & Auto-Remediation System

#### [`azure-observability-auto-remediation`](https://github.com/votaquann/azure-observability-auto-remediation)











---

### 3.3. Technical Runbooks & Documentation

The following technical documents and architecture references are maintained within this repository for direct review:

| Document Title | Scope & Purpose | Direct Link |
| :--- | :--- | :--- |
| **Azure Auto-Remediation System Report** | End-to-end architecture design, Terraform manifests, Logic App webhook payloads, and operational KQL incident runbooks. | [`View PDF ↗`](./azure_labs/docs/Azure-Auto-Remediation-Report.pdf) |
| **AZ-104 Core Cloud-Native Reference** | Consolidated technical notes and hands-on guide covering Identity (RBAC/Managed ID), VNet/NSG, AKS Storage, and LAW. | [`View PDF ↗`](./azure_labs/docs/AZ104-Core-Foundations.pdf) |

---

<div align="center">

<br>

**Portfolio Maintained by Võ Tá Minh Quân**  
*Cloud Operations & Devops Engineer • Information Assurance*  
*Da Nang City, Vietnam*

</div>
