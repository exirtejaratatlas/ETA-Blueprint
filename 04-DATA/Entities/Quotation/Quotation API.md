---
document_id: ETA-ENT-QTN-007
title: Quotation API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation API

## Purpose

The Quotation API provides standardized enterprise access to supplier quotations across the ETA Procurement Ecosystem.

It supports Procurement, Engineering, AI Services, Supplier Portal, ERP Integration, Executive Dashboards, and external enterprise systems.

---

# Base Endpoint

```
/api/v1/quotations
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /quotations | List quotations |
| GET | /quotations/{id} | Get quotation |
| POST | /quotations | Create quotation |
| PUT | /quotations/{id} | Replace quotation |
| PATCH | /quotations/{id} | Partial update |
| DELETE | /quotations/{id} | Soft delete |
| POST | /quotations/search | Enterprise search |
| POST | /quotations/{id}/submit | Submit quotation |
| POST | /quotations/{id}/evaluate | Evaluate quotation |
| POST | /quotations/{id}/award | Award quotation |
| POST | /quotations/{id}/negotiate | Start negotiation |
| GET | /quotations/{id}/history | Revision history |

---

# Request Example

```json
{
  "rfqId":"UUID",
  "supplierId":"UUID",
  "currency":"EUR",
  "validUntil":"2026-09-01",
  "products":[
    {
      "productId":"UUID",
      "quantity":2,
      "unitPrice":12500
    }
  ]
}
```

---

# Response Example

```json
{
  "quotationId":"UUID",
  "quotationNumber":"QTN-2026-000487",
  "status":"Submitted",
  "supplier":"Flowserve GmbH",
  "totalPrice":25000
}
```

---

# Query Parameters

Supported filters

- supplier
- rfq
- status
- currency
- manufacturer
- evaluationStatus
- awardStatus

Pagination

```
?page=1&pageSize=50
```

Sorting

```
?sort=quotationNumber

?sort=-submissionDate
```

---

# Authentication

Supported methods

- OAuth2
- JWT
- API Key
- Service Token

---

# Authorization

Supported Roles

- Procurement
- Engineering
- Commercial
- Compliance
- Finance
- Executive
- Administrator
- Supplier Portal
- AI Agent

---

# Validation Rules

The API validates:

- RFQ exists
- Supplier exists
- Submission deadline
- Currency
- Product lines
- Unit prices
- Required attachments
- Business rule compliance

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Quotation Not Found |
| 409 | Duplicate Quotation |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

The Quotation API publishes:

- QuotationCreated
- QuotationSubmitted
- QuotationUpdated
- QuotationEvaluated
- NegotiationStarted
- QuotationAwarded
- QuotationRejected
- QuotationClosed

---

# AI Integration

The API exposes quotation data for:

- Supplier Ranking
- Price Benchmarking
- Technical Comparison
- Cost Estimation
- Lead Time Prediction
- Procurement Copilot
- Award Recommendation
- Knowledge Graph

---

# Odoo Synchronization

Quotation synchronizes with:

- purchase.order
- purchase.order.line
- purchase.requisition
- documents.document

Synchronization is asynchronous, event-driven, and fully audit logged.

---

# Versioning

Current Version

```
v1
```

Future Versions

```
v2

v3
```

Backward compatibility shall always be preserved.

---

# Long-Term Vision

The Quotation API becomes the enterprise supplier evaluation gateway of ETA, enabling secure API-first quotation management, engineering validation, AI-assisted procurement, supplier collaboration, and ERP synchronization.