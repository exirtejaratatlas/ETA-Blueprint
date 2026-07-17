---
document_id: ETA-ENT-QTN-003
title: Quotation Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Relationships

## Purpose

This document defines all enterprise relationships between the Quotation entity and other domains inside the ETA Enterprise Ecosystem.

Quotation is the decision layer between RFQ and Purchase Order.

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

├── Supplier

├── Manufacturer

├── Product

├── Engineering

├── Procurement

├── Purchase Order

├── Contract

├── Documents

└── AI
```

---

# RFQ

Relationship

One RFQ

↓

Many Quotations

Relationship Type

One-to-Many

Purpose

Each RFQ can receive multiple supplier quotations.

---

# Supplier

Relationship

One Supplier

↓

Many Quotations

Relationship Type

One-to-Many

Purpose

Each quotation belongs to one supplier.

---

# Manufacturer

Relationship

Many Quotations

↓

Many Manufacturers

Relationship Type

Many-to-Many

Purpose

Suppliers may offer multiple manufacturers and manufacturers appear across many quotations.

---

# Product

Relationship

One Quotation

↓

Many Product Lines

Relationship Type

One-to-Many

Purpose

Each quotation contains one or more quoted products.

---

# Engineering

Relationship

One Quotation

↓

Many Engineering Reviews

Relationship Type

One-to-Many

Purpose

Engineering validates supplier technical compliance.

---

# Procurement

Relationship

One Procurement Evaluation

↓

Many Quotations

Relationship Type

One-to-Many

Purpose

Procurement compares quotations before award.

---

# Purchase Order

Relationship

One Quotation

↓

One or Many Purchase Orders

Relationship Type

One-to-Many

Purpose

Awarded quotations generate Purchase Orders.

---

# Contract

Relationship

Many Quotations

↓

Many Contracts

Relationship Type

Many-to-Many

Purpose

Framework agreements may govern awarded quotations.

---

# Documents

Relationship

One Quotation

↓

Many Documents

Relationship Type

One-to-Many

Examples

- Commercial Proposal
- Technical Proposal
- Datasheets
- Drawings
- Certificates
- Warranty Documents
- Packing Documents

---

# AI

AI consumes quotation data for:

- Supplier Ranking
- Commercial Comparison
- Technical Comparison
- Price Benchmarking
- Cost Estimation
- Award Recommendation
- Risk Analysis
- Procurement Copilot

---

# Analytics

Quotation contributes to:

- Supplier Performance
- Win Rate
- Price Benchmark
- Cost Saving
- Procurement KPI
- Executive Dashboard
- AI Learning Dataset

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| RFQ | One-to-Many |
| Supplier | One-to-Many |
| Manufacturer | Many-to-Many |
| Product | One-to-Many |
| Engineering Review | One-to-Many |
| Procurement Evaluation | One-to-Many |
| Purchase Order | One-to-Many |
| Contract | Many-to-Many |
| Documents | One-to-Many |

---

# Long-Term Vision

The Quotation entity acts as the enterprise evaluation hub, transforming supplier offers into measurable procurement decisions through engineering validation, commercial comparison, AI recommendations, and award governance.