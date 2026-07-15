---
document_id: ETA-DATA-001
title: Enterprise Data Dictionary
version: 2.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---
# Enterprise Data Dictionary

## Purpose

The Enterprise Data Dictionary is the authoritative reference for every business entity, attribute, relationship, metadata standard, and governance rule across the ETA Enterprise Ecosystem.

It defines the common language used by business users, software developers, solution architects, AI agents, data engineers, ERP systems, APIs, analytics platforms, and external integrations.

Every database table, API contract, AI model, Odoo object, workflow, and report must comply with this document.

This document is the **Single Source of Truth (SSOT)** for enterprise data.

---

# Scope

The Enterprise Data Dictionary governs all structured business data within ETA, including:

- Customer Data
- Supplier Data
- Manufacturer Data
- Product Data
- Procurement Data
- RFQs
- Quotations
- Purchase Orders
- Sales Orders
- Contracts
- Projects
- Inventory
- Logistics
- Finance
- Documents
- AI Knowledge
- Analytics
- Identity & Security
- Workflow Metadata
- System Configuration

This document applies to:

- ETA Platform
- Odoo ERP
- CRM
- Procurement Portal
- Supplier Portal
- Manufacturer Portal
- Mobile Applications
- REST APIs
- AI Services
- Data Warehouse
- Business Intelligence
- Knowledge Graph

---

# Objectives

The Enterprise Data Dictionary exists to:

- Standardize enterprise terminology.
- Eliminate duplicate definitions.
- Improve data quality.
- Support enterprise integration.
- Enable AI reasoning.
- Improve reporting consistency.
- Reduce implementation ambiguity.
- Support scalable software architecture.
- Preserve enterprise knowledge.

---

# Enterprise Data Principles

ETA follows these enterprise data principles.

## Single Source of Truth

Every business entity has exactly one authoritative owner.

Duplicate master data is prohibited.

---

## Business First

Data structures reflect business concepts rather than software implementation.

The business model always drives the data model.

---

## API First

Every entity should be designed for API exposure.

Internal and external integrations must consume standardized data structures.

---

## AI Ready

Every entity must contain sufficient metadata for:

- Retrieval
- Semantic Search
- Knowledge Graph
- AI Reasoning
- Recommendations
- Analytics

---

## Odoo Native

Whenever practical, entities should align with Odoo Enterprise models.

ETA extends—not replaces—the ERP data model.

---

## Security by Design

Every entity supports:

- Ownership
- Auditability
- Access Control
- Version History
- Traceability

---

## Enterprise Scalability

Entities must support:

- Multi-company
- Multi-country
- Multi-currency
- Multi-language
- Multi-user

without structural redesign.

---

# Enterprise Naming Convention

## Documents

```
ETA-AREA-NUMBER
```

Examples

```
ETA-DATA-001
ETA-BLUEPRINT-003
ETA-AI-015
```

---

## Entities

Entity names use singular nouns.

Examples

- Customer
- Supplier
- Product
- Project
- Contract

Never:

- Customers
- Products
- Projects

---

## Database Tables

snake_case

Examples

```
customer
supplier
purchase_order
project_task
quotation
```

---

## API Endpoints

Plural resources

```
/customers
/suppliers
/projects
/contracts
```

---

## Primary Keys

Every entity has one immutable identifier.

Examples

```
Customer ID
Supplier ID
Project ID
Contract ID
```

IDs are never reused.

---

## Foreign Keys

Foreign Keys always reference the Primary Identifier.

Examples

```
Customer ID
Supplier ID
Project ID
```

Never duplicate business identifiers.

---

# Data Classification

ETA classifies enterprise information into four categories.

## Master Data

Stable business objects.

Examples

- Customer
- Supplier
- Manufacturer
- Product
- User
- Currency
- Country

---

## Transaction Data

Operational records.

Examples

- RFQ
- Quotation
- Purchase Order
- Invoice
- Payment
- Shipment

---

## Reference Data

Controlled lists used throughout the platform.

Examples

- Incoterms
- Payment Terms
- Units
- Countries
- Currencies
- Industries

---

## Analytical Data

Derived information.

Examples

- KPIs
- AI Scores
- Forecasts
- Dashboards
- Risk Ratings

---

# Data Ownership

Every entity has one business owner.

| Domain | Owner |
|---------|-------|
| Customer | CRM |
| Supplier | Procurement |
| Manufacturer | Procurement |
| Product | Engineering |
| Contract | Legal / Commercial |
| Project | Project Management |
| Inventory | Warehouse |
| Finance | Finance |
| User | Administration |
| AI Knowledge | AI Platform |

Ownership determines:

- Creation
- Modification
- Validation
- Governance

---

# Enterprise Metadata Standard

Every business entity must contain the following metadata.

## Mandatory Fields

- ID
- Created Date
- Created By
- Modified Date
- Modified By
- Status
- Company
- Version
- Active Flag

---

## Optional Metadata

- Source System
- External Identifier
- Import Batch
- AI Tags
- Search Keywords
- Classification
- Business Owner

---

# Document Governance

Changes to enterprise data definitions require:

1. Business approval
2. Architecture review
3. Documentation update
4. Git commit
5. Version increment

No implementation may precede documentation.

---

# Versioning Rules

Major Version

Structural changes.

Example

```
1.0 → 2.0
```

Minor Version

Business enhancements.

Example

```
2.0 → 2.1
```

Patch Version

Editorial corrections.

Example

```
2.1 → 2.1.1
```

---

# Enterprise Identifier Standards

Every enterprise entity must use globally unique identifiers.

Supported identifier types include:

- UUID
- Auto Increment ID
- Business Code
- External System ID

Each entity should maintain:

- Internal Identifier
- Business Identifier
- External Reference (optional)

Identifiers are immutable throughout the entity lifecycle.

---

# Standard Audit Fields

Every transactional entity must include:

- Created By
- Created Date
- Modified By
- Modified Date
- Approved By
- Approved Date
- Status
- Version
- Company
- Active Flag
- Deleted Flag (Soft Delete)
- Row Version (Concurrency Control)

Audit fields are mandatory for enterprise traceability.

---

# Data Quality Principles

ETA follows the following enterprise data quality dimensions:

- Accuracy
- Completeness
- Consistency
- Timeliness
- Uniqueness
- Validity
- Integrity
- Traceability

Every business entity should satisfy these dimensions before becoming Active.

---

# Enterprise Search Standards

Every searchable entity should expose:

- Search Title
- Search Keywords
- Search Tags
- AI Embeddings
- Full Text Index
- Business Classification

These fields support:

- Enterprise Search
- AI Retrieval
- Knowledge Graph
- RAG
- Semantic Search

---

# AI Data Principles

Enterprise data should be designed for AI consumption.

Each entity should support:

- AI Classification
- AI Embeddings
- AI Summary
- AI Relationships
- AI Confidence Score
- AI Recommendations

AI-generated information never replaces business data.

It augments enterprise knowledge while preserving the original source.

---
# Long-Term Vision

The Enterprise Data Dictionary serves as the foundation of every ETA system, ensuring that business knowledge, software architecture, enterprise integrations, analytics, and artificial intelligence all operate using one unified enterprise language.

# Master Data Standards

## Purpose

Master Data represents the core business entities that remain relatively stable over time and are shared across multiple domains within the ETA Enterprise Ecosystem.

Master Data serves as the foundation for all operational, analytical, and AI-driven processes.

All transactional records must reference Master Data entities rather than duplicating business information.

---

# Master Data Principles

Master Data must be:

- Unique
- Accurate
- Consistent
- Governed
- Version Controlled
- Searchable
- AI Ready
- Enterprise Shared

---

# Core Master Data Domains

ETA maintains the following enterprise master data domains:

- Customer
- Supplier
- Manufacturer
- Product
- Organization
- User
- Role
- Country
- Currency
- Unit of Measure
- Warehouse
- Cost Center
- Profit Center
- Payment Terms
- Incoterms
- Tax
- Document Type

---

# Customer Master Data

Purpose

Represents organizations purchasing products or services from ETA.

Primary Identifier

- Customer ID

Business Identifier

- Customer Code

Mandatory Attributes

- Legal Name
- Commercial Name
- Country
- Industry
- Tax Number
- Status

Owner Domain

CRM

Referenced By

- Opportunity
- Quotation
- Contract
- Project
- Invoice
- Payment

---

# Supplier Master Data

Purpose

Represents approved suppliers and distributors.

Primary Identifier

- Supplier ID

Business Identifier

- Supplier Code

Mandatory Attributes

- Legal Name
- Country
- Supplier Category
- Qualification Status
- Payment Terms

Owner Domain

Procurement

Referenced By

- RFQ
- Quotation
- Purchase Order
- Contract
- Shipment

---

# Manufacturer Master Data

Purpose

Represents Original Equipment Manufacturers (OEMs).

Primary Identifier

- Manufacturer ID

Business Identifier

- Manufacturer Code

Mandatory Attributes

- Legal Name
- Brand
- Country
- Certifications
- Product Categories

Referenced By

- Product
- Supplier
- Technical Documents

---

# Product Master Data

Purpose

Represents all products and services managed by ETA.

Primary Identifier

- Product ID

Business Identifier

- Product Code

Mandatory Attributes

- Product Name
- Category
- Unit of Measure
- Manufacturer
- Status

Referenced By

- RFQ
- Quotation
- Purchase Order
- Inventory
- Project

---

# Organization Master Data

Purpose

Represents legal entities operating within ETA.

Examples

- Exir Tejarat Atlas
- Allison General Trading LLC

Referenced By

All enterprise transactions.

---

# User Master Data

Purpose

Represents authenticated enterprise users.

Mandatory Attributes

- User ID
- Full Name
- Email
- Department
- Role
- Status

Referenced By

Every auditable business transaction.

---

# Country Master Data

Purpose

Standard list of countries.

Standard

ISO 3166

Referenced By

- Customer
- Supplier
- Manufacturer
- Shipment
- Organization

---

# Currency Master Data

Purpose

Standard list of supported currencies.

Examples

- IRR
- USD
- EUR
- AED
- CNY

Referenced By

All financial transactions.

---

# Unit of Measure

Purpose

Standard measurement units.

Examples

- PCS
- KG
- TON
- METER
- LITER
- SET

Referenced By

Products and Inventory.

---

# Warehouse Master Data

Purpose

Represents physical and virtual inventory locations.

Referenced By

- Inventory
- Procurement
- Logistics
- Projects

---

# Payment Terms

Examples

- Advance Payment
- Net 30
- Net 60
- LC
- CAD

Referenced By

Customers, Suppliers, Contracts, Invoices.

---

# Incoterms

Supported according to ICC standards.

Examples

- EXW
- FCA
- FOB
- CFR
- CIF
- CPT
- CIP
- DAP
- DPU
- DDP

---

# Tax Master Data

Purpose

Defines taxation rules.

Referenced By

Finance, Invoices, Contracts.

---

# Master Data Governance

Every master entity must have:

- Business Owner
- Steward
- Approval Workflow
- Change History
- Audit Trail

Only the owning domain may modify master data.

---

# AI Usage

Master Data powers:

- Semantic Search
- Knowledge Graph
- Recommendation Engine
- Supplier Matching
- Product Matching
- Customer Insights
- AI Copilot

Master Data is continuously enriched through AI while preserving the original authoritative record.

---

# Master Data Lifecycle

Every Master Data entity follows the same lifecycle:

1. Creation
2. Validation
3. Approval
4. Activation
5. Usage
6. Update
7. Versioning
8. Deactivation
9. Archive

Master Data is never physically deleted from the enterprise repository.

---

# Master Data Quality KPIs

The following KPIs are continuously monitored:

- Duplicate Rate
- Data Completeness
- Validation Success Rate
- Approval Time
- Master Data Accuracy
- AI Enrichment Coverage
- Searchability Score
- Reference Integrity

# Transaction Data Standards

## Purpose

Transaction Data represents all operational business activities performed within the ETA Enterprise Ecosystem.

Unlike Master Data, Transaction Data changes continuously and records the execution of business processes.

Transaction Data provides the operational history required for procurement, finance, logistics, analytics, compliance, and artificial intelligence.

---

# Transaction Data Principles

Every transaction must be:

- Traceable
- Auditable
- Immutable after approval
- Linked to Master Data
- Time-stamped
- Version Controlled
- AI Searchable
- Security Classified

---

# Core Transaction Domains

ETA manages the following enterprise transaction entities:

- Opportunity
- RFQ
- Quotation
- Sales Order
- Purchase Order
- Contract
- Project
- Invoice
- Payment
- Shipment
- Inventory Movement
- Approval
- Workflow Instance
- Audit Event
- AI Recommendation

---

# Opportunity

Purpose

Represents a commercial sales opportunity before procurement begins.

Owner

CRM

Lifecycle

Lead
→ Qualified
→ Proposal
→ Negotiation
→ Won / Lost

Referenced By

- Customer
- Quotation
- Contract
- Project

---

# Request For Quotation (RFQ)

Purpose

Represents customer procurement requests.

Mandatory Information

- RFQ Number
- Customer
- Project
- Products
- Required Delivery Date
- Technical Documents

Referenced By

- Quotation
- Supplier
- Procurement

---

# Quotation

Purpose

Represents supplier or customer commercial offers.

Mandatory Information

- Quote Number
- RFQ Reference
- Supplier
- Customer
- Currency
- Validity
- Commercial Terms

Referenced By

- Purchase Order
- Sales Order
- Contract

---

# Purchase Order

Purpose

Represents approved procurement orders.

Mandatory Information

- PO Number
- Supplier
- Contract
- Currency
- Payment Terms
- Delivery Terms

Status

Draft

Approved

Released

Closed

Cancelled

---

# Sales Order

Purpose

Represents approved customer sales.

Referenced By

- Customer
- Invoice
- Shipment

---

# Invoice

Purpose

Represents financial billing documents.

Referenced By

- Customer
- Supplier
- Payment
- Finance

---

# Payment

Purpose

Represents incoming and outgoing financial transactions.

Examples

- Customer Payment
- Supplier Payment
- Advance Payment
- Refund

---

# Shipment

Purpose

Represents logistics execution.

Contains

- Shipment Number
- Carrier
- Incoterm
- Origin
- Destination
- Tracking Number

---

# Inventory Movement

Purpose

Tracks stock movement.

Movement Types

- Receipt
- Issue
- Transfer
- Adjustment
- Return

---

# Approval

Purpose

Represents approval decisions across ETA.

Examples

- PO Approval
- Contract Approval
- Budget Approval
- Invoice Approval

---

# Workflow Instance

Purpose

Represents execution of enterprise workflows.

Examples

- RFQ Workflow
- Procurement Workflow
- Contract Workflow
- Finance Workflow

---

# Audit Event

Purpose

Records every critical business action.

Contains

- User
- Action
- Timestamp
- Entity
- Previous Value
- New Value

Audit Events cannot be modified.

---

# AI Recommendation

Purpose

Stores AI-generated recommendations.

Examples

- Recommended Supplier
- Risk Alert
- Technical Match
- Procurement Optimization
- Pricing Insight

AI recommendations never overwrite business transactions.

---

# Transaction Lifecycle

All transaction entities follow:

1. Draft
2. Validation
3. Review
4. Approval
5. Execution
6. Completion
7. Archive

Certain entities support:

- Rejection
- Cancellation
- Revision

---

# Transaction Integrity Rules

Every transaction:

- References valid Master Data.
- Has one unique Transaction ID.
- Contains complete audit history.
- Records timestamps.
- Maintains approval status.
- Cannot violate business rules.

---

# AI Usage

Transaction Data powers:

- Procurement Analytics
- AI Copilot
- Forecasting
- Supplier Recommendations
- Delivery Prediction
- Risk Detection
- Executive Reporting
- Knowledge Graph Updates

---

# Transaction KPIs

Examples include:

- RFQ Cycle Time
- Procurement Lead Time
- Quote Response Time
- PO Approval Time
- Invoice Processing Time
- Payment Delay
- Shipment Accuracy
- Workflow Completion Rate
- AI Recommendation Acceptance Rate

# Transaction Data Standards

## Purpose

Transaction Data represents all operational business activities performed within the ETA Enterprise Ecosystem.

Unlike Master Data, Transaction Data changes continuously and records the execution of business processes.

Transaction Data provides the operational history required for procurement, finance, logistics, analytics, compliance, and artificial intelligence.

---

# Transaction Data Principles

Every transaction must be:

- Traceable
- Auditable
- Immutable after approval
- Linked to Master Data
- Time-stamped
- Version Controlled
- AI Searchable
- Security Classified

---

# Core Transaction Domains

ETA manages the following enterprise transaction entities:

- Opportunity
- RFQ
- Quotation
- Sales Order
- Purchase Order
- Contract
- Project
- Invoice
- Payment
- Shipment
- Inventory Movement
- Approval
- Workflow Instance
- Audit Event
- AI Recommendation

---

# Opportunity

Purpose

Represents a commercial sales opportunity before procurement begins.

Owner

CRM

Lifecycle

Lead
→ Qualified
→ Proposal
→ Negotiation
→ Won / Lost

Referenced By

- Customer
- Quotation
- Contract
- Project

---

# Request For Quotation (RFQ)

Purpose

Represents customer procurement requests.

Mandatory Information

- RFQ Number
- Customer
- Project
- Products
- Required Delivery Date
- Technical Documents

Referenced By

- Quotation
- Supplier
- Procurement

---

# Quotation

Purpose

Represents supplier or customer commercial offers.

Mandatory Information

- Quote Number
- RFQ Reference
- Supplier
- Customer
- Currency
- Validity
- Commercial Terms

Referenced By

- Purchase Order
- Sales Order
- Contract

---

# Purchase Order

Purpose

Represents approved procurement orders.

Mandatory Information

- PO Number
- Supplier
- Contract
- Currency
- Payment Terms
- Delivery Terms

Status

Draft

Approved

Released

Closed

Cancelled

---

# Sales Order

Purpose

Represents approved customer sales.

Referenced By

- Customer
- Invoice
- Shipment

---

# Invoice

Purpose

Represents financial billing documents.

Referenced By

- Customer
- Supplier
- Payment
- Finance

---

# Payment

Purpose

Represents incoming and outgoing financial transactions.

Examples

- Customer Payment
- Supplier Payment
- Advance Payment
- Refund

---

# Shipment

Purpose

Represents logistics execution.

Contains

- Shipment Number
- Carrier
- Incoterm
- Origin
- Destination
- Tracking Number

---

# Inventory Movement

Purpose

Tracks stock movement.

Movement Types

- Receipt
- Issue
- Transfer
- Adjustment
- Return

---

# Approval

Purpose

Represents approval decisions across ETA.

Examples

- PO Approval
- Contract Approval
- Budget Approval
- Invoice Approval

---

# Workflow Instance

Purpose

Represents execution of enterprise workflows.

Examples

- RFQ Workflow
- Procurement Workflow
- Contract Workflow
- Finance Workflow

---

# Audit Event

Purpose

Records every critical business action.

Contains

- User
- Action
- Timestamp
- Entity
- Previous Value
- New Value

Audit Events cannot be modified.

---

# AI Recommendation

Purpose

Stores AI-generated recommendations.

Examples

- Recommended Supplier
- Risk Alert
- Technical Match
- Procurement Optimization
- Pricing Insight

AI recommendations never overwrite business transactions.

---

# Transaction Lifecycle

All transaction entities follow:

1. Draft
2. Validation
3. Review
4. Approval
5. Execution
6. Completion
7. Archive

Certain entities support:

- Rejection
- Cancellation
- Revision

---

# Transaction Integrity Rules

Every transaction:

- References valid Master Data.
- Has one unique Transaction ID.
- Contains complete audit history.
- Records timestamps.
- Maintains approval status.
- Cannot violate business rules.

---

# AI Usage

Transaction Data powers:

- Procurement Analytics
- AI Copilot
- Forecasting
- Supplier Recommendations
- Delivery Prediction
- Risk Detection
- Executive Reporting
- Knowledge Graph Updates

---

# Transaction KPIs

Examples include:

- RFQ Cycle Time
- Procurement Lead Time
- Quote Response Time
- PO Approval Time
- Invoice Processing Time
- Payment Delay
- Shipment Accuracy
- Workflow Completion Rate
- AI Recommendation Acceptance Rate