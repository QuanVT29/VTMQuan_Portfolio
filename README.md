<div align="center">

# Multi-Cloud Engineering & Operations Portfolio


[![AWS SAA-C03](https://img.shields.io/badge/AWS-Certified_Solutions_Architect_Associate-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://www.credly.com/)
[![Azure Operations](https://img.shields.io/badge/Azure-Cloud_Operations_Engineer-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-AKS_%26_EKS-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![ITSM Integration](https://img.shields.io/badge/ITSM-ServiceNow_Automation-81B5A1?style=for-the-badge&logo=servicenow&logoColor=white)](https://www.servicenow.com/)

[Curriculum Vitae (PDF)](./docs/CV_VoTaMinhQuan_CloudOps_DevOps.pdf) • [Credly Certification Badge](https://www.credly.com/badges/1db6d09f-23c5-4364-99d0-10f5469515f9/public_url) • [GitHub Repositories](https://github.com/QuanVT29)

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

---

## 1. Introduction & Verified Credentials


I am an **Information Assurance undergraduate at FPT University** and a certified AWS Solutions Architect (SAA-C03) specializing in **Cloud Infrastructure, DevSecOps, and Cloud Operations**.

Bridging a strong foundation in network security, Linux systems hardening, and cloud engineering, my hands-on experience focuses on architecting multi-cloud environments (AWS & Azure) via **Terraform**, orchestrating microservices on **Kubernetes (EKS & AKS)**, and building closed-loop observability and automated incident remediation workflows.

- **Education:** Bachelor of Information Assurance, FPT University (Da Nang) | (Expected: Jan 2028)
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
* **Compute & Container Platforms**: Amazon EKS, EC2 (ARM64 Graviton), Auto Scaling Groups (ASG), AWS Lambda.
  
* **Enterprise Networking & Edge Security**: Multi-AZ VPC design, Public/Private subnets, Route 53 (DNS Failover / Latency Routing), Application Load Balancers (ALB), AWS WAF v2.
  
* **Identity, Secrets & Encryption**: IAM Roles for Service Accounts (IRSA), GitHub Actions OIDC federation, AWS Secrets Manager (auto-rotation), AWS KMS (CMK envelope encryption).
  
* **Data Persistence & Storage**: Amazon RDS (Multi-AZ PostgreSQL/MySQL), Amazon S3, Elastic Block Store (EBS), Elastic File System (EFS).
  
* **Infrastructure as Code (IaC) & Automation**: Modular Terraform architecture, remote state management with S3 backend and DynamoDB state locking.
  
* **Shift-Left DevSecOps & CI/CD**: Automated CI/CD pipelines via GitHub Actions and Tekton, SAST scanning (SonarQube), container image vulnerability auditing (Trivy), and IaC policy-as-code enforcement (Checkov).
  
* **Cloud Migration & Disaster Recovery**: Multi-Region Active-Passive DR strategies (RTO/RPO validation); server rehosting via AWS Application Migration Service (MGN); homogeneous and heterogeneous database migration using AWS Database Migration Service (DMS) and AWS Schema Conversion Tool (SCT).

---

<br>


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

| Module | Focus Area | Implemented Capabilities & Tech Stack |
| :--- | :--- | :--- |
| **01. Identity & Governance** | Zero-Trust & Cost Control | Management Groups, Granular RBAC, AKS Workload Identity, Azure Policy & Budget Alerts. |
| **02. Core Networking** | Micro-segmentation & PaaS | 3-Tier VNet (`10.0.0.0/16`), NSG/ASG Whitelisting, Azure Private Endpoints, Private DNS Zones. |
| **03. Storage & Secrets** | Data Security & Secretless Pods | Blob Lifecycle Tiering, SAS tokens, Key Vault RBAC, Secrets Store CSI Driver (`SecretProviderClass`). |
| **04. Container Platform** | AKS & Stateful Enterprise Tier | System/User Node Pools, Authorized IP Ranges, Azure Cache for Redis (C0), Azure SQL Serverless. |
| **05. Day-2 Cloud-Ops** | Observability, Automation & ITSM | Centralized LAW, KQL Triage, App Insights Tracing, P1–P4 Alerts, PowerShell Runbooks, ServiceNow API. |



---

<br>



### 3.2. Flagship Project: Cloud-Native Observability & Auto-Remediation System

#### [`azure-cloudops-autoremediation`](https://github.com/QuanVT29/azure-cloudops-autoremediation.git)


- **What it does:**

  An enterprise-grade, zero-trust Core Banking platform on Microsoft Azure, codified 100% via modular Terraform across isolated lifecycle layers (`00-bootstrap` remote state, `01-network`, `02-security`, `03-compute-data`, `04-telemetry`, and `05-automation`). Designed around a segmented Virtual Network (`10.0.0.0/16`) with granular Network Security Groups (NSGs), Private DNS Zones, and Private Endpoints, the architecture eliminates public internet exposure for the backend Azure SQL Database while running a multi-replica FastAPI microservice and In-Cluster Redis cache on Azure Kubernetes Service (AKS). Secrets are dynamically mounted and rotated from Azure Key Vault via the Secrets Store CSI Driver under least-privilege RBAC and System-Assigned Managed Identities.

  To guarantee production resilience, the platform implements full-stack observability—combining Log Analytics (`ContainerLogV2`, `KubeEvents`), Container Insights, Application Insights distributed tracing, and FinOps daily ingestion quota governance—paired with an event-driven autonomous incident response pipeline. Validated through a custom live SRE Chaos Engineering Simulator (`HTTP 500` API outages, `OOMKilled` `512Mi` memory limit breaches, and `>3.5s` SQL lock latency SLA violations), custom KQL alert rules perform severity-tiered triage (`P1/Sev1` vs. `P2/Sev2`) to prevent alert fatigue. Critical `P1` outages trigger Azure Logic Apps to automatically log structured incidents via the ServiceNow ITSM Table API while simultaneously invoking Azure Automation PowerShell Runbooks for autonomous pod self-healing.

- **Key Engineering & SRE Outcomes:**
  - **Autonomous Self-Healing (`MTTR < 60s`):** Automated `P1` API outage detection, ServiceNow ticket creation, and zero-downtime `kubectl rollout restart` execution via Managed Identity-authenticated PowerShell Runbooks without human intervention.
  - **Zero-Downtime High Availability:** Verified sub-2-second replica traffic failover and 23-second native Kubernetes pod recovery during Linux `cgroup` `OOMKilling` events.
  - **Intelligent Alert Triage:** Differentiated `P1` hard outages (auto-remediation + Sev1 ticket) from `P2` latency degradation (`3500ms > 2500ms` SLA, routed to Sev2 DBA/App triage without blindly restarting healthy pods).
  - **Shift-Left DevSecOps & NOC Readiness:** Enforced IaC static security scanning (`TFLint`, `Checkov`) and authored production-grade L1/L2 KQL Diagnostic Playbooks, Runbook SOPs, and Root Cause Analysis (RCA) post-mortem documentation.

- **Stack:**

  Azure (AKS, VNet, NSG, Private Endpoints, Private DNS, Azure SQL, Key Vault, Log Analytics, Container Insights, Application Insights, Azure Monitor, Logic Apps, Azure Automation, Managed Identity), Terraform, Kubernetes, PowerShell, KQL, Python (FastAPI), Redis, ServiceNow ITSM, TFLint, Checkov, Bash.








---

<br>


<div align="center">

<br>

**Portfolio Maintained by Võ Tá Minh Quân**  
*Cloud Operations & Devops Engineer • Information Assurance*  
*Da Nang City, Vietnam*

</div>



