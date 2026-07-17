---
document_id: ETA-ENT-QTN-001
title: Quotation Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Entity

## Purpose

The Quotation entity represents the complete commercial and technical proposal submitted by a supplier in response to an RFQ.

It serves as the primary evaluation object for supplier selection, commercial comparison, technical validation, negotiation, procurement approval, and purchase award.

---

# Business Objectives

The Quotation entity enables ETA to:

- Receive supplier offers
- Compare multiple quotations
- Validate technical compliance
- Evaluate commercial conditions
- Record negotiations
- Support AI-assisted supplier ranking
- Preserve procurement traceability
- Generate Purchase Orders

---

# Core Responsibilities

The Quotation manages:

- Supplier Proposal
- Commercial Proposal
- Technical Proposal
- Pricing
- Delivery Commitments
- Incoterms
- Payment Terms
- Technical Deviations
- Commercial Deviations
- Evaluation Scores
- Award Recommendation

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

Every quotation owns one immutable:

Quotation ID

Example

```
QTN-2026-000487
```

---

# Business Keys

Additional identifiers include:

- Quotation Number
- Supplier Quotation Number
- RFQ Number
- Supplier Reference
- Internal Procurement Reference

---

# Quotation Types

Supported quotation types

- Budgetary Quotation
- Budgetary Binding
- Commercial Quotation
- Technical Quotation
- Final Offer
- Revised Offer
- Negotiated Offer
- Framework Agreement Offer

---

# Quotation Status

Supported lifecycle states

- Draft
- Submitted
- Under Technical Review
- Under Commercial Review
- Clarification Requested
- Revised
- Approved
- Rejected
- Awarded
- Expired
- Archived

---

# Enterprise Characteristics

Every quotation supports:

- Multiple Product Lines
- Multiple Revisions
- Multiple Attachments
- Multiple Currencies
- Multiple Delivery Schedules
- Multiple Taxes
- Multiple Evaluation Scores
- Multi-language Communication

---

# Related Domains

Quotation integrates with:

- RFQ
- Supplier
- Manufacturer
- Product
- Engineering
- Procurement
- Purchase Order
- Contract
- AI
- Documents

---

# Odoo Mapping

Primary Models

```
purchase.order

purchase.order.line
```

ETA extends Odoo with quotation comparison, technical evaluation, commercial scoring, AI procurement intelligence, and enterprise approval workflows.

---

# AI Integration

AI uses quotation information for:

- Supplier Ranking
- Price Benchmarking
- Alternative Recommendations
- Delivery Prediction
- Commercial Risk Analysis
- Technical Comparison
- Award Recommendation
- Procurement Copilot

---

# Long-Term Vision

The Quotation entity becomes the enterprise decision layer of ETA, transforming supplier responses into transparent, measurable, AI-assisted procurement decisions while maintaining complete commercial and technical traceability.