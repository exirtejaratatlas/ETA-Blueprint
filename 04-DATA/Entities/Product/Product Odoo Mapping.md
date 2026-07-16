---
document_id: ETA-ENT-PRODUCT-006
title: Product Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product Odoo Mapping

## Purpose

This document defines how the ETA Product entity maps to Odoo Enterprise.

ETA extends Odoo Product Management with enterprise engineering, procurement, AI, logistics, compliance, and commercial intelligence.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Product Template | product.template |
| Product Variant | product.product |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Product ID | x_product_id |
| Product Code | default_code |
| Product Name | name |
| Product Type | detailed_type |
| Category | categ_id |
| UOM | uom_id |
| Purchase UOM | uom_po_id |
| Barcode | barcode |
| Active | active |

---

# Engineering Extensions

Custom Fields

- x_revision
- x_datasheet
- x_ga_drawing
- x_engineering_notes
- x_pressure_rating
- x_temperature_rating
- x_material
- x_grade
- x_weight
- x_dimension

---

# Procurement Extensions

Custom Fields

- x_primary_supplier
- x_preferred_supplier
- x_manufacturer
- x_manufacturer_part_number
- x_supplier_part_number
- x_procurement_category
- x_lead_time
- x_moq
- x_contract_required

---

# Inventory Extensions

Custom Fields

- x_safety_stock
- x_reorder_point
- x_maximum_stock
- x_serial_tracking
- x_batch_tracking
- x_storage_method
- x_hazardous_material

---

# Commercial Extensions

Custom Fields

- x_target_purchase_price
- x_last_purchase_price
- x_market_price
- x_currency
- x_tax_category
- x_price_valid_from
- x_price_valid_until

---

# AI Extensions

Custom Fields

- x_ai_summary
- x_ai_product_score
- x_ai_procurement_score
- x_ai_risk_score
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Contacts
- Purchase
- Sales
- Inventory
- Manufacturing
- PLM
- Quality
- Documents
- Accounting
- Project

---

# Security

Supported Roles

- Engineering
- Procurement
- Warehouse
- Commercial
- Finance
- Executive
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Event Driven
- Incremental
- Bidirectional where applicable
- Audit Logged

---

# Upgrade Strategy

ETA extends Odoo using custom modules only.

Core models remain untouched to preserve upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Product Management into an enterprise engineering and procurement platform while remaining fully compatible with future Odoo Enterprise releases.