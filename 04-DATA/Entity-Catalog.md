---
document_id: ETA-DATA-003
title: Entity Catalog
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# ETA Entity Catalog

## Purpose

This document defines the primary business entities used across the ETA Enterprise Procurement Ecosystem.

Each entity represents an important business concept and serves as the foundation for database design, APIs, AI memory, analytics, and integrations.

---

# Entity Standards

Each entity includes:

- Entity Code
- Domain
- Purpose
- Description
- Data Owner
- Related Entities

Entity identifiers use UUID.

---

# Organization Domain

## Organization

Code

ENT-ORG

Purpose

Represents the legal organization using ETA.

Data Owner

Executive Management

Related Entities

- Company
- User
- Department

---

## Company

Code

ENT-COM

Purpose

Represents a legal company within the organization.

Related

- Branch
- Department
- Employee

---

## Branch

Code

ENT-BRA

Purpose

Represents operational branches.

---

## Department

Code

ENT-DEP

Purpose

Represents organizational departments.

---

## Employee

Code

ENT-EMP

Purpose

Represents personnel working inside the organization.

---

# Identity Domain

## User

Code

ENT-USR

Purpose

Represents authenticated platform users.

Related

- Role
- Permission

---

## Role

Code

ENT-ROL

Purpose

Defines user responsibilities.

---

## Permission

Code

ENT-PER

Purpose

Defines access rights.

---

# CRM Domain

## Customer

Code

ENT-CUS

Purpose

Represents customers purchasing products or services.

Related

- Contact
- Opportunity

---

## Contact

Code

ENT-CON

Purpose

Represents customer contacts.

---

## Lead

Code

ENT-LED

Purpose

Represents potential customers.

---

## Opportunity

Code

ENT-OPP

Purpose

Represents sales opportunities.

---

## Activity

Code

ENT-ACT

Purpose

Represents meetings, calls, emails and follow-ups.

---

# Procurement Domain

## RFQ

Code

ENT-RFQ

Purpose

Represents Requests for Quotation.

Related

- Supplier
- Product
- Quotation

---

## Supplier

Code

ENT-SUP

Purpose

Represents approved suppliers.

---

## Manufacturer

Code

ENT-MFG

Purpose

Represents original equipment manufacturers.

---

## Quotation

Code

ENT-QUO

Purpose

Represents supplier quotations.

---

## Purchase Order

Code

ENT-PO

Purpose

Represents purchase commitments.

---

## Contract

Code

ENT-CTR

Purpose

Represents procurement contracts.

---

# Product Domain

## Product

Code

ENT-PRD

Purpose

Represents commercial products.

---

## Material

Code

ENT-MAT

Purpose

Represents raw or processed materials.

---

## Product Category

Code

ENT-CAT

Purpose

Groups products into categories.

---

## Brand

Code

ENT-BRD

Purpose

Represents commercial brands.

---

## Technical Datasheet

Code

ENT-TDS

Purpose

Stores technical specifications.

---

## Certificate

Code

ENT-CER

Purpose

Stores compliance certificates.

---

# Engineering Domain

## Equipment

Code

ENT-EQP

Purpose

Represents industrial equipment.

---

## Drawing

Code

ENT-DRW

Purpose

Engineering drawings.

---

## Technical Specification

Code

ENT-SPC

Purpose

Stores engineering specifications.

---

## BOM

Code

ENT-BOM

Purpose

Bill of Materials.

---

# Document Domain

## File

Code

ENT-FIL

Purpose

Stores enterprise files.

---

## Folder

Code

ENT-FDR

Purpose

Organizes documents.

---

## Version

Code

ENT-VSN

Purpose

Tracks document revisions.

---

## Attachment

Code

ENT-ATT

Purpose

Links files to business records.

---

# AI Domain

## Agent

Code

ENT-AIA

Purpose

Represents enterprise AI agents.

---

## Prompt

Code

ENT-PRM

Purpose

Stores reusable prompts.

---

## Conversation

Code

ENT-CNV

Purpose

Stores AI conversations.

---

## Memory

Code

ENT-MEM

Purpose

Stores enterprise AI memory.

---

## Embedding

Code

ENT-EMB

Purpose

Stores vector embeddings.

---

## Knowledge Node

Code

ENT-KNW

Purpose

Represents enterprise knowledge.

---

# Analytics Domain

## Dashboard

Code

ENT-DSH

Purpose

Business dashboards.

---

## KPI

Code

ENT-KPI

Purpose

Enterprise metrics.

---

## Report

Code

ENT-RPT

Purpose

Generated reports.

---

# Audit Domain

## Audit Log

Code

ENT-AUD

Purpose

Tracks system changes.

---

## Security Event

Code

ENT-SEV

Purpose

Stores security events.

---

# Long-Term Vision

The Entity Catalog establishes a common business language across ERP, CRM, AI, Procurement, Engineering, Analytics, and future enterprise services, ensuring consistency, governance, and interoperability throughout the ETA ecosystem.