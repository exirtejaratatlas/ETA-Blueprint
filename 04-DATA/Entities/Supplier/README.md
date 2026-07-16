---
document_id: ETA-ENT-SUPPLIER-000
title: Supplier Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier Entity

## Purpose

The Supplier entity represents every organization that provides products, materials, equipment, engineering services, logistics services, manufacturing capabilities, or commercial support to ETA.

Supplier is one of the core Master Data entities of the ETA Enterprise Ecosystem.

It is the primary source for procurement, RFQs, quotations, purchase orders, contracts, logistics, quality evaluation, and supplier performance management.

---

# Documents

This entity consists of:

- Supplier Entity
- Supplier Attributes
- Supplier Relationships
- Supplier Business Rules
- Supplier Lifecycle
- Supplier Odoo Mapping
- Supplier API

---

# Related Domains

Supplier interacts with:

- Procurement
- RFQ
- Quotation
- Purchase Order
- Contract
- Product
- Inventory
- Logistics
- Finance
- AI

---

# Primary Odoo Model

```
res.partner
```

Supplier records extend the native Odoo Partner model using ETA enterprise extensions.

---

# Long-Term Vision

Supplier becomes the enterprise procurement master, enabling intelligent sourcing, supplier evaluation, AI-assisted purchasing, risk management, and complete supplier lifecycle governance.