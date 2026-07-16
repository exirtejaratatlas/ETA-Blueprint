---
document_id: ETA-ENT-MANUFACTURER-006
title: Manufacturer Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer Odoo Mapping

## Purpose

This document defines how the ETA Manufacturer entity maps to Odoo Enterprise.

ETA treats manufacturers as specialized Partner records while extending the standard model through enterprise custom fields.

---

# Primary Odoo Model

| ETA Entity | Odoo Model |
|------------|------------|
| Manufacturer | res.partner |

Partner Type

```
is_company = True
```

Manufacturer Flag

```
x_is_manufacturer = True
```

---

# Core Field Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Manufacturer ID | x_manufacturer_id |
| Manufacturer Code | ref |
| Company Name | name |
| Legal Name | x_legal_name |
| Country | country_id |
| State | state_id |
| City | city |
| Address | street |
| Postal Code | zip |
| Website | website |
| Phone | phone |
| Email | email |
| VAT Number | vat |
| Active | active |

---

# Custom ETA Fields

Enterprise extensions include:

- x_manufacturer_id
- x_manufacturer_type
- x_oem_type
- x_engineering_score
- x_ai_summary
- x_ai_risk_score
- x_capability_score
- x_factory_count
- x_preferred_manufacturer
- x_strategic_manufacturer

---

# Related Odoo Modules

Manufacturer integrates with:

- Contacts
- Purchase
- Inventory
- PLM
- Manufacturing
- Documents
- Quality
- Approvals

---

# Relationships

Manufacturer links to:

- product.template
- product.product
- purchase.order
- documents.document
- mrp.bom
- quality.point

---

# Security

Supported Roles

- Engineering
- Procurement
- Commercial
- Executive
- Administrator

---

# AI Extensions

ETA AI provides:

- OEM Recommendation
- Capability Analysis
- Product Matching
- Technical Copilot
- Manufacturer Ranking
- Risk Prediction

---

# Upgrade Strategy

ETA extends Odoo through custom modules.

Core Odoo models remain untouched to ensure upgrade compatibility.

---

# Long-Term Vision

Manufacturer remains fully compatible with future Odoo Enterprise releases while supporting enterprise engineering intelligence, AI-assisted OEM selection, and strategic manufacturing governance.