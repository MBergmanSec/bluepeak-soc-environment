# Departments

| Document Information | |
|----------------------|------------------------------------------------|
| Document Name | Departments |
| Version | 1.0 |
| Status | Draft |
| Owner | BluePeak Security Operations |
| Last Reviewed | 27 July 2026 |
| Next Review | As Required |

BluePeak's departments operate as an interconnected business ecosystem.

Warehouse Operations fulfil customer orders.

Transport & Fleet deliver those orders.

Customer Service supports customers throughout the process.

Finance manages payments.

HR supports employees.

IT provides technology services.

The Security Operations team helps protect the systems and information that enable every department to perform its role.

---

# 1. Objective

Provide an overview of the business departments that make up BluePeak Logistics, their primary responsibilities, the systems they rely on, and the role each plays in delivering business operations.

---

# 2. Audience

This document is intended for:

- IT Support Engineers
- Systems Administrators
- Network Engineers
- Security Operations (SOC)
- Security Engineers
- Other technical employees

---

# 3. Overview

BluePeak Logistics is made up of several business units that work together to deliver reliable logistics and warehousing services across Queensland and New South Wales.

Each department has unique operational responsibilities but relies on shared technology platforms and collaboration to support customers and maintain daily operations.

Understanding the responsibilities and dependencies of each department enables technical teams to better assess business impact, prioritise incidents, and provide effective support.

---

# Executive Leadership

### Business Function

Provides strategic direction and executive oversight for the organisation.

### Primary Responsibilities

- Company strategy
- Financial oversight
- Governance
- Major business decisions
- Regulatory compliance

### Common Job Titles

- Chief Executive Officer (CEO)
- Chief Operating Officer (COO)
- Chief Financial Officer (CFO)
- Chief Information Officer (CIO)

### Key Business Systems

- Microsoft 365
- Business Intelligence dashboards
- Financial reporting platforms

### Data Classification

- Corporate strategy
- Financial reports
- Board documentation

### Operational Dependencies

Executive leadership supports business decision making across all departments.

### SOC Perspective

Executive accounts are attractive targets for Business Email Compromise (BEC), credential theft, and targeted phishing attacks due to their authority and access to sensitive business information.

---

# Finance

### Business Function

Manages BluePeak's financial operations and ensures accurate financial reporting.

### Primary Responsibilities

- Payroll
- Accounts payable
- Accounts receivable
- Budgeting
- Financial reporting

### Common Job Titles

- Finance Manager
- Payroll Officer
- Accountant
- Accounts Officer

### Key Business Systems

- ERP
- Payroll System
- Microsoft 365
- Banking Platforms

### Data Classification

- Financial records
- Payroll information
- Banking details

### Operational Dependencies

Supports payroll, supplier payments, and financial reporting. Extended outages may delay employee payments and vendor transactions.

### SOC Perspective

Finance users are common targets for invoice fraud, Business Email Compromise (BEC), phishing campaigns, and attempts to manipulate payment processes.

---

# Human Resources

### Business Function

Manages employee lifecycle processes from recruitment through to offboarding.

### Primary Responsibilities

- Recruitment
- Employee records
- Onboarding
- Offboarding
- Performance administration

### Common Job Titles

- HR Manager
- HR Advisor
- Recruitment Officer

### Key Business Systems

- HR Information System (HRIS)
- Microsoft 365
- Document Management

### Data Classification

- Personally Identifiable Information (PII)
- Employment records
- Identity documentation

### Operational Dependencies

Supports recruitment, onboarding, and workforce administration across the organisation.

### SOC Perspective

HR regularly handles sensitive personal information and frequently communicates with external applicants, making it a common target for phishing and social engineering attacks.

---

# Information Technology

### Business Function

Designs, supports, and maintains BluePeak's technology environment.

### Primary Responsibilities

- Infrastructure
- Service Desk
- Networking
- Identity management
- Endpoint management
- System administration

### Common Job Titles

- IT Manager
- Systems Administrator
- Network Administrator
- Service Desk Analyst

### Key Business Systems

- Active Directory
- Microsoft 365
- Microsoft Defender
- VMware
- Backup Systems
- Splunk

### Data Classification

- Infrastructure configuration
- Administrative credentials
- System documentation

### Operational Dependencies

Provides technology services supporting every business department.

### SOC Perspective

Administrative activity is expected within IT. Investigations involving privileged accounts require careful validation to distinguish legitimate administration from malicious behaviour.

---

# Security Operations

### Business Function

Monitors, investigates, and responds to cybersecurity events affecting BluePeak Logistics.

Business hours are covered by the internal Security Operations team. After-hours monitoring is provided by BluePeak's Managed Security Service Provider (MSSP), with critical incidents escalated to internal staff as required.

### Primary Responsibilities

- Security monitoring
- Incident response
- Threat detection
- Investigation
- Security reporting
- Security awareness

### Common Job Titles

- Security Manager
- Senior Security Analyst
- Security Analyst
- Junior SOC Analyst

### Key Business Systems

- Splunk
- Microsoft Defender
- Sysmon
- Microsoft 365 Security
- Threat Intelligence Platforms

### Data Classification

- Security alerts
- Investigation records
- Incident reports

### Operational Dependencies

Supports all business departments through monitoring, detection, and incident response.

### SOC Perspective

The SOC protects business operations through visibility and investigation but does not own business systems or data. Security works in partnership with IT and business stakeholders to reduce organisational risk.

---

# Customer Service

### Business Function

Provides frontline support for customers and shipment enquiries.

### Primary Responsibilities

- Customer enquiries
- Shipment tracking
- Issue resolution

### Common Job Titles

- Customer Service Representative
- Customer Support Lead

### Key Business Systems

- CRM
- Microsoft 365
- Shipment Tracking Platform

### Data Classification

- Customer information
- Shipment records

### Operational Dependencies

Acts as the primary communication channel between BluePeak and its customers.

### SOC Perspective

Customer-facing staff are frequent targets for phishing, social engineering, and account impersonation attempts.

---

# Warehouse Operations

### Business Function

Manages inventory, warehousing, and order fulfilment across BluePeak distribution centres.

### Primary Responsibilities

- Inventory management
- Goods receivable
- Dispatch
- Stock control
- Warehouse safety

### Common Job Titles

- Warehouse Manager
- Warehouse Supervisor
- Storeperson
- Forklift Operator

### Key Business Systems

- Warehouse Management System (WMS)
- Barcode scanners
- Inventory systems

### Data Classification

- Inventory records
- Shipment information

### Operational Dependencies

Represents BluePeak's largest operational department. Extended disruption directly affects customer deliveries and contractual obligations.

### SOC Perspective

Warehouse environments often contain shared devices, shift workers, and operational systems. Maintaining availability is typically the highest security priority.

---

# Transport & Fleet

### Business Function

Coordinates vehicle fleets and freight movement between customers and distribution centres.

### Primary Responsibilities

- Fleet scheduling
- Driver coordination
- Route management
- Vehicle compliance

### Common Job Titles

- Fleet Manager
- Transport Coordinator
- Driver

### Key Business Systems

- Fleet Management Platform
- GPS Tracking
- Microsoft 365

### Data Classification

- Vehicle records
- Route information
- Delivery schedules

### Operational Dependencies

Supports timely freight movement and customer deliveries.

### SOC Perspective

GPS systems, mobile devices, and remote connectivity increase the department's exposure to operational disruption and mobile security risks.

---

# Procurement & Supply Chain

### Business Function

Manages purchasing, supplier relationships, and inventory procurement.

### Primary Responsibilities

- Supplier management
- Purchasing
- Contract administration

### Common Job Titles

- Procurement Manager
- Purchasing Officer

### Key Business Systems

- ERP
- Supplier Portal
- Microsoft 365

### Data Classification

- Supplier contracts
- Purchase orders

### Operational Dependencies

Supports inventory availability and operational continuity.

### SOC Perspective

Compromised supplier communications or fraudulent purchase requests may disrupt operations or result in financial loss.

---

# Marketing & Communications

### Business Function

Manages BluePeak's public image and internal communications.

### Primary Responsibilities

- Website management
- Marketing campaigns
- Internal communications

### Common Job Titles

- Marketing Manager
- Marketing Coordinator

### Key Business Systems

- Content Management System
- Microsoft 365
- Social Media Platforms

### Data Classification

- Marketing material
- Brand assets

### Operational Dependencies

Supports customer engagement and corporate communications.

### SOC Perspective

Public-facing platforms require monitoring for website compromise, brand impersonation, and unauthorized content changes.

---

# Related Documents

- Company-Overview.md
- Organisation-Chart.md
- Office-Locations.md
- Critical-Business-Systems.md

---

# SOC Perspective

Understanding a user's department provides critical context during investigations.

Business function, access requirements, and operational impact all influence how alerts are prioritised and investigated. Analysts should consider departmental responsibilities alongside technical evidence when assessing risk and determining appropriate response actions.

---

# Acceptance Criteria

After reading this document, a technical employee should be able to:

- Describe the purpose of each department.
- Understand how departments support business operations.
- Identify the systems commonly used by each department.
- Recognise the types of data managed by each department.
- Understand the operational impact of disruptions.
- Appreciate the different security considerations associated with each business function.

---

## Revision History

| Version | Date | Author | Summary |
|---------|------|--------|---------|
| 1.0 | 27 Jul 2026 | BluePeak Security Operations | Initial draft created. |