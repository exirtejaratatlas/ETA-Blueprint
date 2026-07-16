---
document_id: ETA-ENT-RFQ-003
title: RFQ Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Relationships

## Purpose

This document defines all enterprise relationships between the RFQ entity and other domains inside the ETA Enterprise Ecosystem.

RFQ is the central transaction connecting Customer demand with Procurement execution.

---

# Enterprise Relationship Overview

```
Customer

↓

Opportunity

↓

RFQ

├── Product

├── Supplier

├── Manufacturer

├── Engineering

├── Quotation

├── Purchase Order

├── Contract

├── Project

├── Documents

└── AI
```

---

# Customer

Relationship

One Customer

↓

Many RFQs

Relationship Type

One-to-Many

Purpose

One customer may submit multiple RFQs.

---

# Opportunity

Relationship

One Opportunity

↓

Many RFQs

Relationship Type

One-to-Many

Purpose

Commercial opportunities may generate several RFQs.

---

# Product

Relationship

One RFQ

↓

Many Products

Relationship Type

One-to-Many

Purpose

Each RFQ contains one or more requested products.

---

# Supplier

Relationship

Many RFQs

↓

Many Suppliers

Relationship Type

Many-to-Many

Purpose

An RFQ may be sent to multiple suppliers and suppliers receive multiple RFQs.

---

# Manufacturer

Relationship

Many RFQs

↓

Many Manufacturers

Relationship Type

Many-to-Many

Purpose

Manufacturers are referenced for OEM validation and approved alternatives.

---

# Engineering

Relationship

One RFQ

↓

Many Engineering Reviews

Relationship Type

One-to-Many

Purpose

Engineering validates technical specifications before procurement.

---

# Quotation

Relationship

One RFQ

↓

Many Quotations

Relationship Type

One-to-Many

Purpose

Each invited supplier may submit one quotation.

---

# Purchase Order

Relationship

One RFQ

↓

Many Purchase Orders

Relationship Type

One-to-Many

Purpose

Awarded quotations generate Purchase Orders.

---

# Contract

Relationship

Many RFQs

↓

Many Contracts

Relationship Type

Many-to-Many

Purpose

Framework agreements and long-term contracts may govern RFQs.

---

# Project

Relationship

One Project

↓

Many RFQs

Relationship Type

One-to-Many

Purpose

Projects usually generate multiple procurement requests.

---

# Documents

Relationship

One RFQ

↓

Many Documents

Relationship Type

One-to-Many

Examples

- Datasheets
- RFQ Files
- Drawings
- BOQ
- Technical Specifications
- Commercial Attachments

---

# AI

AI consumes RFQ information for:

- Supplier Recommendation
- Manufacturer Recommendation
- Product Matching
- Alternative Products
- Cost Estimation
- Lead Time Prediction
- Risk Analysis
- Procurement Copilot

---

# Analytics

RFQ contributes to:

- Procurement KPIs
- Supplier Performance
- Procurement Cycle Time
- Cost Saving
- Response Rate
- Award Rate
- Executive Dashboards

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| Customer | One-to-Many |
| Opportunity | One-to-Many |
| Product | One-to-Many |
| Supplier | Many-to-Many |
| Manufacturer | Many-to-Many |
| Engineering Review | One-to-Many |
| Quotation | One-to-Many |
| Purchase Order | One-to-Many |
| Contract | Many-to-Many |
| Project | One-to-Many |
| Documents | One-to-Many |

---

# Long-Term Vision

The RFQ entity acts as the enterprise orchestration point that transforms customer demand into engineering validation, supplier engagement, commercial evaluation, purchasing decisions, and AI-assisted procurement intelligence.