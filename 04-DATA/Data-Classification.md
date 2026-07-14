---
document_id: ETA-DATA-013
title: Data Classification
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
website: https://exiratlas.com
classification: Internal
last_updated: 2026
---

# ETA Data Classification

## Purpose

This document defines the enterprise data classification framework used throughout the ETA Enterprise Procurement Ecosystem.

Data classification determines how information is stored, protected, accessed, transmitted, archived, and processed by humans and AI.

---

# Classification Principles

ETA follows these principles

- Least Privilege
- Need to Know
- Zero Trust
- Encryption by Default
- AI Safe Access
- Auditability
- Regulatory Compliance

---

# Classification Levels

## Level 1 — Public

Description

Information approved for public release.

Examples

- Website content
- Company brochure
- Public product catalog
- Marketing materials
- Press releases

Access

Public

Encryption

Optional

AI Access

Allowed

Export

Allowed

Retention

Unlimited

---

## Level 2 — Internal

Description

Internal operational information.

Examples

- Internal procedures
- Organization charts
- Department documentation
- Internal reports
- Project documentation

Access

Employees

Encryption

Recommended

AI Access

Allowed

Export

Controlled

Retention

According to business policy

---

## Level 3 — Confidential

Description

Sensitive business information.

Examples

- Customers
- Suppliers
- Manufacturers
- Opportunities
- RFQs
- Quotations
- Purchase Orders
- Contracts
- Engineering documents

Access

Authorized Departments

Encryption

Required

AI Access

Allowed only through governed enterprise AI

Export

Approval Required

Audit Logging

Mandatory

Retention

Business retention policy

---

## Level 4 — Restricted

Description

Highly sensitive operational information.

Examples

- Financial records
- Banking information
- Employee records
- Payroll
- Tax documents
- Legal documents
- Compliance reports

Access

Authorized Personnel Only

Encryption

Mandatory

AI Access

Restricted

Export

Management Approval Required

Audit Logging

Mandatory

Retention

Legal requirements

---

## Level 5 — Highly Restricted

Description

Critical enterprise security assets.

Examples

- Password hashes
- API Keys
- OAuth Secrets
- Encryption Keys
- Certificates
- Security configurations
- Infrastructure credentials
- AI system secrets
- Enterprise prompt library
- AI orchestration configuration

Access

Security Administrators Only

Encryption

Mandatory

AI Access

Prohibited unless explicitly approved

Export

Prohibited

Audit Logging

Mandatory

Retention

Security policy

---

# AI Classification Rules

AI may access

- Public
- Internal
- Approved Confidential

AI may not directly access

- Restricted
- Highly Restricted

unless explicit authorization exists.

---

# Data Handling Requirements

## Public

Freely shareable.

---

## Internal

Internal collaboration only.

---

## Confidential

Secure transmission required.

Encrypted storage required.

---

## Restricted

Role-based access control.

Encryption mandatory.

Multi-factor authentication recommended.

---

## Highly Restricted

Dedicated access controls.

Security monitoring.

Continuous auditing.

No uncontrolled replication.

---

# Storage Requirements

Public

Standard Storage

Internal

Enterprise Storage

Confidential

Encrypted Storage

Restricted

Encrypted + Access Controlled

Highly Restricted

Dedicated Secure Storage

---

# Transmission Requirements

Public

HTTPS

Internal

TLS

Confidential

TLS + Authentication

Restricted

Encrypted Channel + Approval

Highly Restricted

Dedicated Secure Channels

---

# Backup Requirements

Public

Standard Backup

Internal

Daily Backup

Confidential

Encrypted Backup

Restricted

Encrypted + Isolated Backup

Highly Restricted

Offline + Encrypted Backup

---

# AI Memory Policy

Only approved enterprise knowledge may enter

- Vector Database
- Knowledge Graph
- Long-Term AI Memory

Sensitive business data requires explicit approval before AI indexing.

---

# Compliance

ETA aligns with

- ISO 27001
- ISO 9001
- GDPR (where applicable)
- Internal Information Security Policies

---

# Responsibilities

Executive Management

Enterprise Policy

Security Officer

Classification Enforcement

Data Owner

Classification Decision

Data Steward

Monitoring

AI Governance Lead

AI Classification Compliance

---

# Success Metrics

100% classified enterprise data

100% encrypted restricted data

100% audit logging for restricted access

0 unauthorized AI access

0 uncontrolled exports

---

# Long-Term Vision

ETA maintains an enterprise-wide information classification framework where every business record, engineering asset, procurement transaction, AI memory, document, and security artifact is consistently classified, protected, governed, and monitored according to its business value and risk across the entire Exir Tejarat Atlas ecosystem.