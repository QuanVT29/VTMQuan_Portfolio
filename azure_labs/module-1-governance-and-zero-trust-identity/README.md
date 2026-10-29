# Module 01: Cloud Governance, Zero-Trust Identity & Financial Guardrails

## 1. Overview & Architectural Context

In an enterprise-grade cloud environment, operational excellence begins before any virtual machine or container is provisioned. Establishing robust **Governance, Zero-Trust Identity, and Cost Guardrails** ensures that infrastructure remains compliant, auditable, secure, and protected against budget overruns.

This module lays the operational foundation for the entire platform, adhering to the **AZ-104 Azure Administrator** standard and enterprise Cloud Operations requirements.

---

## 2. Azure Management Hierarchy

Azure enforces a strict 4-level hierarchical governance model. Every resource deployed to the platform inherits access controls, compliance rules, and audit configurations from the levels above it.

![](module-1-governance-and-zero-trust-identity/images/Management_Hierarchy.png)



### Hierarchy Breakdown

| Hierarchy Level | Functional Scope | Cloud-Ops Responsibility |
| :--- | :--- | :--- |
| **Microsoft Entra ID Tenant** | Global Identity Boundary | Centralized user, group, and enterprise application lifecycle management. |
| **Management Groups** | Cross-Subscription Policy Scope | Apply organizational compliance (Azure Policy) and baseline RBAC across multiple subscriptions simultaneously. |
| **Subscriptions** | Billing & Quota Boundary | Tracks cloud expenditures, establishes service limits (vCPU quotas), and isolates environments. |
| **Resource Groups (RG)** | Lifecycle & Logical Grouping | Groups resources that share the same lifecycle (e.g., provisioned, updated, and decommissioned together). |
| **Resources** | Functional Infrastructure | The actual operational instances (e.g., AKS clusters, Managed Disks, VNets). |

> **Operational Insight:** Unlike AWS, where resources reside directly inside an Account, Azure **strictly requires** every single resource to reside within exactly one Resource Group. Deleting a Resource Group triggers a cascading, atomic deletion of all encapsulated resources—preventing orphaned infrastructure and lingering costs.

---


## 3. Identity vs. Access Management: AuthN vs. AuthZ

Enterprise security requires a strict separation of concerns between identity verification and access permissions:
