---
document_id: ETA-ENT-INVC-000
title: Invoice Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Invoice Entity

## Purpose

The Invoice entity represents all financial billing documents exchanged between ETA, suppliers, customers, logistics providers, and financial systems.

It governs invoice validation, three-way matching, tax compliance, accounting integration, payment preparation, and AI-assisted financial analysis.

Invoice is the financial bridge between procurement execution and payment processing.

---

# Documents

This entity consists of:

- Invoice Entity
- Invoice Attributes
- Invoice Relationships
- Invoice Business Rules
- Invoice Lifecycle
- Invoice Odoo Mapping
- Invoice API

---

# Related Domains

Invoice integrates with:

- Supplier
- Customer
- Product
- Purchase Order
- Contract
- Shipment
- Inventory
- Payment
- Accounting
- Documents
- AI

---

# Primary Odoo Models

```
account.move

account.move.line

account.payment

account.tax
```

ETA extends Odoo Accounting with enterprise invoice governance, AI financial validation, intelligent matching, procurement synchronization, and executive financial analytics.

---

# Enterprise Role

The Invoice acts as:

- Financial Document
- Supplier Billing Record
- Customer Billing Record
- Tax Document
- Accounting Source
- Payment Trigger
- Cost Allocation Source
- Financial Audit Record

---

# Invoice Types

Supported invoice categories include:

- Supplier Invoice
- Customer Invoice
- Proforma Invoice
- Commercial Invoice
- Tax Invoice
- Credit Note
- Debit Note
- Advance Invoice
- Progress Invoice
- Final Invoice

---

# Long-Term Vision

The Invoice entity becomes the financial transaction backbone of ETA by integrating procurement, logistics, inventory, accounting, taxation, payment processing, ERP, AI, and complete enterprise financial traceability.