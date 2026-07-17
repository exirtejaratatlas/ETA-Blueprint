---
document_id: ETA-ENT-SHP-001
title: Shipment Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment Entity

## Purpose

The Shipment entity represents the complete physical movement of goods from supplier to the final destination.

It manages transportation, customs, freight forwarding, logistics milestones, warehouse receiving, shipment visibility, and operational execution across the ETA Enterprise Procurement Ecosystem.

---

# Business Objectives

The Shipment enables ETA to:

- Track shipments end-to-end
- Manage international logistics
- Coordinate customs clearance
- Monitor transportation performance
- Support warehouse receiving
- Connect procurement with inventory
- Predict delays using AI
- Maintain complete shipment traceability

---

# Core Responsibilities

The Shipment manages:

- Shipment Header
- Shipment Lines
- Transportation
- Carrier
- Containers
- Tracking
- Customs
- Delivery
- Receiving
- Logistics Documents
- ETA Prediction
- AI Monitoring

---

# Entity Ownership

Business Owner

Logistics Department

Operational Owner

Supply Chain Department

System Owner

ETA Platform

---

# Primary Identifier

Every Shipment owns one immutable:

Shipment ID

Example

```
SHP-2026-000145
```

---

# Business Keys

Additional identifiers include:

- Shipment Number
- Tracking Number
- Bill of Lading
- Air Waybill
- Container Number
- Customs Declaration Number

---

# Shipment Types

Supported shipment types

- Air Freight
- Sea Freight
- Road Freight
- Rail Freight
- Courier
- Multimodal
- Domestic
- International
- Partial Shipment
- Consolidated Shipment

---

# Shipment Status

Supported lifecycle states

- Draft
- Planned
- Booked
- Dispatched
- In Transit
- Customs Clearance
- Arrived
- Receiving
- Completed
- Closed
- Archived

---

# Enterprise Characteristics

Every Shipment supports:

- Multiple Products
- Multiple Containers
- Multiple Tracking Events
- Multiple Documents
- Multiple Deliveries
- Multiple Warehouse Receipts
- Multi Currency
- Multi Company

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

# Odoo Mapping

Primary Enterprise Models

```
stock.picking

stock.move

stock.move.line

delivery.carrier
```

ETA extends Odoo with enterprise logistics orchestration, customs management, multimodal transportation, AI shipment prediction, and end-to-end shipment governance.

---

# AI Integration

AI analyzes Shipments for:

- ETA Prediction
- Delay Detection
- Route Optimization
- Carrier Performance
- Customs Risk
- Delivery Forecast
- Logistics KPI
- Executive Copilot

---

# Long-Term Vision

The Shipment entity becomes the logistics execution backbone of ETA, connecting procurement, transportation, customs, warehouses, inventory, ERP, finance, and AI into a unified enterprise shipment management platform with complete operational traceability.