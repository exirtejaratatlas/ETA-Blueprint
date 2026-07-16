---
document_id: ETA-ENT-PRODUCT-007
title: Product API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product API

## Purpose

The Product API provides standardized, secure, and scalable access to Product master data across the ETA Enterprise Ecosystem.

It enables integration with ERP, CRM, Procurement, Inventory, AI Services, Mobile Applications, and external systems.

---

# Base Endpoint

```
/api/v1/products
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /products | List Products |
| GET | /products/{id} | Get Product |
| POST | /products | Create Product |
| PUT | /products/{id} | Replace Product |
| PATCH | /products/{id} | Partial Update |
| DELETE | /products/{id} | Soft Delete |
| POST | /products/search | Enterprise Search |
| GET | /products/{id}/suppliers | Product Suppliers |
| GET | /products/{id}/manufacturer | Product Manufacturer |
| GET | /products/{id}/documents | Product Documents |
| GET | /products/{id}/inventory | Inventory Status |

---

# Request Example

```json
{
  "productCode": "PRD-000125",
  "productName": "Centrifugal Pump",
  "category": "Pump",
  "manufacturerId": "UUID",
  "supplierId": "UUID",
  "uom": "EA",
  "active": true
}
```

---

# Response Example

```json
{
  "productId": "UUID",
  "productCode": "PRD-000125",
  "productName": "Centrifugal Pump",
  "status": "Active",
  "createdDate": "2026-07-16T10:00:00Z"
}
```

---

# Query Parameters

Supported filters

- category
- manufacturer
- supplier
- productType
- status
- strategicItem
- active

Pagination

```
?page=1&pageSize=50
```

Sorting

```
?sort=productName
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

- Engineering
- Procurement
- Warehouse
- Commercial
- Finance
- Executive
- Administrator
- AI Agent

---

# Validation Rules

The API validates:

- Required Fields
- Unique Product Code
- Product Category
- Manufacturer Reference
- Supplier Reference
- UOM Validation
- Lifecycle Status
- Business Rule Compliance

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Product Not Found |
| 409 | Duplicate Product |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

Product API publishes:

- ProductCreated
- ProductUpdated
- ProductApproved
- ProductActivated
- ProductRevised
- ProductObsolete
- ProductArchived

---

# AI Integration

The Product API exposes data for:

- Product Matching
- Alternative Products
- Technical Comparison
- Procurement Copilot
- Engineering Copilot
- Semantic Search
- Knowledge Graph
- AI Recommendations
- Demand Forecasting

---

# Odoo Synchronization

Product synchronizes with:

- product.template
- product.product
- product.category
- purchase.order.line
- stock.move
- stock.quant
- mrp.bom
- account.move.line

Synchronization is asynchronous and event-driven.

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

The Product API becomes the enterprise gateway for all product information, providing secure API-first access to engineering knowledge, procurement data, inventory status, AI intelligence, ERP integrations, and enterprise-wide product lifecycle management.