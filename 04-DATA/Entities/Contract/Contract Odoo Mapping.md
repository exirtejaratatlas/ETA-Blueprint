---
document_id: ETA-ENT-CON-006
title: Contract Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Contract Odoo Mapping

## Purpose

This document defines the mapping between the ETA Contract entity and Odoo Enterprise models.

ETA extends Odoo by introducing enterprise contract governance, legal lifecycle management, procurement framework agreements, commercial compliance, and AI-powered contract intelligence.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Contract | purchase.requisition |
| Purchase Contract | purchase.order |
| Sales Contract | sale.order |
| Contract Documents | documents.document |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Contract ID | x_contract_id |
| Contract Number | name |
| Contract Type | x_contract_type |
| Customer | partner_id |
| Supplier | partner_id |
| Company | company_id |
| Contract Status | state |
| Currency | currency_id |

---

# Commercial Extensions

Custom Fields

- x_contract_value
- x_payment_terms
- x_incoterm
- x_delivery_terms
- x_warranty_period
- x_penalty_rules
- x_framework_agreement
- x_contract_scope

---

# Legal Extensions

Custom Fields

- x_governing_law
- x_jurisdiction
- x_arbitration
- x_confidentiality
- x_force_majeure
- x_intellectual_property
- x_legal_notes

---

# Lifecycle Extensions

Custom Fields

- x_effective_date
- x_expiration_date
- x_renewal_date
- x_auto_renewal
- x_amendment_number
- x_contract_version
- x_contract_owner

---

# Compliance Extensions

Custom Fields

- x_compliance_status
- x_compliance_score
- x_regulatory_requirements
- x_quality_requirements
- x_export_control
- x_sanctions_compliance

---

# AI Extensions

Custom Fields

- x_ai_contract_score
- x_ai_clause_analysis
- x_ai_risk_score
- x_ai_renewal_probability
- x_ai_recommendation
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Purchase
- Sales
- Documents
- Accounting
- Approvals
- Contacts
- Sign
- Quality

---

# Security

Supported Roles

- Legal
- Procurement
- Commercial
- Finance
- Executive
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Event Driven
- Incremental
- ERP First
- Audit Logged
- AI Enabled

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Native Odoo models remain untouched to preserve long-term upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo into an enterprise contract management platform supporting legal governance, procurement framework agreements, lifecycle control, compliance monitoring, AI intelligence, and complete enterprise traceability.