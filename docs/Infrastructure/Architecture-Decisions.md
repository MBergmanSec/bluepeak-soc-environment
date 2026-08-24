# Architecture Decisions

## Purpose

This document records the major architectural decisions that shape the BluePeak Logistics technology environment.

It focuses on why key architectural choices were made rather than documenting detailed configurations or implementation procedures.

---

## Hybrid Infrastructure

BluePeak operates a hybrid technology environment.

Cloud services are used where they provide practical business and operational benefits, while selected on-premises infrastructure is retained for identity, integrations, security monitoring and core operational services.

This approach provides flexibility without requiring all business systems to be hosted or managed internally.

---

## Virtualisation Platform

Microsoft Hyper-V is used as BluePeak's primary on-premises virtualisation platform.

Core server workloads are virtualised where practical to simplify infrastructure management, improve resource utilisation and allow the environment to scale as business requirements change.

---

## Active Directory Resilience

BluePeak operates two Active Directory Domain Controllers.

Maintaining two Domain Controllers provides redundancy for critical identity services, including authentication and DNS, and reduces reliance on a single server.

---

## Primary Infrastructure Location

BluePeak's primary on-premises infrastructure is hosted from the Brisbane main office.

Core server workloads, virtualisation infrastructure and central security monitoring are primarily operated from Brisbane.

Regional locations rely on centrally managed services rather than maintaining unnecessary duplicate server infrastructure.

---

## Hybrid Identity

BluePeak uses on-premises Active Directory together with Microsoft Entra ID.

Active Directory provides core internal identity and authentication services, while Entra ID supports access to Microsoft 365 and other cloud-based services.

This reflects BluePeak's broader hybrid infrastructure strategy.

---

## Centralised Security Monitoring

Security telemetry from relevant systems is centrally collected and analysed using Splunk Enterprise.

BluePeak prioritises telemetry that supports meaningful detection, investigation and incident response rather than attempting to collect every available log source.

This provides the Security Operations team with central visibility while keeping monitoring proportionate to the organisation's operational requirements.

---

## Architecture Review

Architectural decisions may be reviewed as BluePeak's business requirements, technology environment and security needs evolve.

Changes that materially affect the environment should be reflected in this document.