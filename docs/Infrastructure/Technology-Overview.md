# Technology Overview

---

## Document Information

| Item | Details |
|------|---------|
| Document Name | Technology Overview |
| Department | Information Technology |
| Audience | All Employees |
| Version | 1.0 |
| Status | Draft |

---

# Purpose

This document provides a high-level overview of the technology environment used by BluePeak Logistics.

The environment has been designed to support business operations across multiple Australian locations while providing secure, reliable and scalable technology services.

This document introduces the major technology platforms used throughout the organisation. Detailed information about each platform is provided in the supporting infrastructure documentation.

---

# Technology Philosophy

BluePeak Logistics operates a hybrid technology environment that combines cloud services with on-premises infrastructure.

Technology decisions are guided by the following principles:

- Business First
- Realism Over Complexity
- Simplicity Wins
- Secure by Design
- Scalable Growth
- One Source of Truth

Technology exists to support business operations rather than drive them.

---

# Environment Overview

BluePeak supports approximately 320 employees across five Australian locations.

The technology environment is designed to provide consistent access to business systems, secure communication, collaboration, and operational support regardless of employee location.

Core infrastructure is centrally managed from the Brisbane Headquarters while cloud services provide collaboration and accessibility across the organisation.

---

# Core Technology Areas

| Technology Area | Purpose |
|-----------------|---------|
| Identity & Access | User authentication and access management |
| Productivity Services | Email, collaboration and document management |
| Business Applications | CRM, ERP, WMS and Fleet Management |
| Server Infrastructure | Core business services and shared resources |
| Network Infrastructure | Secure connectivity between all company locations |
| Endpoint Devices | Employee workstations, laptops and operational devices |
| Security Services | Monitoring, endpoint protection and incident response |
| Backup & Recovery | Business continuity and disaster recovery |

---

# Hybrid Technology Model

BluePeak utilises both cloud-based and on-premises services.

## Cloud Services

- Microsoft 365
- Exchange Online
- Microsoft Teams
- SharePoint Online
- OneDrive
- Microsoft Entra ID

Cloud services provide collaboration, communication and secure access for employees across all company locations.

---

## On-Premises Services

- Active Directory
- Virtual Server Infrastructure
- File Services
- Print Services
- Legacy Business System Integrations
- Backup Infrastructure

These services support business operations that require local infrastructure or integration with internal systems.

---

# Business Capability Mapping

| Business Function | Supporting Technology |
|-------------------|-----------------------|
| Employee Identity | Active Directory & Entra ID |
| Customer Communication | Microsoft 365 |
| Order Management | ERP |
| Inventory Management | Warehouse Management System (WMS) |
| Fleet Operations | Fleet Management System (FMS) |
| File Collaboration | SharePoint & OneDrive |
| Endpoint Security | Microsoft Defender |
| Security Monitoring | Splunk SIEM |

---

# Technology Stack

| Layer               | Primary Technology                                                          |
| ------------------- | --------------------------------------------------------------------------- |
| Identity            | Active Directory + Microsoft Entra ID                                       |
| Productivity        | Microsoft 365                                                               |
| Collaboration       | Teams & SharePoint                                                          |
| Email               | Exchange Online                                                             |
| Endpoint Management | Microsoft Intune *(if we decide to use it)*                                 |
| Endpoint Protection | Microsoft Defender for Endpoint                                             |
| SIEM                | Splunk Enterprise                                                           |
| Operating Systems   | Windows Server & Windows 11                                                 |
| Virtualisation      | VMware Workstation (Lab) / Hyper-V or VMware ESXi (BluePeak - we'll decide) |
| Networking          | Cisco & Fortinet *(placeholder until we decide)*                            |


# IT Operating Model

BluePeak Logistics operates a hybrid IT support model.

A small internal Information Technology team manages daily operations, user support, infrastructure, and business systems.

Specialist services such as penetration testing, after-hours security monitoring, and major technology projects are provided by trusted external partners when required.

This approach allows the organisation to maintain strong internal capability while leveraging specialist expertise where appropriate.

---

# Related Documents

- Company-Overview.md
- Business-Processes.md
- Identity-and-Access.md
- Server-Infrastructure.md
- Network-Overview.md
- Business-Applications.md

---

# SOC Perspective

Understanding the technology environment allows Security Operations to assess the business impact of security events and understand how systems interact across the organisation.

Knowledge of the environment improves investigation accuracy, incident prioritisation and communication with business stakeholders.

---

# Acceptance Criteria

After reading this document, an employee should be able to:

- Understand BluePeak's overall technology environment.
- Explain the difference between cloud and on-premises services.
- Identify the major technology areas supporting the business.
- Understand how technology enables business operations.