---
document_id: ETA-ENT-INVC-006
title: Invoice Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Invoice Odoo Mapping

## Purpose

This document defines the mapping between the ETA Invoice entity and Odoo Enterprise Accounting models.

ETA extends Odoo Accounting by introducing enterprise invoice governance, procurement synchronization, AI financial intelligence, tax compliance, and executive financial analytics.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Invoice | account.move |
| Invoice Line | account.move.line |
| Tax | account.tax |
| Payment | account.payment |
| Journal | account.journal |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Invoice ID | x_invoice_id |
| Invoice Number | name |
| Invoice Type | move_type |
| Supplier | partner_id |
| Company | company_id |
| Currency | currency_id |
| Invoice Date | invoice_date |
| Due Date | invoice_date_due |
| Accounting Journal | journal_id |
| Payment State | payment_state |
| Invoice State | state |

---

# Financial Extensions

Custom Fields

- x_supplier_invoice_number
- x_contract_reference
- x_purchase_order_reference
- x_shipment_reference
- x_inventory_reference
- x_cost_center
- x_profit_center
- x_business_unit

---

# Tax Extensions

Custom Fields

- x_tax_validation_status
- x_customs_tax
- x_withholding_tax
- x_tax_compliance_score

---

# Three-Way Matching Extensions

Custom Fields

- x_matching_status
- x_matching_score
- x_matching_exception
- x_matching_notes

---

# AI Extensions

Custom Fields

- x_ai_fraud_score
- x_ai_duplicate_detection
- x_ai_payment_priority
- x_ai_financial_risk
- x_ai_cashflow_prediction
- x_ai_summary
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Accounting
- Purchase
- Sales
- Inventory
- Documents
- Payments
- Expenses

---

# Security

Supported Roles

- Finance
- Accounting
- Procurement
- Executive
- Auditor
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Real-Time
- Event Driven
- Financial First
- Audit Logged
- AI Enabled

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Native accounting models remain untouched to preserve long-term upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Accounting into an enterprise financial intelligence platform supporting invoice governance, procurement-finance synchronization, tax compliance, AI validation, executive analytics, and complete financial traceability.