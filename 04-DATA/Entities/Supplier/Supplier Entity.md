---
document_id: ETA-ENT-SUPPLIER-001
title: Supplier Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier Entity

## Purpose

The Supplier entity represents every organization capable of supplying products, equipment, engineering services, manufacturing services, logistics services, or commercial support to ETA.

Suppliers are one of the core master data entities and serve as the foundation of procurement operations across the enterprise.

---

# Business Objectives

The Supplier entity enables ETA to:

- Centralize supplier information.
- Support strategic sourcing.
- Evaluate supplier performance.
- Manage procurement relationships.
- Improve purchasing efficiency.
- Reduce supplier risks.
- Enable AI-assisted supplier recommendations.
- Preserve supplier knowledge.

---

# Core Responsibilities

Supplier manages:

- Supplier Master Data
- Commercial Information
- Financial Information
- Banking Information
- Compliance Information
- Certifications
- Supplier Performance
- Risk Assessment
- AI Metadata

---

# Entity Ownership

Business Owner

Procurement Department

Technical Owner

Enterprise Architecture

System Owner

ETA Platform

---

# Primary Identifier

Every Supplier owns one immutable:

Supplier ID

Example

```
SUP-000125
```

---

# Business Keys

Additional identifiers include:

- Supplier Code
- ERP Partner Number
- Tax Number
- Registration Number
- External Vendor ID

---

# Supplier Categories

Examples

- Manufacturer
- Distributor
- Trading Company
- Service Provider
- Logistics Provider
- OEM
- EPC Contractor
- Consultant

---

# Supplier Status

Lifecycle status

- Draft
- Under Review
- Approved
- Active
- Suspended
- Inactive
- Archived

---

# Related Domains

Supplier integrates with:

- Procurement
- Product
- RFQ
- Quotation
- Purchase Order
- Contract
- Inventory
- Logistics
- Finance
- AI

---

# Odoo Mapping

Primary Model

```
res.partner
```

Partner Type

Vendor

ETA extends the native Vendor model with enterprise procurement capabilities.

---

# Enterprise Characteristics

Supplier supports:

- Multi-company
- Multi-country
- Multi-currency
- Multi-language
- Multiple Contacts
- Multiple Bank Accounts
- Multiple Certifications
- Multiple Products
- Multiple Contracts

---

# AI Integration

AI uses Supplier information for:

- Supplier Ranking
- Vendor Recommendation
- Risk Assessment
- Procurement Optimization
- Lead Time Prediction
- Price Analysis
- Supplier Scoring

---

# Long-Term Vision

The Supplier entity becomes the enterprise supplier intelligence hub, providing complete visibility into vendor capabilities, commercial relationships, procurement history, compliance, financial health, and AI-assisted sourcing across the ETA ecosystem.