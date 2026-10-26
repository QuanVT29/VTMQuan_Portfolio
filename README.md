<div align="center">

# Multi-Cloud Engineering & Operations Portfolio

**Production Architectures, DevSecOps Automation, and Day-2 Azure Cloud Operations**

[![AWS SAA-C03](https://img.shields.io/badge/AWS-Certified_Solutions_Architect_Associate-FF9900?style=for-the-badge&logo=amazon-aws&logoColor=white)](https://www.credly.com/)
[![Azure Operations](https://img.shields.io/badge/Azure-Cloud_Operations_Engineer-0078D4?style=for-the-badge&logo=microsoft-azure&logoColor=white)](https://azure.microsoft.com/)
[![Kubernetes](https://img.shields.io/badge/Kubernetes-AKS_%26_EKS-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://kubernetes.io/)
[![Terraform](https://img.shields.io/badge/IaC-Terraform-7B42BC?style=for-the-badge&logo=terraform&logoColor=white)](https://www.terraform.io/)
[![ITSM Integration](https://img.shields.io/badge/ITSM-ServiceNow_Automation-81B5A1?style=for-the-badge&logo=servicenow&logoColor=white)](https://www.servicenow.com/)

[Curriculum Vitae (PDF)](./01-credentials/docs/CV_VoTaMinhQuan_CloudOps.pdf) • [Credly Certification Badge](https://www.credly.com/) • [GitHub Repositories](https://github.com/)

</div>

---

## Table of Contents
1. [Introduction & Verified Credentials](#1-introduction--verified-credentials)
2. [Amazon Web Services (AWS) & DevSecOps Platform](#2-amazon-web-services-aws--devsecops-platform)
   - [Core Technical Knowledge](#21-core-aws--devsecops-competencies)
   - [Production Projects & Workload Migration Labs](#22-production-projects--migration-labs)
3. [Microsoft Azure & Cloud Operations (Day-2 Ops)](#3-microsoft-azure--cloud-operations-day-2-ops)
   - [Core Architectural & Operational Knowledge](#31-azure-core-pillars--cloud-ops-competencies)
   - [Flagship Project: Cloud-Native Observability & Auto-Remediation System](#32-flagship-project-cloud-native-observability--auto-remediation-system)
   - [Technical Runbooks & Lab Reports](#33-technical-runbooks--lab-reports)

---

## 1. Introduction & Verified Credentials

I am a Cloud and Infrastructure Operations Engineer with an academic background in Information Assurance. My technical foundation spans multi-cloud architecture (AWS & Azure), container orchestration (Kubernetes), Infrastructure as Code (Terraform), and enterprise Day-2 operations—focusing on closed-loop observability, runbook automation, and root-cause troubleshooting.

### Verified Credentials
* **[AWS Certified Solutions Architect – Associate (SAA-C03)](https://www.credly.com/)**: Certified verification of enterprise cloud architecture design, multi-tier network isolation, high availability, and secure workload operations.
* **Microsoft Certified: Azure Fundamentals (AZ-900) & AZ-104 Focus Track**: In-depth specialization covering Azure identity governance, software-defined networking, AKS orchestration, and Log Analytics.
* **Formal Education**: Undergraduate in Information Assurance, Đại học FPT Đà Nẵng.

---

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

## 3. Microsoft Azure & Cloud Operations (Day-2 Ops)

### 3.1. Azure Core Pillars & Cloud-Ops Competencies

#### A. Core Cloud-Native Administration (AZ-104 Focus)
* **Identity & Governance**: Azure Active Directory (Microsoft Entra ID), Role-Based Access Control (RBAC) at Management Group, Subscription, and Resource Group scopes; Managed Identities (System-Assigned & User-Assigned) for secretless automation.
* **Virtual Networking & Security**: Azure VNet architecture, Public/Private subnet partitioning, Network Security Groups (NSGs) with stateful rule definitions, Application Security Groups (ASGs).
* **Compute & Storage Operations**: Azure Kubernetes Service (AKS) lifecycle management, private cluster architecture, system/user node pool administration; Azure Blob Storage for cold diagnostic data and Azure File Shares (SMB/NFS) for container persistent volumes.
* **Centralized Telemetry**: Log Analytics Workspace (LAW) provisioning and diagnostic settings collection across VMs, AKS clusters, Azure SQL, and networking components.

#### B. Day-2 Cloud Operations & SRE Practices
* **KQL (Kusto Query Language) Log Analytics**: Writing high-performance queries using `where`, `summarize`, `project`, `extend`, and `join` across `ContainerLogV2`, `KubeEvents`, `KubePodInventory`, and `AppExceptions` tables to pinpoint incident root causes.
* **Event-Driven Automation**: Developing PowerShell and Python runbooks running inside Azure Automation Accounts, authenticated via Managed Identity to auto-remediate failing workloads without human credentials.
* **Application Insights & Distributed Tracing**: SDK instrumentation, Application Map dependency tracking, API latency breakdown across cache (Redis) and database queries, and unhandled exception triage.
* **ITSM Incident Lifecycle (ServiceNow)**: Webhook integration via Azure Logic Apps mapping Azure Monitor alerts (P1 to P4) directly to ServiceNow incident records.
* **Kubernetes Production Troubleshooting**: Real-time diagnostic procedures to resolve `OOMKilled`, `CrashLoopBackOff`, and `ImagePullBackOff` conditions using `kubectl` paired with Log Analytics event correlation.

---

### 3.2. Flagship Project: Cloud-Native Observability & Auto-Remediation System

#### [`azure-observability-auto-remediation`](https://github.com/votaquann/azure-observability-auto-remediation)
