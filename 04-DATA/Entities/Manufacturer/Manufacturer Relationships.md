---
document_id: ETA-ENT-MANUFACTURER-003
title: Manufacturer Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer Relationships

## Purpose

This document defines the enterprise relationships of the Manufacturer entity with all other business domains across the ETA Enterprise Ecosystem.

Manufacturers are core master data entities that define product origin, engineering capabilities, production capacity, certifications, and strategic sourcing relationships.

---

# Relationship Overview

```
Manufacturer

├── Products

├── Suppliers

├── RFQs

├── Quotations

├── Purchase Orders

├── Contracts

├── Projects

├── Shipments

├── Inventory

├── Documents

└── AI Knowledge
```

---

# Product Domain

Relationship

One Manufacturer

↓

Many Products

Every Product has one Primary Manufacturer.

Relationship Type

One-to-Many

---

# Supplier Domain

Relationship

One Manufacturer

↓

Many Suppliers

One Supplier

↓

Many Manufacturers

Relationship Type

Many-to-Many

Purpose

Manufacturers may appoint:

- Authorized Distributors
- Regional Suppliers
- Trading Companies
- EPC Partners

---

# Procurement Domain

Procurement references Manufacturer during sourcing.

Manufacturer influences:

- Approved Vendor Lists
- Preferred Vendors
- OEM Selection
- Technical Evaluation

---

# RFQ Domain

Relationship

One Manufacturer

↓

Many RFQs

Procurement may issue RFQs directly to OEMs or through suppliers.

---

# Quotation Domain

Manufacturer pricing may originate from:

- OEM
- Authorized Distributor
- Regional Partner

One Manufacturer

↓

Many Quotations

---

# Purchase Order Domain

Purchase Orders may reference:

- Manufacturer
- Supplier

This preserves OEM traceability.

---

# Contract Domain

Manufacturers may participate in:

- Supply Agreements
- OEM Agreements
- Framework Contracts
- Strategic Partnerships

Relationship

One Manufacturer

↓

Many Contracts

---

# Project Domain

Projects consume OEM products.

Relationship

One Project

↓

Many Manufacturers

One Manufacturer

↓

Many Projects

---

# Inventory Domain

Inventory preserves manufacturer traceability.

Relationship

Manufacturer

↓

Product

↓

Inventory

Important for:

- Warranty
- QA/QC
- Traceability
- Recalls

---

# Shipment Domain

Manufacturer participates in:

- Factory Shipment
- Export Shipment
- Consolidation Shipment

Relationship

Manufacturer

↓

Many Shipments

---

# Document Domain

Manufacturers own:

- Catalogs
- Datasheets
- GA Drawings
- Certificates
- Test Reports
- Manuals
- Engineering Documents

One Manufacturer

↓

Many Documents

---

# Finance Domain

Manufacturer information supports:

- Procurement Spend Analysis
- Strategic Sourcing
- Vendor Cost Analysis

Financial ownership remains under Supplier.

---

# AI Domain

AI utilizes Manufacturer data for:

- OEM Recommendation
- Product Matching
- Capability Analysis
- Alternative Manufacturer Discovery
- Risk Analysis
- Engineering Knowledge Graph
- Technical Copilot

---

# Identity Domain

Manufacturer information is protected through RBAC.

Roles

- Engineering
- Procurement
- Commercial
- Executive
- Administrator

---

# Notifications

Manufacturer events generate:

- Certification Expiration Alerts
- Engineering Updates
- Product Changes
- Supplier Changes
- Risk Notifications

---

# Reporting

Manufacturer contributes to:

- OEM Performance Dashboard
- Strategic Sourcing Reports
- Product Coverage Reports
- Engineering Reports
- Executive Analytics

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| Product | One-to-Many |
| Supplier | Many-to-Many |
| RFQ | One-to-Many |
| Quotation | One-to-Many |
| Purchase Order | One-to-Many |
| Contract | One-to-Many |
| Project | Many-to-Many |
| Shipment | One-to-Many |
| Inventory | One-to-Many |
| Document | One-to-Many |

---

# Long-Term Vision

Manufacturer becomes ETA's enterprise OEM intelligence hub, connecting engineering knowledge, products, suppliers, procurement, logistics, AI, and strategic sourcing into a unified manufacturing knowledge platform.