---
document_id: ETA-ENT-MANUFACTURER-001
title: Manufacturer Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer Entity

## Purpose

The Manufacturer entity represents every Original Equipment Manufacturer (OEM), factory, fabrication facility, industrial producer, or certified manufacturing organization within the ETA Enterprise Ecosystem.

Manufacturers are independent enterprise master data entities responsible for designing and producing products that are supplied either directly to ETA or indirectly through suppliers and distributors.

---

# Business Objectives

The Manufacturer entity enables ETA to:

- Centralize OEM information.
- Track manufacturing capabilities.
- Maintain engineering references.
- Manage certifications.
- Support multi-supplier sourcing.
- Preserve technical knowledge.
- Improve procurement decisions.
- Enable AI-assisted manufacturer recommendations.

---

# Core Responsibilities

Manufacturer manages:

- Manufacturer Master Data
- Production Facilities
- Engineering Capabilities
- Product Portfolio
- Certifications
- Manufacturing Standards
- Lead Times
- OEM Documentation
- AI Metadata

---

# Entity Ownership

Business Owner

Procurement Department

Technical Owner

Engineering Department

System Owner

ETA Platform

---

# Primary Identifier

Every Manufacturer owns one immutable:

Manufacturer ID

Example

```
MFG-000078
```

---

# Business Keys

Additional identifiers include:

- Manufacturer Code
- OEM Code
- Registration Number
- Tax Number
- External ERP ID

---

# Manufacturer Categories

Examples

- Pump Manufacturer
- Valve Manufacturer
- Compressor Manufacturer
- Motor Manufacturer
- Instrumentation Manufacturer
- Steel Producer
- EPC Fabricator
- OEM

---

# Manufacturer Status

Lifecycle Status

- Draft
- Under Review
- Approved
- Active
- Suspended
- Archived

---

# Related Domains

Manufacturer integrates with:

- Product
- Supplier
- Procurement
- RFQ
- Purchase Order
- Contract
- Inventory
- Logistics
- AI

---

# Odoo Mapping

Primary Model

```
res.partner
```

ETA extends Odoo with manufacturer-specific enterprise fields.

---

# Enterprise Characteristics

Manufacturer supports:

- Multiple Factories
- Multiple Countries
- Multiple Brands
- Multiple Product Families
- Multiple Certifications
- Multiple Suppliers
- Multiple Contracts

---

# AI Integration

AI uses Manufacturer information for:

- OEM Recommendation
- Product Matching
- Engineering Validation
- Risk Assessment
- Lead Time Prediction
- Capability Analysis
- Knowledge Graph

---

# Long-Term Vision

The Manufacturer entity becomes ETA's enterprise manufacturing intelligence repository, providing complete visibility into global OEM capabilities, engineering expertise, manufacturing standards, certifications, production capacity, and strategic sourcing opportunities.