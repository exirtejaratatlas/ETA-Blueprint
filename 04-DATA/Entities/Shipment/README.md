---
document_id: ETA-ENT-SHP-000
title: Shipment Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment Entity

## Purpose

The Shipment entity represents the complete logistics execution process within the ETA Enterprise Procurement Ecosystem.

It governs transportation, freight forwarding, customs clearance, tracking, delivery milestones, receiving, and shipment performance from supplier dispatch to final warehouse receipt.

Shipment serves as the operational bridge between Purchase Orders and Inventory.

---

# Documents

This entity consists of:

- Shipment Entity
- Shipment Attributes
- Shipment Relationships
- Shipment Business Rules
- Shipment Lifecycle
- Shipment Odoo Mapping
- Shipment API

---

# Related Domains

Shipment integrates with:

- Supplier
- Manufacturer
- Product
- Purchase Order
- Contract
- Warehouse
- Inventory
- Invoice
- Payment
- Documents
- AI

---

# Primary Odoo Models

```
stock.picking

stock.move

stock.move.line

delivery.carrier
```

ETA extends Odoo by introducing enterprise shipment orchestration, multimodal logistics, customs management, AI-powered ETA prediction, and end-to-end shipment visibility.

---

# Enterprise Role

The Shipment acts as:

- Logistics Execution
- Transportation Record
- Customs Reference
- Tracking Hub
- Delivery Monitor
- Warehouse Receiving Trigger
- Inventory Source
- AI Logistics Intelligence

---

# Shipment Types

Supported shipment types include:

- Air Freight
- Sea Freight
- Road Freight
- Rail Freight
- Courier
- Multimodal Shipment
- Local Delivery
- International Delivery
- Partial Shipment
- Consolidated Shipment

---

# Long-Term Vision

The Shipment entity becomes the logistics orchestration layer of ETA, connecting procurement, suppliers, transportation, customs, warehouses, inventory, finance, ERP, and AI into a unified enterprise shipment management platform with complete end-to-end traceability.