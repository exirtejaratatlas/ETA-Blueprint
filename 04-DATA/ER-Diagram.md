---
document_id: ETA-DATA-016
title: ER Diagram
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
website: https://exiratlas.com
classification: Internal
last_updated: 2026
---

# ETA Enterprise Entity Relationship Model

## Purpose

This document defines the conceptual Entity Relationship Model (ERM) for the ETA Enterprise Procurement Ecosystem.

It serves as the foundation for PostgreSQL database design, API contracts, ERP integration, CRM integration, AI memory synchronization and analytics.

---

# Design Principles

- Domain Driven Design
- Normalized Database
- UUID Everywhere
- Multi-Tenant
- AI Ready
- Event Ready
- Audit Ready
- Enterprise Scale

---

# Core Domains

## Organization

Entities

Company

BusinessUnit

Department

Employee

Role

Office

---

Relationships

Company

1 → N BusinessUnit

BusinessUnit

1 → N Department

Department

1 → N Employee

Employee

N → N Role

---

# CRM

Entities

Customer

Contact

Opportunity

Lead

Activity

Project

Contract

---

Relationships

Customer

1 → N Contact

Customer

1 → N Opportunity

Opportunity

1 → N Activity

Opportunity

0..1 → Project

Project

1 → N Contract

---

# Supplier Management

Entities

Supplier

Manufacturer

Brand

Certificate

Evaluation

Country

---

Relationships

Manufacturer

1 → N Brand

Supplier

N → N Brand

Supplier

1 → N Evaluation

Supplier

N → N Certificate

Country

1 → N Supplier

---

# Product Management

Entities

Product

Category

Material

Specification

Equipment

Alternative

---

Relationships

Category

1 → N Product

Product

N → N Material

Product

N → N Specification

Equipment

N → N Product

Product

N → N Alternative

---

# Engineering

Entities

Datasheet

Drawing

Revision

Standard

MaterialGrade

Inspection

---

Relationships

Product

1 → N Datasheet

Product

1 → N Drawing

Drawing

1 → N Revision

Specification

N → N Standard

Inspection

N → N Equipment

---

# Procurement

Entities

RFQ

Quotation

PurchaseOrder

Shipment

Invoice

VendorEvaluation

Payment

---

Relationships

Opportunity

1 → N RFQ

RFQ

1 → N Quotation

Quotation

0..1 → PurchaseOrder

PurchaseOrder

1 → N Shipment

Shipment

1 → N Invoice

Invoice

0..N Payment

PurchaseOrder

1 → N VendorEvaluation

---

# Logistics

Entities

Warehouse

Location

Inventory

Batch

SerialNumber

---

Relationships

Warehouse

1 → N Location

Location

1 → N Inventory

Inventory

1 → N Batch

Batch

1 → N SerialNumber

---

# Finance

Entities

Currency

ExchangeRate

CostCenter

Bank

Transaction

---

Relationships

Currency

1 → N ExchangeRate

Invoice

N → 1 Currency

Payment

N → 1 Bank

Transaction

N → 1 CostCenter

---

# Documents

Entities

Document

Attachment

Approval

Version

Tag

---

Relationships

Document

1 → N Version

Document

1 → N Attachment

Document

N → N Tag

Document

1 → N Approval

---

# AI

Entities

Agent

Prompt

Memory

Embedding

KnowledgeNode

Conversation

Decision

Workflow

---

Relationships

Agent

1 → N Conversation

Conversation

1 → N Memory

Memory

1 → N Embedding

KnowledgeNode

N → N Memory

Agent

N → N Workflow

Decision

N → N KnowledgeNode

---

# Security

Entities

User

Permission

Role

AuditLog

APIKey

Secret

---

Relationships

User

N → N Role

Role

N → N Permission

User

1 → N AuditLog

User

1 → N APIKey

---

# Universal Audit

Every business entity contains

id

tenantId

createdAt

updatedAt

createdBy

updatedBy

version

status

isActive

deletedAt

---

# High-Level Relationships

Customer

↓

Opportunity

↓

RFQ

↓

Quotation

↓

Purchase Order

↓

Shipment

↓

Invoice

↓

Payment

Supplier

↓

Quotation

↓

Purchase Order

↓

Vendor Evaluation

Product

↓

Specification

↓

Datasheet

↓

Drawing

↓

Revision

KnowledgeNode

↓

Embedding

↓

Memory

↓

AI Agent

---

# Database Strategy

Database

PostgreSQL

Primary Keys

UUID

Soft Delete

Yes

Versioning

Yes

Audit

Mandatory

Multi-Tenant

Yes

---

# Future Extensions

Future entities

Risk

Compliance

Tender

BOM

Digital Twin

IoT Device

Predictive Maintenance

Supply Chain Graph

Workflow Engine

Marketplace

---

# Long-Term Vision

The ETA Enterprise Entity Relationship Model provides the canonical enterprise data structure connecting every customer, supplier, manufacturer, engineering document, procurement process, financial transaction, AI memory and organizational asset into one unified enterprise data platform for Exir Tejarat Atlas.