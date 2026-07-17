---
document_id: ETA-ENT-QTN-006
title: Quotation Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Odoo Mapping

## Purpose

This document defines the mapping between the ETA Quotation entity and Odoo Enterprise Purchasing models.

ETA extends Odoo Purchase Orders to support enterprise quotation evaluation, supplier comparison, engineering validation, AI procurement intelligence, negotiation history, and procurement governance.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Quotation | purchase.order |
| Quotation Line | purchase.order.line |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Quotation ID | x_quotation_id |
| Quotation Number | name |
| RFQ ID | requisition_id |
| Supplier | partner_id |
| Procurement Owner | user_id |
| Company | company_id |
| Currency | currency_id |
| Status | state |

---

# Product Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Product | product_id |
| Description | name |
| Quantity | product_qty |
| Unit Price | price_unit |
| Taxes | taxes_id |
| Unit of Measure | product_uom |
| Planned Date | date_planned |

---

# Commercial Extensions

Custom Fields

- x_payment_terms
- x_incoterm
- x_delivery_location
- x_delivery_time
- x_valid_until
- x_warranty_period
- x_discount_percentage
- x_freight_cost
- x_insurance_cost

---

# Engineering Extensions

Custom Fields

- x_engineering_status
- x_engineering_score
- x_technical_compliance
- x_datasheet_attached
- x_ga_drawing_attached
- x_certificates
- x_technical_deviations
- x_material_compliance

---

# Procurement Extensions

Custom Fields

- x_procurement_score
- x_supplier_rank
- x_award_status
- x_award_date
- x_negotiation_round
- x_revision
- x_procurement_notes

---

# AI Extensions

Custom Fields

- x_ai_supplier_score
- x_ai_price_score
- x_ai_lead_time
- x_ai_risk_score
- x_ai_recommendation
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Purchase
- Purchase Requisition
- Inventory
- Accounting
- Contacts
- Documents
- Project
- Quality
- Approvals

---

# Security

Supported Roles

- Procurement
- Engineering
- Compliance
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
- AI Aware

---

# Upgrade Strategy

ETA extends Purchase Orders exclusively through custom modules.

Native Odoo purchasing models remain untouched for future upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Purchase Orders into enterprise quotation objects supporting engineering review, AI-assisted procurement, supplier benchmarking, negotiation management, and award governance.