---
document_id: ETA-ENT-PO-001
title: Purchase Order Entity
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order Entity

## Purpose

The Purchase Order (PO) entity represents the legally binding procurement document issued by ETA after quotation approval and supplier award.

It formalizes the commercial agreement between ETA and the supplier and initiates manufacturing, logistics, inventory, invoicing, and payment processes.

---

# Business Objectives

The Purchase Order enables ETA to:

- Issue procurement commitments
- Authorize supplier production
- Control procurement execution
- Track delivery commitments
- Synchronize ERP operations
- Trigger logistics workflow
- Trigger inventory planning
- Trigger invoice processing
- Support AI procurement monitoring

---

# Core Responsibilities

The Purchase Order manages:

- Supplier Commitment
- Ordered Products
- Quantities
- Commercial Terms
- Delivery Schedule
- Shipment Tracking
- Contract References
- Approval Workflow
- Financial Commitment
- Procurement Execution

---

# Entity Ownership

Business Owner

Procurement Department

Commercial Owner

Supply Chain Department

System Owner

ETA Platform

---

# Primary Identifier

Every Purchase Order owns one immutable:

Purchase Order ID

Example

```
PO-2026-000248
```

---

# Business Keys

Additional identifiers include:

- Purchase Order Number
- Supplier PO Reference
- RFQ Number
- Quotation Number
- Contract Number
- Procurement Reference

---

# Purchase Order Types

Supported PO types

- Standard Purchase Order
- Blanket Purchase Order
- Framework Purchase Order
- Emergency Purchase Order
- Service Purchase Order
- Capital Equipment Purchase Order
- Project Purchase Order

---

# Purchase Order Status

Supported lifecycle states

- Draft
- Pending Approval
- Approved
- Sent to Supplier
- Supplier Accepted
- Partially Delivered
- Fully Delivered
- Closed
- Cancelled
- Archived

---

# Enterprise Characteristics

Every Purchase Order supports:

- Multiple Product Lines
- Multiple Deliveries
- Partial Deliveries
- Multiple Shipments
- Multiple Invoices
- Multiple Payments
- Multiple Attachments
- Multi Currency
- Multi Warehouse

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

# Odoo Mapping

Primary Models

```
purchase.order

purchase.order.line
```

ETA extends Odoo Purchase Orders with enterprise approval workflow, AI monitoring, supplier performance analytics, shipment governance, and complete procurement traceability.

---

# AI Integration

AI uses Purchase Order information for:

- Delivery Prediction
- Supplier Performance
- Procurement Risk
- Cost Monitoring
- Shipment Monitoring
- Payment Forecasting
- Contract Compliance
- Procurement Copilot

---

# Long-Term Vision

The Purchase Order entity becomes the operational execution layer of ETA, connecting procurement decisions with supplier fulfillment, logistics, inventory, finance, ERP, and AI-driven operational intelligence.