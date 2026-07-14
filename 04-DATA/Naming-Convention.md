---
document_id: ETA-DATA-009
title: Naming Convention
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
website: https://exiratlas.com
classification: Internal
last_updated: 2026
---

# ETA Naming Convention

## Purpose

This document defines enterprise naming standards used across the ETA Enterprise Procurement Ecosystem.

Consistent naming improves maintainability, readability, interoperability, automation, and AI understanding.

---

# General Principles

Naming should be

- Consistent
- Human Readable
- Machine Friendly
- Unique
- Stable
- Future Proof

Avoid

- Abbreviations without documentation
- Spaces
- Local language identifiers
- Special characters

---

# Business Entity Names

Use

PascalCase

Examples

Customer

Supplier

PurchaseOrder

TechnicalSpecification

EngineeringPackage

KnowledgeNode

---

# Database Tables

Use

snake_case

Examples

customer

supplier

purchase_order

technical_specification

knowledge_node

audit_log

---

# Database Columns

Use

camelCase

Examples

customerId

supplierId

createdAt

updatedAt

purchaseOrderNumber

---

# Primary Keys

Always

id

Type

UUID

---

# Foreign Keys

Convention

entityId

Examples

customerId

supplierId

productId

rfqId

contractId

---

# API Endpoints

Use

kebab-case

Examples

/api/customers

/api/purchase-orders

/api/rfqs

/api/suppliers

/api/ai-agents

---

# JSON Fields

Use

camelCase

Example

{
  "customerId": "...",
  "purchaseOrderNumber": "...",
  "createdAt": "..."
}

---

# File Naming

Use

PascalCase for official documents

Examples

CompanyProfile.pdf

SupplierEvaluation.xlsx

PurchaseOrderTemplate.docx

---

Technical files

Use

kebab-case

Examples

supplier-list.csv

product-catalog.json

knowledge-export.zip

---

# Git Branches

Convention

type/description

Examples

feature/procurement-workflow

feature/ai-agent

bugfix/login

hotfix/payment

docs/data-layer

refactor/api

---

# Git Tags

Convention

vMajor.Minor.Patch

Examples

v1.0.0

v1.1.0

v2.0.0

---

# Docker

Images

eta-api

eta-web

eta-ai

eta-worker

Containers

eta-api-prod

eta-ai-prod

eta-postgres

eta-qdrant

---

# AI Agents

Convention

ETA-{Domain}-Agent

Examples

ETA-Procurement-Agent

ETA-Sales-Agent

ETA-Engineering-Agent

ETA-RAG-Agent

ETA-Analytics-Agent

ETA-Orchestrator

---

# Prompt Names

Convention

Domain_Action

Examples

Procurement_RFQAnalysis

Sales_CustomerSummary

Engineering_DatasheetReview

AI_KnowledgeSearch

---

# Document Codes

Convention

ETA-DOMAIN-Number

Examples

ETA-RFQ-000001

ETA-PO-000021

ETA-CON-000005

ETA-INV-000003

---

# Master Data Codes

Customers

ETA-CUS-000001

Suppliers

ETA-SUP-000001

Manufacturers

ETA-MFG-000001

Products

ETA-PRD-000001

Materials

ETA-MAT-000001

Equipment

ETA-EQP-000001

---

# AI Object Codes

Agent

ETA-AIA-001

Prompt

ETA-PRM-001

Memory

ETA-MEM-001

Knowledge Node

ETA-KNW-001

Embedding

ETA-EMB-001

---

# Environment Names

Development

dev

Testing

test

Staging

staging

Production

prod

---

# Domain Standards

Primary Domain

exiratlas.com

Recommended Subdomains

www.exiratlas.com

api.exiratlas.com

portal.exiratlas.com

docs.exiratlas.com

supplier.exiratlas.com

customer.exiratlas.com

ai.exiratlas.com

---

# Reserved Prefixes

ETA

Enterprise Objects

SYS

System Objects

AI

Artificial Intelligence

TMP

Temporary Objects

INT

Integration Objects

---

# Long-Term Vision

ETA maintains a unified enterprise naming standard across business entities, databases, APIs, AI agents, infrastructure, documentation, and integrations to ensure clarity, consistency, automation readiness, and long-term maintainability throughout the Exir Tejarat Atlas ecosystem.