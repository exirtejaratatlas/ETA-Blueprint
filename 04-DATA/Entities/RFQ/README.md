---
document_id: ETA-ENT-RFQ-000
title: RFQ Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Entity

## Purpose

The Request for Quotation (RFQ) entity represents the initial procurement request within the ETA Enterprise Ecosystem.

It is the starting point of the sourcing lifecycle, connecting customer requirements with suppliers, manufacturers, quotations, purchase orders, engineering reviews, and AI-assisted procurement.

---

# Documents

This entity consists of:

- RFQ Entity
- RFQ Attributes
- RFQ Relationships
- RFQ Business Rules
- RFQ Lifecycle
- RFQ Odoo Mapping
- RFQ API

---

# Related Domains

RFQ integrates with:

- Customer
- Product
- Supplier
- Manufacturer
- Procurement
- Engineering
- Quotation
- Purchase Order
- Contract
- Project
- AI

---

# Primary Odoo Models

```
purchase.requisition
purchase.requisition.line
```

ETA extends these models with enterprise procurement workflow, technical evaluation, and AI capabilities.

---

# Long-Term Vision

The RFQ entity becomes the enterprise procurement gateway of ETA, orchestrating customer requests, engineering validation, supplier sourcing, quotation comparison, AI recommendations, and strategic purchasing through a unified procurement workflow.