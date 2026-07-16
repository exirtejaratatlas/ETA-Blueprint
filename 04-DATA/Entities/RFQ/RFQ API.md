---
document_id: ETA-ENT-RFQ-007
title: RFQ API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ API

## Purpose

The RFQ API provides standardized enterprise access to Request for Quotation data across the ETA Enterprise Ecosystem.

It enables secure integration with ERP, CRM, Procurement, Engineering, AI Services, Supplier Portal, Mobile Applications, and external systems.

---

# Base Endpoint

```
/api/v1/rfqs
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /rfqs | List RFQs |
| GET | /rfqs/{id} | Get RFQ |
| POST | /rfqs | Create RFQ |
| PUT | /rfqs/{id} | Replace RFQ |
| PATCH | /rfqs/{id} | Partial Update |
| DELETE | /rfqs/{id} | Soft Delete |
| POST | /rfqs/search | Enterprise Search |
| POST | /rfqs/{id}/approve | Approve RFQ |
| POST | /rfqs/{id}/send | Send RFQ |
| GET | /rfqs/{id}/quotations | RFQ Quotations |
| GET | /rfqs/{id}/suppliers | Invited Suppliers |
| GET | /rfqs/{id}/documents | RFQ Documents |

---

# Request Example

```json
{
  "customerId": "UUID",
  "rfqTitle": "Cooling Water Pump",
  "rfqType": "Competitive",
  "priority": "High",
  "requiredDeliveryDate": "2026-09-01",
  "products": [
    {
      "productId": "UUID",
      "quantity": 2,
      "uom": "EA"
    }
  ]
}
```

---

# Response Example

```json
{
  "rfqId": "UUID",
  "rfqNumber": "RFQ-2026-000154",
  "status": "Draft",
  "createdDate": "2026-07-16T10:00:00Z"
}
```

---

# Query Parameters

Supported filters

- customer
- project
- status
- priority
- supplier
- procurementOwner
- rfqType

Pagination

```
?page=1&pageSize=50
```

Sorting

```
?sort=rfqNumber
?sort=-createdDate
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
- Compliance
- Commercial
- Finance
- Executive
- Administrator
- AI Agent

---

# Validation Rules

The API validates:

- Customer exists
- Product Lines exist
- Quantities are positive
- Required delivery date
- Procurement ownership
- Supplier eligibility
- Business rule compliance

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | RFQ Not Found |
| 409 | Duplicate RFQ |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

The RFQ API publishes:

- RFQCreated
- RFQUpdated
- RFQApproved
- RFQSent
- RFQCancelled
- RFQClosed
- RFQAwarded

---

# AI Integration

The RFQ API exposes data for:

- Supplier Recommendation
- Product Matching
- Manufacturer Recommendation
- Cost Estimation
- Lead Time Prediction
- Procurement Copilot
- Engineering Copilot
- Knowledge Graph

---

# Odoo Synchronization

RFQ synchronizes with:

- purchase.requisition
- purchase.requisition.line
- purchase.order
- purchase.order.line
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

Backward compatibility must always be preserved.

---

# Long-Term Vision

The RFQ API becomes the enterprise procurement gateway of ETA, providing API-first access to sourcing workflows, engineering validation, supplier collaboration, AI procurement services, and ERP integrations.