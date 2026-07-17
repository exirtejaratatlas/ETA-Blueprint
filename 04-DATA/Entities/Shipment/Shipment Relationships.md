---
document_id: ETA-ENT-SHP-003
title: Shipment Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment Relationships

## Purpose

This document defines all enterprise relationships between the Shipment entity and other domains inside the ETA Enterprise Procurement Ecosystem.

Shipment is the operational logistics hub connecting procurement execution with warehouse operations, inventory, finance, customs, and AI logistics intelligence.

---

# Enterprise Relationship Overview

```
Supplier

↓

Purchase Order

↓

Shipment

├── Manufacturer

├── Product

├── Contract

├── Warehouse

├── Inventory

├── Invoice

├── Payment

├── Documents

└── AI
```

---

# Supplier

Relationship

One Supplier

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

A supplier may dispatch multiple shipments.

---

# Manufacturer

Relationship

One Manufacturer

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

Manufacturers may produce goods shipped in multiple deliveries.

---

# Product

Relationship

Many Products

↓

Many Shipments

Relationship Type

Many-to-Many

Purpose

Each shipment contains multiple products, and products may appear in multiple shipments.

---

# Purchase Order

Relationship

One Purchase Order

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

Purchase Orders may be fulfilled through partial or multiple shipments.

---

# Contract

Relationship

One Contract

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

Shipment execution follows contractual obligations.

---

# Warehouse

Relationship

One Warehouse

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

Shipments are received into designated warehouses.

---

# Inventory

Relationship

One Shipment

↓

Many Inventory Transactions

Relationship Type

One-to-Many

Purpose

Receiving a shipment generates inventory movements.

---

# Invoice

Relationship

One Shipment

↓

Many Invoices

Relationship Type

One-to-Many

Purpose

Shipments support supplier invoice validation.

---

# Payment

Relationship

Shipment

↓

Payment Verification

Relationship Type

Supporting Relationship

Purpose

Payment release may depend on shipment completion and receiving confirmation.

---

# Documents

Relationship

One Shipment

↓

Many Documents

Relationship Type

One-to-Many

Examples

- Bill of Lading
- Air Waybill
- Packing List
- Commercial Invoice
- Certificate of Origin
- Insurance Certificate
- Customs Documents
- Delivery Note
- Inspection Reports

---

# AI

AI consumes Shipment information for:

- ETA Prediction
- Delay Detection
- Route Optimization
- Carrier Performance
- Customs Risk Analysis
- Logistics KPI
- Executive Copilot

---

# Analytics

Shipment contributes to:

- Logistics Performance
- Supplier Delivery Performance
- Carrier Performance
- Inventory Lead Time
- Customs Efficiency
- Procurement KPI
- Executive Dashboard

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| Supplier | One-to-Many |
| Manufacturer | One-to-Many |
| Product | Many-to-Many |
| Purchase Order | One-to-Many |
| Contract | One-to-Many |
| Warehouse | One-to-Many |
| Inventory | One-to-Many |
| Invoice | One-to-Many |
| Payment | Supporting |
| Documents | One-to-Many |

---

# Long-Term Vision

The Shipment entity serves as the enterprise logistics orchestration layer of ETA, connecting procurement, transportation, customs, warehouses, inventory, finance, ERP, AI, and analytics into a fully traceable end-to-end logistics ecosystem.