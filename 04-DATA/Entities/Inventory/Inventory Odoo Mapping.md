---
document_id: ETA-ENT-INV-006
title: Inventory Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Inventory Odoo Mapping

## Purpose

This document defines the mapping between the ETA Inventory entity and Odoo Enterprise Inventory models.

ETA extends Odoo by introducing enterprise inventory intelligence, AI demand forecasting, warehouse optimization, advanced stock governance, and complete inventory traceability.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Inventory | stock.quant |
| Stock Movement | stock.move |
| Stock Move Line | stock.move.line |
| Warehouse | stock.warehouse |
| Location | stock.location |
| Batch / Lot | stock.lot |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Inventory ID | x_inventory_id |
| SKU | default_code |
| Product | product_id |
| Warehouse | warehouse_id |
| Location | location_id |
| On Hand Quantity | quantity |
| Reserved Quantity | reserved_quantity |
| Company | company_id |
| Inventory Status | x_inventory_status |

---

# Warehouse Extensions

Custom Fields

- x_storage_location
- x_bin_location
- x_zone
- x_aisle
- x_rack
- x_shelf
- x_position

---

# Batch & Traceability Extensions

Custom Fields

- x_batch_number
- x_supplier_batch
- x_traceability_status
- x_country_of_origin
- x_quality_status
- x_expiration_date

---

# Valuation Extensions

Custom Fields

- x_inventory_value
- x_average_cost
- x_fifo_cost
- x_standard_cost
- x_last_purchase_cost
- x_currency

---

# Replenishment Extensions

Custom Fields

- x_reorder_point
- x_safety_stock
- x_minimum_stock
- x_maximum_stock
- x_lead_time
- x_preferred_supplier

---

# AI Extensions

Custom Fields

- x_ai_inventory_score
- x_ai_demand_forecast
- x_ai_reorder_prediction
- x_ai_stockout_risk
- x_ai_overstock_risk
- x_ai_slow_moving_score
- x_ai_dead_stock_score
- x_ai_recommendation
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Inventory
- Purchase
- Sales
- Manufacturing
- Barcode
- Accounting
- Quality

---

# Security

Supported Roles

- Warehouse
- Logistics
- Procurement
- Finance
- Executive
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Real-time
- Event Driven
- Warehouse First
- Inventory Consistent
- Audit Logged
- AI Enabled

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Native inventory models remain untouched to preserve long-term upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Inventory into an enterprise inventory intelligence platform supporting warehouse optimization, AI forecasting, stock governance, procurement synchronization, financial valuation, and complete inventory traceability.