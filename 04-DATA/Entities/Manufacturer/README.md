---
document_id: ETA-ENT-MANUFACTURER-000
title: Manufacturer Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer Entity

## Purpose

The Manufacturer entity represents every Original Equipment Manufacturer (OEM), factory, industrial producer, or fabrication facility that manufactures products supplied through the ETA Enterprise Ecosystem.

Manufacturers are independent master data entities and may supply products directly or through one or more suppliers and distributors.

---

# Documents

This entity consists of:

- Manufacturer Entity
- Manufacturer Attributes
- Manufacturer Relationships
- Manufacturer Business Rules
- Manufacturer Lifecycle
- Manufacturer Odoo Mapping
- Manufacturer API

---

# Related Domains

Manufacturer interacts with:

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

# Primary Odoo Model

```
res.partner
```

Manufacturer records extend the Partner model with manufacturer-specific enterprise metadata.

---

# Long-Term Vision

Manufacturer becomes the enterprise manufacturing intelligence hub, enabling ETA to maintain complete visibility of OEM capabilities, production facilities, certifications, lead times, engineering strengths, and global manufacturing relationships.