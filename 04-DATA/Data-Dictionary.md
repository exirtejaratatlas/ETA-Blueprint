---
document_id: ETA-DATA-004
title: Data Dictionary
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# ETA Data Dictionary

## Purpose

This document defines the standard attributes used across the ETA Enterprise Procurement Ecosystem.

The Data Dictionary ensures consistency between:

- PostgreSQL
- APIs
- AI Memory
- ERP
- CRM
- Analytics
- Integrations

---

# Naming Standards

Entity Names

PascalCase

Example

Customer

PurchaseOrder

Supplier

---

Field Names

camelCase

Example

createdAt

supplierId

purchaseOrderNumber

---

Identifiers

UUID

Example

550e8400-e29b-41d4-a716-446655440000

---

# Common Base Fields

Every entity includes the following standard fields.

| Field | Type | Description |
|--------|------|-------------|
| id | UUID | Primary identifier |
| tenantId | UUID | Tenant identifier |
| createdAt | DateTime | Creation timestamp |
| updatedAt | DateTime | Last update timestamp |
| createdBy | UUID | Creator |
| updatedBy | UUID | Last modifier |
| version | Integer | Record version |
| status | Enum | Business status |
| isActive | Boolean | Active flag |
| deletedAt | DateTime | Soft delete timestamp |

---

# Customer

| Field | Type |
|--------|------|
| customerCode | String |
| legalName | String |
| tradeName | String |
| nationalId | String |
| taxId | String |
| website | URL |
| email | Email |
| phone | String |
| country | String |
| city | String |

---

# Supplier

| Field | Type |
|--------|------|
| supplierCode | String |
| legalName | String |
| qualificationLevel | Enum |
| paymentTerms | String |
| incoterms | String |
| preferredCurrency | String |
| country | String |

---

# Manufacturer

| Field | Type |
|--------|------|
| manufacturerCode | String |
| companyName | String |
| country | String |
| website | URL |
| status | Enum |

---

# Product

| Field | Type |
|--------|------|
| productCode | String |
| productName | String |
| categoryId | UUID |
| manufacturerId | UUID |
| brandId | UUID |
| lifecycleStatus | Enum |
| revision | String |

---

# Material

| Field | Type |
|--------|------|
| materialCode | String |
| description | String |
| standard | String |
| grade | String |
| unit | String |

---

# Equipment

| Field | Type |
|--------|------|
| equipmentCode | String |
| tagNumber | String |
| model | String |
| serialNumber | String |
| manufacturerId | UUID |

---

# RFQ

| Field | Type |
|--------|------|
| rfqNumber | String |
| customerId | UUID |
| issueDate | Date |
| dueDate | Date |
| ownerId | UUID |
| priority | Enum |

---

# Quotation

| Field | Type |
|--------|------|
| quotationNumber | String |
| supplierId | UUID |
| rfqId | UUID |
| currency | String |
| validityDate | Date |

---

# Purchase Order

| Field | Type |
|--------|------|
| poNumber | String |
| supplierId | UUID |
| contractId | UUID |
| currency | String |
| paymentTerms | String |
| deliveryTerms | String |

---

# Contract

| Field | Type |
|--------|------|
| contractNumber | String |
| customerId | UUID |
| supplierId | UUID |
| effectiveDate | Date |
| expirationDate | Date |

---

# Document

| Field | Type |
|--------|------|
| documentNumber | String |
| documentType | Enum |
| fileName | String |
| fileSize | Integer |
| storageLocation | String |
| checksum | String |

---

# AI Agent

| Field | Type |
|--------|------|
| agentCode | String |
| agentName | String |
| provider | String |
| model | String |
| contextWindow | Integer |
| temperature | Decimal |

---

# Prompt

| Field | Type |
|--------|------|
| promptCode | String |
| promptName | String |
| version | String |
| owner | String |
| status | Enum |

---

# Memory

| Field | Type |
|--------|------|
| memoryType | Enum |
| source | String |
| embeddingId | UUID |
| confidence | Decimal |

---

# Embedding

| Field | Type |
|--------|------|
| vectorId | UUID |
| model | String |
| dimensions | Integer |
| sourceDocument | UUID |

---

# Audit Log

| Field | Type |
|--------|------|
| eventType | String |
| entityType | String |
| entityId | UUID |
| userId | UUID |
| timestamp | DateTime |
| ipAddress | String |

---

# Standard Enumerations

Status

- Draft
- Active
- Pending
- Approved
- Rejected
- Archived
- Deleted

Priority

- Low
- Medium
- High
- Critical

Approval

- Pending
- Approved
- Rejected

---

# Long-Term Vision

The ETA Data Dictionary provides a standardized enterprise vocabulary for databases, APIs, AI services, integrations, analytics, and business applications, ensuring consistency across the entire Exir Tejarat Atlas technology ecosystem.