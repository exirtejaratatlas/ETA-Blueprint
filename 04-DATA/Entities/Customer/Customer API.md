---
document_id: ETA-ENT-CUSTOMER-007
title: Customer API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Customer API

## Purpose

This document defines the standard REST API specification for the Customer entity within the ETA Enterprise Ecosystem.

The API is designed to support:

- ETA Platform
- Odoo ERP
- Supplier Portal
- Procurement Portal
- Mobile Applications
- AI Services
- External Integrations

---

# Base Endpoint

```
/api/v1/customers
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /customers | List Customers |
| GET | /customers/{id} | Get Customer |
| POST | /customers | Create Customer |
| PUT | /customers/{id} | Update Customer |
| PATCH | /customers/{id} | Partial Update |
| DELETE | /customers/{id} | Soft Delete |
| POST | /customers/search | Enterprise Search |
| GET | /customers/{id}/projects | Customer Projects |
| GET | /customers/{id}/contracts | Customer Contracts |
| GET | /customers/{id}/orders | Customer Orders |

---

# Request Example

```json
{
  "customerCode": "CUS-10025",
  "companyName": "ABC Petrochemical",
  "country": "Iran",
  "industry": "Petrochemical",
  "email": "info@abc.com",
  "phone": "+98xxxxxxxxxx"
}
```

---

# Response Example

```json
{
  "customerId": "UUID",
  "customerCode": "CUS-10025",
  "companyName": "ABC Petrochemical",
  "status": "Active",
  "createdDate": "2026-07-16T10:00:00Z"
}
```

---

# Query Parameters

Supported filters include:

- status
- country
- industry
- accountManager
- strategicAccount
- customerType

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

Supported authentication:

- OAuth2
- JWT
- API Key
- Service Token

---

# Authorization

RBAC roles

- Administrator
- Sales Manager
- Procurement Manager
- Finance
- Executive
- AI Agent

---

# Validation Rules

The API validates:

- Required Fields
- Duplicate Customer Code
- Duplicate Legal Name
- Country Validation
- Email Format
- Status Transition Rules

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Customer Not Found |
| 409 | Duplicate Customer |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

Customer API publishes:

- CustomerCreated
- CustomerUpdated
- CustomerActivated
- CustomerArchived
- CustomerDeleted
- CustomerMerged

---

# AI Integration

The Customer API exposes data to AI services for:

- Customer Summaries
- Risk Assessment
- Opportunity Scoring
- Semantic Search
- Knowledge Graph
- Recommendation Engine

---

# Odoo Synchronization

Customer APIs synchronize with:

- res.partner
- crm.lead
- sale.order
- account.move
- project.project

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

Backwards compatibility must be maintained.

---

# Long-Term Vision

The Customer API becomes the canonical enterprise interface for customer information, providing secure, scalable, API-first access across every ETA application, AI service, and external integration.