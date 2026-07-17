---
document_id: ETA-ENT-PO-006
title: Purchase Order Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order Odoo Mapping

## Purpose

This document defines the mapping between the ETA Purchase Order entity and Odoo Enterprise Purchasing models.

ETA extends Odoo Purchase Orders with enterprise procurement governance, supplier collaboration, logistics tracking, inventory synchronization, AI monitoring, and complete auditability.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Purchase Order | purchase.order |
| Purchase Order Line | purchase.order.line |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Purchase Order ID | x_purchase_order_id |
| Purchase Order Number | name |
| Supplier | partner_id |
| RFQ Reference | requisition_id |
| Buyer | user_id |
| Company | company_id |
| Currency | currency_id |
| Status | state |

---

# Purchase Order Line Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Product | product_id |
| Description | name |
| Quantity | product_qty |
| Unit Price | price_unit |
| Taxes | taxes_id |
| UOM | product_uom |
| Planned Date | date_planned |

---

# Commercial Extensions

Custom Fields

- x_payment_terms
- x_incoterm
- x_contract_reference
- x_delivery_location
- x_delivery_schedule
- x_warranty_period
- x_discount_percentage
- x_total_lead_time

---

# Logistics Extensions

Custom Fields

- x_shipment_status
- x_tracking_number
- x_carrier
- x_bill_of_lading
- x_partial_delivery
- x_receiving_status
- x_inventory_status

---

# Financial Extensions

Custom Fields

- x_invoice_status
- x_invoice_reference
- x_payment_status
- x_payment_reference
- x_remaining_balance
- x_cost_center
- x_profit_center

---

# AI Extensions

Custom Fields

- x_ai_supplier_score
- x_ai_delivery_prediction
- x_ai_delay_risk
- x_ai_procurement_summary
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Purchase
- Purchase Requisition
- Inventory
- Accounting
- Documents
- Approvals
- Quality
- Contacts

---

# Security

Supported Roles

- Procurement
- Engineering
- Logistics
- Warehouse
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

Native Purchase models remain untouched to preserve future upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Purchase Orders into enterprise procurement execution objects supporting supplier collaboration, logistics orchestration, inventory integration, finance automation, AI monitoring, and full Source-to-Pay governance.