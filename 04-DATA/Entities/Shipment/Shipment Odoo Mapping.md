---
document_id: ETA-ENT-SHP-006
title: Shipment Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment Odoo Mapping

## Purpose

This document defines the mapping between the ETA Shipment entity and Odoo Enterprise logistics models.

ETA extends Odoo with enterprise shipment orchestration, international logistics, customs management, warehouse synchronization, AI-powered ETA prediction, and complete end-to-end shipment visibility.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Shipment | stock.picking |
| Shipment Line | stock.move |
| Package Line | stock.move.line |
| Carrier | delivery.carrier |
| Warehouse | stock.warehouse |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Shipment ID | x_shipment_id |
| Shipment Number | name |
| Purchase Order | origin |
| Supplier | partner_id |
| Company | company_id |
| Shipment Status | state |
| Warehouse | picking_type_id |
| Carrier | carrier_id |

---

# Logistics Extensions

Custom Fields

- x_tracking_number
- x_bill_of_lading
- x_air_waybill
- x_container_number
- x_transport_mode
- x_origin_port
- x_destination_port
- x_route_description
- x_freight_forwarder

---

# Customs Extensions

Custom Fields

- x_customs_status
- x_customs_declaration
- x_customs_broker
- x_import_license
- x_export_license
- x_customs_cost
- x_customs_notes

---

# Receiving Extensions

Custom Fields

- x_receiving_status
- x_receiving_date
- x_inspection_status
- x_received_quantity
- x_accepted_quantity
- x_rejected_quantity

---

# Financial Extensions

Custom Fields

- x_freight_cost
- x_insurance_cost
- x_transport_cost
- x_total_shipment_cost
- x_currency

---

# AI Extensions

Custom Fields

- x_ai_eta_prediction
- x_ai_delay_probability
- x_ai_carrier_score
- x_ai_customs_risk
- x_ai_logistics_recommendation
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Inventory
- Purchase
- Sales
- Delivery
- Barcode
- Documents
- Accounting

---

# Security

Supported Roles

- Logistics
- Warehouse
- Procurement
- Finance
- Executive
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Event Driven
- Incremental
- Warehouse First
- Audit Logged
- AI Enabled

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Native logistics models remain untouched to preserve long-term upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo into an enterprise logistics platform supporting transportation orchestration, customs management, warehouse execution, AI shipment intelligence, and complete operational traceability.