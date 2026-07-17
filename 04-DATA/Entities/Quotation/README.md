---
document_id: ETA-ENT-QTN-000
title: Quotation Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Entity

## Purpose

The Quotation entity represents the commercial and technical response submitted by suppliers against an RFQ.

It captures pricing, technical compliance, commercial conditions, delivery commitments, supplier deviations, and procurement evaluation results.

The Quotation entity serves as the primary decision object for supplier selection and purchase award.

---

# Documents

This entity consists of:

- Quotation Entity
- Quotation Attributes
- Quotation Relationships
- Quotation Business Rules
- Quotation Lifecycle
- Quotation Odoo Mapping
- Quotation API

---

# Related Domains

Quotation integrates with:

- RFQ
- Supplier
- Manufacturer
- Product
- Customer
- Purchase Order
- Contract
- AI
- Engineering
- Procurement

---

# Primary Odoo Models

```
purchase.order

purchase.order.line
```

ETA extends these models with enterprise quotation comparison, technical evaluation, commercial scoring, AI recommendation, negotiation history, and supplier performance analytics.

---

# Long-Term Vision

The Quotation entity becomes the intelligent procurement evaluation layer of ETA, enabling transparent supplier comparison, AI-assisted award decisions, engineering validation, and enterprise purchasing governance.