---
document_id: ETA-ENT-RFQ-001
title: RFQ Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Entity

## Purpose

The Request for Quotation (RFQ) entity represents the formal procurement request issued by ETA to one or more suppliers for obtaining commercial and technical quotations.

The RFQ serves as the primary transaction that initiates the enterprise sourcing process.

---

# Business Objectives

The RFQ entity enables ETA to:

- Standardize procurement requests.
- Centralize sourcing activities.
- Support multi-supplier quotations.
- Preserve engineering requirements.
- Improve supplier response quality.
- Enable AI-assisted sourcing.
- Maintain procurement traceability.
- Integrate ERP, CRM, and Procurement.

---

# Core Responsibilities

The RFQ manages:

- Customer Requirements
- Product Requirements
- Technical Specifications
- Supplier Invitations
- Manufacturer References
- Engineering Documents
- Commercial Conditions
- Procurement Workflow
- Approval Process
- AI Recommendations

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

Every RFQ owns one immutable:

RFQ ID

Example

```
RFQ-2026-000154
```

---

# Business Keys

Additional identifiers include:

- RFQ Number
- Customer RFQ Number
- Project Number
- Opportunity Number
- Procurement Reference
- External Reference

---

# RFQ Types

Supported RFQ Types

- Customer RFQ
- Internal RFQ
- Strategic RFQ
- Budgetary RFQ
- Competitive RFQ
- Emergency RFQ
- Repeat RFQ
- Project RFQ

---

# RFQ Status

Supported lifecycle states

- Draft
- Engineering Review
- Procurement Review
- Approved
- Sent
- Supplier Responding
- Quotation Received
- Evaluation
- Awarded
- Closed
- Cancelled

---

# Enterprise Characteristics

Every RFQ supports:

- Multiple Products
- Multiple Suppliers
- Multiple Manufacturers
- Multiple Attachments
- Multiple Revisions
- Multiple Currencies
- Multiple Companies
- Multi-language Communication

---

# Related Domains

RFQ integrates with:

- Customer
- Product
- Supplier
- Manufacturer
- Quotation
- Purchase Order
- Contract
- Project
- Document
- AI

---

# Odoo Mapping

Primary Models

```
purchase.requisition

purchase.requisition.line
```

ETA extends Odoo with enterprise procurement workflow, quotation comparison, AI sourcing, and engineering approval capabilities.

---

# AI Integration

AI utilizes RFQ information for:

- Supplier Recommendation
- Alternative Manufacturer Discovery
- Technical Matching
- Procurement Copilot
- Lead Time Prediction
- Cost Estimation
- Risk Assessment
- Semantic Search

---

# Long-Term Vision

The RFQ entity becomes the intelligent procurement gateway of ETA, connecting customer demand, engineering validation, supplier collaboration, AI-driven sourcing, and enterprise purchasing into one unified procurement process.