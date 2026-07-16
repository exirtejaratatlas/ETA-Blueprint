---
document_id: ETA-ENT-SUPPLIER-006
title: Supplier Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier Odoo Mapping

## Purpose

This document defines how the ETA Supplier entity maps to Odoo Enterprise models.

ETA extends the native Odoo Vendor model while preserving upgrade compatibility.

---

# Primary Odoo Model

| ETA Entity | Odoo Model |
|------------|------------|
| Supplier | res.partner |

Partner Type

```
supplier_rank > 0
```

---

# Core Field Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Supplier ID | x_supplier_id |
| Supplier Code | ref |
| Company Name | name |
| Legal Name | x_legal_name |
| Country | country_id |
| State | state_id |
| City | city |
| Address | street |
| Postal Code | zip |
| Website | website |
| Phone | phone |
| Mobile | mobile |
| Email | email |
| VAT Number | vat |
| Currency | property_purchase_currency_id |
| Payment Terms | property_supplier_payment_term_id |
| Supplier Rating | x_supplier_rating |
| Active Flag | active |

---

# Custom ETA Fields

The following enterprise fields require custom Odoo extensions.

| Field |
|-------|
| x_supplier_id |
| x_supplier_type |
| x_ai_summary |
| x_ai_risk_score |
| x_compliance_status |
| x_kyc_status |
| x_aml_status |
| x_supplier_score |
| x_lead_time |
| x_preferred_supplier |
| x_strategic_supplier |

---

# Related Odoo Modules

Supplier integrates with:

- Contacts
- Purchase
- Inventory
- Accounting
- Documents
- Approvals
- Quality
- Sign

---

# Relationships

Supplier links to:

- purchase.order
- purchase.requisition
- account.move
- stock.picking
- documents.document
- project.project
- product.supplierinfo

---

# Security

Access is governed by Odoo Groups and ETA RBAC.

Typical roles:

- Procurement User
- Procurement Manager
- Finance
- Commercial
- Executive
- Administrator

---

# AI Extensions

ETA AI enhances Odoo with:

- Supplier Ranking
- Vendor Recommendation
- Risk Prediction
- Lead Time Forecast
- Price Benchmarking
- Supplier Copilot

These capabilities are implemented outside the standard Odoo models through ETA AI services.

---

# Upgrade Strategy

ETA follows an extension-first approach.

- Standard Odoo fields remain unchanged.
- Enterprise functionality is implemented through custom modules.
- No core Odoo models are modified directly.

---

# Long-Term Vision

The Supplier entity remains fully compatible with future Odoo Enterprise releases while providing advanced procurement intelligence, AI-assisted sourcing, and enterprise-grade supplier governance.