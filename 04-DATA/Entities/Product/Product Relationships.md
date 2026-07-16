---
document_id: ETA-ENT-PRODUCT-003
title: Product Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product Relationships

## Purpose

This document defines all enterprise relationships between the Product entity and other business domains within the ETA Enterprise Ecosystem.

Products serve as the central enterprise object connecting engineering, procurement, inventory, logistics, finance, CRM, AI, and project management.

---

# Enterprise Relationship Overview

```
Product

├── Customer

├── Supplier

├── Manufacturer

├── RFQ

├── Quotation

├── Purchase Order

├── Sales Order

├── Inventory

├── Shipment

├── Contract

├── Project

├── Invoice

├── Payment

├── Document

├── AI Knowledge

└── Analytics
```

---

# Customer Domain

Relationship

Many Customers

↓

Many Products

Purpose

Customers request, purchase, approve, and consume Products.

Relationship Type

Many-to-Many

---

# Supplier Domain

Relationship

Many Suppliers

↓

Many Products

One Product may have multiple approved suppliers.

Relationship Type

Many-to-Many

---

# Manufacturer Domain

Relationship

One Manufacturer

↓

Many Products

Each Product has one Primary Manufacturer but may support alternate OEMs.

Relationship Type

One-to-Many

---

# RFQ Domain

Relationship

One RFQ

↓

Many Products

Each RFQ may contain multiple Product lines.

Relationship Type

One-to-Many

---

# Quotation Domain

Relationship

One Quotation

↓

Many Products

Quoted pricing is maintained per Product line.

Relationship Type

One-to-Many

---

# Purchase Order Domain

Relationship

One Purchase Order

↓

Many Products

Products are procured through Purchase Orders.

Relationship Type

One-to-Many

---

# Sales Order Domain

Relationship

One Sales Order

↓

Many Products

Products are sold through Sales Orders.

Relationship Type

One-to-Many

---

# Inventory Domain

Relationship

One Product

↓

Many Inventory Records

Inventory exists per warehouse, company, and location.

Relationship Type

One-to-Many

---

# Shipment Domain

Relationship

One Shipment

↓

Many Products

Products participate in inbound and outbound shipments.

Relationship Type

One-to-Many

---

# Contract Domain

Relationship

Many Contracts

↓

Many Products

Products may be governed by commercial agreements and framework contracts.

Relationship Type

Many-to-Many

---

# Project Domain

Relationship

Many Projects

↓

Many Products

Projects consume Products for execution.

Relationship Type

Many-to-Many

---

# Invoice Domain

Relationship

One Invoice

↓

Many Products

Products appear as invoice lines.

Relationship Type

One-to-Many

---

# Payment Domain

Products do not directly own Payments.

Payments relate through:

Product

↓

Purchase Order

↓

Invoice

↓

Payment

---

# Document Domain

Relationship

One Product

↓

Many Documents

Supported documents include:

- Datasheets
- Catalogs
- Manuals
- Certificates
- GA Drawings
- Test Reports
- Photos
- Technical Files

Relationship Type

One-to-Many

---

# AI Domain

AI consumes Product information for:

- Product Matching
- Alternative Products
- Cross Reference
- Technical Comparison
- Semantic Search
- Knowledge Graph
- Procurement Copilot
- Engineering Copilot

---

# Analytics Domain

Products contribute to:

- Revenue Analysis
- Procurement Spend
- Inventory Turnover
- Product Profitability
- Demand Forecasting
- Supplier Performance
- Manufacturer Performance
- Executive Dashboards

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| Customer | Many-to-Many |
| Supplier | Many-to-Many |
| Manufacturer | One-to-Many |
| RFQ | One-to-Many |
| Quotation | One-to-Many |
| Purchase Order | One-to-Many |
| Sales Order | One-to-Many |
| Inventory | One-to-Many |
| Shipment | One-to-Many |
| Contract | Many-to-Many |
| Project | Many-to-Many |
| Invoice | One-to-Many |
| Document | One-to-Many |

---

# Long-Term Vision

The Product entity becomes the central enterprise hub of the ETA ecosystem, linking every commercial, engineering, procurement, logistics, financial, and AI process through a unified enterprise product model.