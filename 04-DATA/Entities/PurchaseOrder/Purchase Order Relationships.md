---
document_id: ETA-ENT-PO-003
title: Purchase Order Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order Relationships

## Purpose

This document defines all enterprise relationships between the Purchase Order entity and other domains inside the ETA Enterprise Procurement Ecosystem.

Purchase Order is the execution layer connecting supplier commitments with logistics, inventory, finance, and contract fulfillment.

---

# Enterprise Relationship Overview

```
Customer

↓

Opportunity

↓

RFQ

↓

Quotation

↓

Purchase Order

├── Supplier

├── Manufacturer

├── Product

├── Shipment

├── Inventory

├── Invoice

├── Payment

├── Contract

├── Documents

└── AI
```

---

# RFQ

Relationship

One RFQ

↓

Many Purchase Orders

Relationship Type

One-to-Many

Purpose

A single RFQ may generate multiple Purchase Orders after supplier award.

---

# Quotation

Relationship

One Quotation

↓

One or Many Purchase Orders

Relationship Type

One-to-Many

Purpose

Approved quotations generate procurement commitments.

---

# Supplier

Relationship

One Supplier

↓

Many Purchase Orders

Relationship Type

One-to-Many

Purpose

Each Purchase Order belongs to exactly one supplier.

---

# Manufacturer

Relationship

Many Purchase Orders

↓

Many Manufacturers

Relationship Type

Many-to-Many

Purpose

Products from different manufacturers may exist in the same procurement portfolio.

---

# Product

Relationship

One Purchase Order

↓

Many Product Lines

Relationship Type

One-to-Many

Purpose

Each Purchase Order contains one or more ordered products.

---

# Shipment

Relationship

One Purchase Order

↓

Many Shipments

Relationship Type

One-to-Many

Purpose

Partial deliveries and multiple logistics operations are supported.

---

# Inventory

Relationship

One Purchase Order

↓

Many Inventory Transactions

Relationship Type

One-to-Many

Purpose

Receiving goods updates warehouse inventory.

---

# Invoice

Relationship

One Purchase Order

↓

Many Supplier Invoices

Relationship Type

One-to-Many

Purpose

Suppliers may invoice partially or completely.

---

# Payment

Relationship

One Purchase Order

↓

Many Payments

Relationship Type

One-to-Many

Purpose

Supports installment payments, advances, and final settlement.

---

# Contract

Relationship

Many Purchase Orders

↓

One Contract

Relationship Type

Many-to-One

Purpose

Framework contracts may govern multiple Purchase Orders.

---

# Documents

Relationship

One Purchase Order

↓

Many Documents

Relationship Type

One-to-Many

Examples

- Purchase Order PDF
- Supplier Confirmation
- Drawings
- Certificates
- Packing List
- Inspection Reports
- Shipping Documents
- Customs Documents

---

# AI

AI consumes Purchase Order data for:

- Delivery Monitoring
- Delay Prediction
- Supplier Performance
- Cost Monitoring
- Procurement Forecasting
- Contract Compliance
- Inventory Prediction
- Executive Copilot

---

# Analytics

Purchase Orders contribute to:

- Procurement KPI
- Supplier KPI
- Delivery Performance
- Cost Saving
- Inventory Planning
- Payment Forecast
- Executive Dashboard

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| RFQ | One-to-Many |
| Quotation | One-to-Many |
| Supplier | One-to-Many |
| Manufacturer | Many-to-Many |
| Product | One-to-Many |
| Shipment | One-to-Many |
| Inventory | One-to-Many |
| Invoice | One-to-Many |
| Payment | One-to-Many |
| Contract | Many-to-One |
| Documents | One-to-Many |

---

# Long-Term Vision

The Purchase Order entity serves as the enterprise execution hub, connecting procurement commitments with supplier fulfillment, logistics, inventory, finance, contracts, and AI-driven operational intelligence across the complete Source-to-Pay lifecycle.