---
document_id: ETA-ENT-PO-007
title: Purchase Order API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order API

## Purpose

The Purchase Order API provides standardized enterprise access to Purchase Orders throughout the ETA Procurement Ecosystem.

It supports Procurement, ERP, Logistics, Inventory, Finance, AI Services, Supplier Portal, and Executive Dashboards.

---

# Base Endpoint

```
/api/v1/purchase-orders
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /purchase-orders | List Purchase Orders |
| GET | /purchase-orders/{id} | Get Purchase Order |
| POST | /purchase-orders | Create Purchase Order |
| PUT | /purchase-orders/{id} | Replace Purchase Order |
| PATCH | /purchase-orders/{id} | Partial Update |
| DELETE | /purchase-orders/{id} | Soft Delete |
| POST | /purchase-orders/search | Enterprise Search |
| POST | /purchase-orders/{id}/approve | Approve Purchase Order |
| POST | /purchase-orders/{id}/send | Send to Supplier |
| POST | /purchase-orders/{id}/receive | Register Goods Receipt |
| POST | /purchase-orders/{id}/close | Close Purchase Order |
| GET | /purchase-orders/{id}/history | Revision History |

---

# Request Example

```json
{
  "quotationId":"UUID",
  "supplierId":"UUID",
  "currency":"EUR",
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
  "purchaseOrderId":"UUID",
  "purchaseOrderNumber":"PO-2026-000248",
  "status":"Approved",
  "supplier":"Flowserve GmbH",
  "grandTotal":25000
}
```

---

# Query Parameters

Supported Filters

- supplier
- status
- rfq
- quotation
- contract
- shipmentStatus
- paymentStatus
- warehouse

Pagination

```
?page=1&pageSize=50
```

Sorting

```
?sort=purchaseOrderNumber

?sort=-poDate
```

---

# Authentication

Supported Methods

- OAuth2
- JWT
- API Key
- Service Token

---

# Authorization

Supported Roles

- Procurement
- Engineering
- Logistics
- Warehouse
- Finance
- Executive
- Administrator
- Supplier Portal
- AI Agent

---

# Validation Rules

The API validates:

- Supplier exists
- Approved quotation exists
- Products exist
- Currency
- Quantities
- Pricing
- Business Rules
- Approval Status

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Purchase Order Not Found |
| 409 | Duplicate Purchase Order |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

The Purchase Order API publishes:

- PurchaseOrderCreated
- PurchaseOrderApproved
- PurchaseOrderSent
- PurchaseOrderAccepted
- GoodsReceived
- InventoryUpdated
- InvoiceLinked
- PaymentCompleted
- PurchaseOrderClosed

---

# AI Integration

The API exposes Purchase Order information for:

- Delivery Prediction
- Supplier Performance
- Procurement Monitoring
- Delay Detection
- Inventory Planning
- Cost Forecasting
- Executive Copilot
- Knowledge Graph

---

# Odoo Synchronization

Purchase Orders synchronize with:

- purchase.order
- purchase.order.line
- stock.picking
- stock.move
- account.move
- account.payment

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

The Purchase Order API becomes the enterprise procurement execution gateway of ETA, enabling secure API-first purchasing, logistics orchestration, inventory synchronization, financial integration, AI monitoring, and complete Source-to-Pay governance.