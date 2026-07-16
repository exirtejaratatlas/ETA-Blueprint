---
document_id: ETA-ENT-CUSTOMER-003
title: Customer Relationships
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Customer Relationships

## Purpose

This document defines every relationship between the Customer entity and the remaining entities inside the ETA Enterprise Ecosystem.

Customer acts as one of the central master entities of the platform.

---

# Relationship Principles

The Customer entity is never duplicated.

Every business transaction references exactly one Customer.

Relationships are enforced through immutable foreign keys.

---

# CRM

Relationship

Customer (1)

↓

Opportunity (N)

Meaning

One customer may have multiple opportunities.

---

Customer (1)

↓

Lead (N)

---

Customer (1)

↓

Activity (N)

---

# Sales

Customer (1)

↓

Quotation (N)

---

Customer (1)

↓

Sales Order (N)

---

Customer (1)

↓

Sales Invoice (N)

---

# Procurement

Customer (1)

↓

RFQ (N)

---

Customer (1)

↓

Purchase Request (N)

---

Customer (1)

↓

Purchase Order (N)

---

# Contract

Customer (1)

↓

Contract (N)

---

Customer (1)

↓

Contract Amendment (N)

---

# Project

Customer (1)

↓

Project (N)

---

Customer (1)

↓

Project Milestone (N)

---

Customer (1)

↓

Deliverable (N)

---

# Logistics

Customer (1)

↓

Shipment (N)

---

Customer (1)

↓

Delivery (N)

---

Customer (1)

↓

Export Document (N)

---

# Finance

Customer (1)

↓

Invoice (N)

---

Customer (1)

↓

Payment (N)

---

Customer (1)

↓

Credit Note (N)

---

Customer (1)

↓

Journal Entry (N)

---

# Support

Customer (1)

↓

Support Ticket (N)

---

Customer (1)

↓

Warranty (N)

---

# Documents

Customer (1)

↓

Document (N)

---

Customer (1)

↓

Drawing (N)

---

Customer (1)

↓

Certificate (N)

---

# AI

Customer (1)

↓

Knowledge Node (1)

---

Customer (1)

↓

Embedding (N)

---

Customer (1)

↓

Recommendation (N)

---

Customer (1)

↓

Risk Assessment (N)

---

# Security

Customer (1)

↓

Audit Log (N)

---

Customer (1)

↓

Approval Workflow (N)

---

# Enterprise Graph

Customer

↓

Supplier

↓

Manufacturer

↓

Product

↓

RFQ

↓

Quotation

↓

Purchase Order

↓

Contract

↓

Project

↓

Shipment

↓

Invoice

↓

Payment

Customer is the commercial root of the enterprise graph.

---

# Cardinality Summary

| Entity | Relationship |
|----------|-------------|
| Opportunity | 1:N |
| RFQ | 1:N |
| Quotation | 1:N |
| Purchase Order | 1:N |
| Contract | 1:N |
| Project | 1:N |
| Shipment | 1:N |
| Invoice | 1:N |
| Payment | 1:N |
| Document | 1:N |
| AI Knowledge | 1:1 |

---

# Business Rules

A Customer:

- must exist before Opportunities.
- must exist before Contracts.
- must exist before Projects.
- cannot be deleted if referenced.
- may become inactive.
- retains historical relationships forever.

---

# Long-Term Vision

Customer becomes the central commercial entity connecting every transaction, project, contract, financial record, AI model, and enterprise knowledge object across ETA.