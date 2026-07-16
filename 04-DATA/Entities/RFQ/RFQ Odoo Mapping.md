---
document_id: ETA-ENT-RFQ-006
title: RFQ Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Odoo Mapping

## Purpose

This document defines the mapping between the ETA RFQ entity and Odoo Enterprise Procurement models.

ETA extends Odoo with enterprise procurement workflow, engineering validation, AI sourcing, supplier intelligence, quotation comparison, and procurement governance.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| RFQ | purchase.requisition |
| RFQ Line | purchase.requisition.line |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| RFQ ID | x_rfq_id |
| RFQ Number | name |
| RFQ Type | x_rfq_type |
| RFQ Status | state |
| Customer | x_customer_id |
| Opportunity | x_opportunity_id |
| Project | x_project_id |
| Priority | priority |
| Procurement Owner | user_id |
| Company | company_id |

---

# Product Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Product | product_id |
| Quantity | product_qty |
| Unit of Measure | product_uom_id |
| Description | description |
| Manufacturer | x_manufacturer_id |
| Preferred Supplier | vendor_id |

---

# Engineering Extensions

Custom Fields

- x_engineering_status
- x_datasheet_required
- x_ga_required
- x_material_requirement
- x_standard_requirement
- x_engineering_notes
- x_revision
- x_technical_risk

---

# Procurement Extensions

Custom Fields

- x_procurement_strategy
- x_budget_amount
- x_budget_approved
- x_cost_center
- x_profit_center
- x_procurement_notes
- x_supplier_count
- x_award_method

---

# Commercial Extensions

Custom Fields

- x_incoterm
- x_payment_terms
- x_currency
- x_exchange_rate
- x_delivery_location
- x_required_delivery_date
- x_partial_delivery
- x_split_award

---

# Compliance Extensions

Custom Fields

- x_export_control
- x_sanction_screening
- x_compliance_status
- x_country_restrictions
- x_certification_required

---

# AI Extensions

Custom Fields

- x_ai_supplier
- x_ai_manufacturer
- x_ai_cost_estimation
- x_ai_lead_time
- x_ai_risk_score
- x_ai_summary
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Purchase
- Inventory
- Contacts
- Documents
- Project
- Accounting
- PLM
- Quality
- Approvals

---

# Security

Supported Roles

- Procurement
- Engineering
- Compliance
- Commercial
- Finance
- Executive
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Event Driven
- Incremental
- Audit Logged
- ERP First
- AI Aware

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Core Purchase models remain untouched to preserve long-term compatibility with future Odoo Enterprise upgrades.

---

# Long-Term Vision

ETA transforms Odoo Purchase Requisitions into an intelligent enterprise sourcing platform with AI-assisted procurement, engineering governance, quotation management, and complete procurement traceability.