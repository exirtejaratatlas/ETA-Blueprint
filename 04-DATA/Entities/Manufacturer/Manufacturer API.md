---
document_id: ETA-ENT-MANUFACTURER-007
title: Manufacturer API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer API

## Purpose

This document defines the REST API specification for Manufacturer management across the ETA Enterprise Ecosystem.

The Manufacturer API provides standardized access to OEM master data, engineering capabilities, certifications, manufacturing facilities, AI insights, and enterprise integrations.

---

# Base Endpoint

```
/api/v1/manufacturers
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /manufacturers | List Manufacturers |
| GET | /manufacturers/{id} | Get Manufacturer |
| POST | /manufacturers | Create Manufacturer |
| PUT | /manufacturers/{id} | Update Manufacturer |
| PATCH | /manufacturers/{id} | Partial Update |
| DELETE | /manufacturers/{id} | Soft Delete |
| POST | /manufacturers/search | Enterprise Search |
| GET | /manufacturers/{id}/products | Manufacturer Products |
| GET | /manufacturers/{id}/suppliers | Related Suppliers |
| GET | /manufacturers/{id}/documents | Engineering Documents |

---

# Request Example

```json
{
  "manufacturerCode": "MFG-000078",
  "companyName": "Flowserve Corporation",
  "manufacturerType": "OEM",
  "country": "United States",
  "website": "https://www.flowserve.com",
  "engineeringCapability": true
}
```

---

# Response Example

```json
{
  "manufacturerId": "UUID",
  "manufacturerCode": "MFG-000078",
  "companyName": "Flowserve Corporation",
  "status": "Active",
  "createdDate": "2026-07-16T10:00:00Z"
}
```

---

# Query Parameters

Supported filters

- manufacturerType
- status
- country
- productCategory
- preferredManufacturer
- strategicManufacturer
- complianceStatus

Pagination

```
?page=1&pageSize=50
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

- Engineering
- Procurement
- Commercial
- Finance
- Executive
- Administrator
- AI Agent

---

# Validation Rules

The API validates:

- Required Fields
- Unique Manufacturer Code
- Duplicate Legal Name
- Country Validation
- Engineering Capability
- Compliance Status
- Lifecycle Transitions

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Manufacturer Not Found |
| 409 | Duplicate Manufacturer |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

Manufacturer API publishes

- ManufacturerCreated
- ManufacturerUpdated
- ManufacturerApproved
- ManufacturerActivated
- ManufacturerSuspended
- ManufacturerArchived

---

# AI Integration

Manufacturer APIs expose data for

- OEM Recommendation
- Capability Analysis
- Product Matching
- Engineering Copilot
- Alternative Manufacturer Discovery
- Risk Assessment
- Knowledge Graph

---

# Odoo Synchronization

Manufacturer synchronizes with

- res.partner
- product.template
- product.product
- mrp.bom
- documents.document
- purchase.order

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

Backward compatibility must always be maintained.

---

# Long-Term Vision

The Manufacturer API becomes the enterprise OEM gateway, providing secure, scalable, API-first access to global manufacturer intelligence, engineering knowledge, AI services, ERP integrations, and procurement workflows throughout the ETA ecosystem.