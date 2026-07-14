---
document_id: ETA-DATA-015
title: Knowledge Graph
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
website: https://exiratlas.com
classification: Internal
last_updated: 2026
---

# ETA Enterprise Knowledge Graph

## Purpose

The ETA Knowledge Graph represents the semantic brain of the Exir Tejarat Atlas ecosystem.

Unlike relational databases that store structured records, the Knowledge Graph models relationships between business entities, engineering knowledge, procurement activities, AI memories and organizational intelligence.

Its purpose is to enable reasoning, semantic search, contextual retrieval, recommendation engines and autonomous AI agents.

---

# Design Principles

- Business First
- AI Native
- Graph Driven
- Explainable
- Traceable
- Multi-Agent Ready
- Enterprise Scale
- Continuous Evolution

---

# High-Level Architecture

Enterprise Data

↓

Knowledge Extraction

↓

Entity Recognition

↓

Relationship Discovery

↓

Knowledge Graph

↓

Reasoning Engine

↓

AI Agents

↓

Business Decisions

---

# Core Node Categories

## Organization

Nodes

- Company
- Business Unit
- Department
- Team
- Employee
- Role
- Office
- Country

---

## Customer Domain

Nodes

- Customer
- Contact
- Opportunity
- Lead
- Project
- Contract

Relationships

Customer

HAS_CONTACT

HAS_PROJECT

SIGNED_CONTRACT

GENERATED_OPPORTUNITY

---

## Supplier Domain

Nodes

- Supplier
- Manufacturer
- Distributor
- Brand
- Country
- Certificate

Relationships

Supplier

SUPPLIES

MANUFACTURES

AUTHORIZED_BY

CERTIFIED_BY

---

## Product Domain

Nodes

- Product
- Equipment
- Material
- Spare Part
- Service
- Category

Relationships

Product

BELONGS_TO_CATEGORY

REQUIRES

COMPATIBLE_WITH

REPLACED_BY

MANUFACTURED_BY

SUPPLIED_BY

---

## Engineering Domain

Nodes

- Datasheet
- Drawing
- Specification
- Standard
- Material Grade
- Pressure Class
- Certificate

Relationships

Specification

REFERENCES_STANDARD

USES_MATERIAL

HAS_DRAWING

HAS_DATASHEET

---

## Procurement Domain

Nodes

- RFQ
- Quotation
- Purchase Order
- Shipment
- Invoice
- Inspection
- Vendor Evaluation

Relationships

RFQ

REQUESTED_FROM

GENERATED_QUOTATION

CONVERTED_TO_PO

PO

RESULTED_IN_SHIPMENT

RESULTED_IN_INVOICE

---

## Financial Domain

Nodes

- Currency
- Exchange Rate
- Payment
- Bank
- Invoice
- Cost Center

Relationships

Invoice

PAID_BY

USES_CURRENCY

BELONGS_TO_COST_CENTER

---

## AI Domain

Nodes

- Agent
- Prompt
- Memory
- Embedding
- Knowledge Node
- Decision
- Conversation
- Workflow

Relationships

Agent

USED_PROMPT

CREATED_MEMORY

GENERATED_DECISION

REFERENCED_NODE

---

# Relationship Types

Business

- OWNS
- BELONGS_TO
- HAS
- CREATED
- UPDATED
- APPROVED

Commercial

- PURCHASED_FROM
- SOLD_TO
- NEGOTIATED_WITH
- CONTRACTED_WITH

Engineering

- REFERENCES
- DEPENDS_ON
- COMPATIBLE_WITH
- REPLACES

AI

- REMEMBERS
- LEARNED_FROM
- GENERATED
- RECOMMENDED
- VERIFIED_BY

Operational

- TRIGGERED
- EXECUTED
- ASSIGNED_TO
- CLOSED_BY

---

# Knowledge Sources

The Knowledge Graph is populated from

- PostgreSQL
- Odoo ERP
- Microsoft Dynamics CRM
- Documents
- Emails
- Contracts
- RFQs
- Purchase Orders
- Engineering Files
- AI Conversations
- Meeting Notes
- Enterprise Policies

---

# AI Reasoning

The graph enables AI to answer questions such as

- Which supplier is most reliable for API pumps?

- Which customers buy galvanized steel every year?

- Which manufacturers are approved for this specification?

- What products are compatible with this equipment?

- Which quotation became a purchase order?

- Which suppliers worked with this customer before?

- Which engineering standard applies here?

- Which projects are similar?

---

# Graph Traversal

Typical traversal

Customer

↓

Opportunity

↓

RFQ

↓

Product

↓

Supplier

↓

Manufacturer

↓

Purchase Order

↓

Shipment

↓

Invoice

↓

Payment

---

# AI Integration

The graph integrates with

- Qdrant
- PostgreSQL
- Enterprise RAG
- AI Memory
- Multi-Agent System
- Analytics
- Recommendation Engine

---

# Governance

Every node includes

- UUID
- Source
- Owner
- Confidence Score
- CreatedAt
- UpdatedAt
- Version
- Classification

Relationships are versioned and auditable.

---

# Security

Graph access follows

Role-Based Access Control

Attribute-Based Access Control

Enterprise Data Classification

Least Privilege

Highly Restricted data is never exposed through unrestricted graph traversal.

---

# Performance

Support

- Millions of nodes
- Tens of millions of relationships
- Semantic search
- Multi-hop traversal
- Graph analytics
- AI reasoning

---

# Future Expansion

The Knowledge Graph will evolve to include

- Digital Twin relationships
- Supply Chain Network
- Risk Graph
- Compliance Graph
- Engineering Dependency Graph
- Customer Behavior Graph
- Procurement Intelligence Graph
- Autonomous Agent Collaboration Graph

---

# Long-Term Vision

The ETA Knowledge Graph becomes the institutional intelligence layer of Exir Tejarat Atlas.

Rather than storing isolated records, the organization maintains a living enterprise knowledge network where customers, suppliers, products, engineering knowledge, procurement history, AI memories, financial information and business decisions are permanently connected, continuously enriched and instantly available for intelligent reasoning across every AI agent and enterprise application.