---
document_id: ETA-ENT-PAY-003
title: Payment Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Payment Relationships

## Purpose

This document defines all enterprise relationships between the Payment entity and other domains inside the ETA Enterprise Procurement Ecosystem.

Payment is the enterprise settlement hub connecting procurement, treasury, banking, accounting, taxation, ERP, AI, and executive financial analytics.

---

# Enterprise Relationship Overview

```
Supplier

↓

Invoice

↓

Payment

├── Customer

├── Purchase Order

├── Contract

├── Bank Account

├── Accounting

├── Treasury

├── Documents

└── AI
```

---

# Supplier

Relationship

One Supplier

↓

Many Payments

Relationship Type

One-to-Many

Purpose

A supplier may receive multiple payments throughout different procurement cycles.

---

# Customer

Relationship

One Customer

↓

Many Receipts

Relationship Type

One-to-Many

Purpose

Customers may perform multiple payments or receipts.

---

# Invoice

Relationship

One Invoice

↓

Many Payments

Relationship Type

One-to-Many

Purpose

Invoices may be settled through one payment or multiple partial payments.

---

# Purchase Order

Relationship

One Purchase Order

↓

Many Payments

Relationship Type

Supporting Relationship

Purpose

Payments inherit procurement references through Purchase Orders.

---

# Contract

Relationship

One Contract

↓

Many Payments

Relationship Type

Supporting Relationship

Purpose

Contract payment milestones and commercial terms govern payment execution.

---

# Shipment

Relationship

One Shipment

↓

Supporting Payment Validation

Relationship Type

Supporting Relationship

Purpose

Shipment completion may be required before payment authorization.

---

# Bank Account

Relationship

One Bank Account

↓

Many Payments

Relationship Type

One-to-Many

Purpose

Payments are executed through treasury-managed bank accounts.

---

# Accounting

Relationship

One Payment

↓

One Journal Entry

Relationship Type

One-to-One

Purpose

Every completed payment creates accounting journal entries.

---

# Treasury

Relationship

One Treasury Account

↓

Many Payments

Relationship Type

One-to-Many

Purpose

Treasury manages liquidity, prioritization, and payment execution.

---

# Documents

Relationship

One Payment

↓

Many Documents

Relationship Type

One-to-Many

Examples

- Payment Voucher
- Bank Receipt
- SWIFT Copy
- LC Documents
- TT Confirmation
- Cheque Scan
- Guarantee
- Treasury Approval

---

# AI

AI consumes payment information for:

- Cash Flow Forecasting
- Liquidity Planning
- Fraud Detection
- Treasury Optimization
- Currency Risk
- Payment Prioritization
- Executive Copilot

---

# Analytics

Payment contributes to:

- Cash Flow Dashboard
- Treasury Dashboard
- AP Aging
- AR Aging
- Payment Performance
- Liquidity Forecast
- Financial Statements

---

# Enterprise Relationship Summary

| Related Entity | Cardinality |
|----------------|-------------|
| Supplier | One-to-Many |
| Customer | One-to-Many |
| Invoice | One-to-Many |
| Purchase Order | Supporting |
| Contract | Supporting |
| Shipment | Supporting |
| Bank Account | One-to-Many |
| Accounting | One-to-One |
| Treasury | One-to-Many |
| Documents | One-to-Many |

---

# Long-Term Vision

The Payment entity serves as the enterprise financial settlement layer of ETA by connecting procurement, treasury, banking, accounting, ERP, AI, and executive financial management into a fully governed payment ecosystem with complete end-to-end financial traceability.