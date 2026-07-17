---
document_id: ETA-ENT-PO-000
title: Purchase Order Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order Entity

## Purpose

The Purchase Order (PO) entity represents the formal procurement commitment issued by ETA to a supplier after quotation evaluation and award.

It legally authorizes the supplier to manufacture, prepare, and deliver the requested goods or services under agreed commercial and technical conditions.

The Purchase Order is the execution layer of the procurement process.

---

# Documents

This entity consists of:

- Purchase Order Entity
- Purchase Order Attributes
- Purchase Order Relationships
- Purchase Order Business Rules
- Purchase Order Lifecycle
- Purchase Order Odoo Mapping
- Purchase Order API

---

# Related Domains

Purchase Orders integrate with:

- RFQ
- Quotation
- Supplier
- Manufacturer
- Product
- Contract
- Shipment
- Inventory
- Invoice
- Payment
- Documents
- AI

---

# Primary Odoo Models

```
purchase.order

purchase.order.line
```

ETA extends Odoo Purchase Orders with enterprise approval workflow, procurement governance, shipment tracking, AI monitoring, supplier performance, and full auditability.

---

# Enterprise Role

The Purchase Order acts as:

- Commercial Commitment
- Procurement Authorization
- ERP Purchasing Document
- Supplier Instruction
- Financial Commitment
- Inventory Trigger
- Shipment Trigger
- Invoice Trigger
- Payment Trigger

---

# Long-Term Vision

The Purchase Order entity serves as the operational execution engine of ETA, connecting procurement decisions with supplier execution, logistics, inventory, finance, and AI-driven enterprise monitoring while ensuring complete traceability across the Source-to-Pay lifecycle.