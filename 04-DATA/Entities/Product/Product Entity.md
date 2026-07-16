---
document_id: ETA-ENT-PRODUCT-001
title: Product Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product Entity

## Purpose

The Product entity represents every physical item, engineered equipment, spare part, material, service, software product, and procurement item managed throughout the ETA Enterprise Ecosystem.

Product is the central business entity connecting customers, suppliers, manufacturers, procurement, contracts, inventory, logistics, finance, projects, and AI.

---

# Business Objectives

The Product entity enables ETA to:

- Centralize enterprise product knowledge.
- Standardize engineering information.
- Support procurement automation.
- Enable AI-assisted sourcing.
- Improve inventory accuracy.
- Preserve manufacturer traceability.
- Support technical comparison.
- Integrate ERP, CRM, Procurement, and AI.

---

# Core Responsibilities

The Product entity manages:

- Product Master Data
- Engineering Specifications
- Technical Documents
- Product Classification
- Manufacturer Information
- Supplier Information
- Pricing References
- Inventory References
- Procurement References
- AI Metadata

---

# Entity Ownership

Business Owner

Engineering Department

Technical Owner

Engineering & Procurement

System Owner

ETA Platform

---

# Primary Identifier

Every Product owns one immutable:

Product ID

Example

```
PRD-000125
```

---

# Business Keys

Additional identifiers include:

- Product Code
- Internal SKU
- Manufacturer Part Number (MPN)
- OEM Code
- Customer Part Number
- UNSPSC Code
- HS Code

---

# Product Categories

Examples

- Pumps
- Compressors
- Gearboxes
- Electric Motors
- Valves
- Bearings
- Instruments
- Steel Products
- Pipes
- Flanges
- Fittings
- Gaskets
- Spare Parts
- Electrical Equipment
- Automation Equipment
- EPC Materials
- Services

---

# Product Types

Supported Product Types

- Physical Product
- Spare Part
- Raw Material
- Semi-Finished Product
- Finished Product
- Service
- Software
- Engineering Item
- Fabricated Item
- Rental Equipment

---

# Product Status

Lifecycle Status

- Draft
- Engineering Review
- Procurement Review
- Approved
- Active
- Obsolete
- Archived

---

# Enterprise Characteristics

Every Product supports:

- Multiple Manufacturers
- Multiple Suppliers
- Multiple Units of Measure
- Multiple Prices
- Multiple Warehouses
- Multiple Companies
- Multiple Languages
- Multiple Documents
- Multiple Certifications
- Multiple Revisions

---

# Related Domains

Product integrates with:

- Customer
- Supplier
- Manufacturer
- Procurement
- RFQ
- Quotation
- Purchase Order
- Inventory
- Shipment
- Contract
- Project
- Finance
- AI

---

# Odoo Mapping

Primary Models

```
product.template

product.product
```

ETA extends Odoo through enterprise engineering, procurement, AI, and technical intelligence modules.

---

# AI Integration

AI utilizes Product information for:

- Product Matching
- Alternative Recommendation
- Technical Comparison
- Engineering Copilot
- Procurement Copilot
- Price Prediction
- Lead Time Prediction
- Knowledge Graph
- Semantic Search

---

# Long-Term Vision

The Product entity becomes the enterprise product knowledge hub of ETA, connecting engineering intelligence, procurement workflows, manufacturers, suppliers, contracts, logistics, finance, AI, and customer requirements into one unified enterprise product platform.