---
document_id: ETA-ENT-SUPPLIER-007
title: Supplier API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier API

## Purpose

This document defines the REST API specification for Supplier management across the ETA Enterprise Ecosystem.

The Supplier API provides standardized access to supplier master data, procurement information, compliance records, AI insights, and enterprise integrations.

---

# Base Endpoint

```
/api/v1/suppliers
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /suppliers | List Suppliers |
| GET | /suppliers/{id} | Get Supplier |
| POST | /suppliers | Create Supplier |
| PUT | /suppliers/{id} | Update Supplier |
| PATCH | /suppliers/{id} | Partial Update |
| DELETE | /suppliers/{id} | Soft Delete |
| POST | /suppliers/search | Enterprise Search |
| GET | /suppliers/{id}/products | Supplier Products |
| GET | /suppliers/{id}/contracts | Supplier Contracts |
| GET | /suppliers/{id}/purchase-orders | Purchase Orders |

---

# Request Example

```json
{
  "supplierCode": "SUP-000125",
  "companyName": "Flowserve Corporation",
  "supplierType": "Manufacturer",
  "country": "United States",
  "email": "sales@flowserve.com",
  "website": "https://www.flowserve.com"
}
```

---

# Response Example

```json
{
  "supplierId": "UUID",
  "supplierCode": "SUP-000125",
  "companyName": "Flowserve Corporation",
  "status": "Active",
  "createdDate": "2026-07-16T10:00:00Z"
}
```

---

# Query Parameters

Supported filters

- supplierType
- status
- country
- industry
- preferredSupplier
- strategicSupplier
- complianceStatus

Pagination

```
?page=1

&pageSize=50
```

Sorting

```
?sort=companyName

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

- Procurement User
- Procurement Manager
- Commercial
- Finance
- Executive
- Administrator
- AI Agent

---

# Validation Rules

The API validates

- Required Fields
- Unique Supplier Code
- Duplicate Legal Name
- Country Validation
- Email Format
- Compliance Status
- Lifecycle Transitions

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Supplier Not Found |
| 409 | Duplicate Supplier |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

Supplier API publishes

- SupplierCreated
- SupplierUpdated
- SupplierApproved
- SupplierActivated
- SupplierSuspended
- SupplierArchived

---

# AI Integration

Supplier APIs expose data to AI services for

- Supplier Recommendation
- Risk Assessment
- Procurement Copilot
- Vendor Ranking
- Lead Time Prediction
- Price Benchmarking
- Knowledge Graph

---

# Odoo Synchronization

Supplier synchronizes with

- res.partner
- purchase.order
- product.supplierinfo
- account.move
- stock.picking

Synchronization is asynchronous and event-driven.

---

# Versioning

Current Version

```
v1
```

Future versions

```
v2

v3
```

Backward compatibility must be maintained.

---

# Long-Term Vision

The Supplier API becomes the enterprise procurement interface, providing secure, scalable, API-first access to supplier information across ERP, procurement, AI services, external integrations, and enterprise analytics.