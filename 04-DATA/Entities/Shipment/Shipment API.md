---
document_id: ETA-ENT-SHP-007
title: Shipment API
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment API

## Purpose

The Shipment API provides standardized enterprise access to shipment and logistics operations across the ETA Enterprise Procurement Ecosystem.

It supports Procurement, Logistics, Warehouse, Finance, ERP, AI Services, Executive Dashboards, and external logistics integrations.

---

# Base Endpoint

```
/api/v1/shipments
```

---

# Supported Operations

| Method | Endpoint | Description |
|---------|----------|-------------|
| GET | /shipments | List shipments |
| GET | /shipments/{id} | Get shipment |
| POST | /shipments | Create shipment |
| PUT | /shipments/{id} | Replace shipment |
| PATCH | /shipments/{id} | Partial update |
| DELETE | /shipments/{id} | Soft delete |
| POST | /shipments/search | Enterprise search |
| POST | /shipments/{id}/dispatch | Dispatch shipment |
| POST | /shipments/{id}/tracking | Add tracking event |
| POST | /shipments/{id}/arrive | Confirm arrival |
| POST | /shipments/{id}/receive | Warehouse receiving |
| POST | /shipments/{id}/complete | Complete shipment |
| GET | /shipments/{id}/history | Shipment history |

---

# Request Example

```json
{
  "purchaseOrderId":"UUID",
  "supplierId":"UUID",
  "transportMode":"Sea",
  "carrier":"Maersk",
  "estimatedArrival":"2026-08-20T10:00:00Z"
}
```

---

# Response Example

```json
{
  "shipmentId":"UUID",
  "shipmentNumber":"SHP-2026-000145",
  "status":"In Transit",
  "trackingNumber":"MSKU123456789",
  "eta":"2026-08-20T10:00:00Z"
}
```

---

# Query Parameters

Supported filters

- supplier
- carrier
- purchaseOrder
- shipmentType
- transportMode
- status
- warehouse
- destinationCountry

Pagination

```
?page=1&pageSize=50
```

Sorting

```
?sort=shipmentNumber

?sort=-estimatedArrival
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

- Logistics
- Warehouse
- Procurement
- Finance
- Executive
- Administrator
- AI Agent

---

# Validation Rules

The API validates:

- Shipment Number uniqueness
- Purchase Order existence
- Supplier validity
- Transport Mode
- Carrier information
- Warehouse
- Business Rules

---

# Error Codes

| Code | Meaning |
|------|---------|
| 400 | Validation Error |
| 401 | Unauthorized |
| 403 | Forbidden |
| 404 | Shipment Not Found |
| 409 | Duplicate Shipment |
| 422 | Business Rule Violation |
| 500 | Internal Server Error |

---

# Events

The Shipment API publishes:

- ShipmentCreated
- ShipmentBooked
- ShipmentDispatched
- ShipmentTrackingUpdated
- ShipmentArrived
- ShipmentReceived
- ShipmentCompleted
- ShipmentClosed
- ShipmentArchived

---

# AI Integration

The API exposes shipment information for:

- ETA Prediction
- Delay Detection
- Route Optimization
- Carrier Performance
- Customs Risk Analysis
- Logistics KPI
- Executive Copilot
- Knowledge Graph

---

# Odoo Synchronization

Shipments synchronize with:

- stock.picking
- stock.move
- stock.move.line
- delivery.carrier
- stock.warehouse

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

The Shipment API becomes the enterprise logistics gateway of ETA, enabling secure API-first shipment lifecycle management, transportation orchestration, warehouse synchronization, customs monitoring, AI-powered logistics intelligence, and complete operational traceability.