---
document_id: ETA-ENT-RFQ-004
title: RFQ Business Rules
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Business Rules

## Purpose

This document defines the enterprise business rules governing Request for Quotation (RFQ) records throughout the ETA Enterprise Ecosystem.

These rules ensure procurement integrity, engineering compliance, supplier governance, commercial transparency, ERP consistency, and AI readiness.

---

# Identity Rules

## BR-001

Every RFQ must have one globally unique RFQ ID.

---

## BR-002

RFQ Number must be unique within the company.

---

## BR-003

Customer RFQ Number may repeat across different customers but must be unique per customer.

---

## BR-004

RFQ Type is mandatory.

---

## BR-005

Every RFQ must always have a lifecycle status.

---

# Customer Rules

## BR-006

An RFQ must belong to exactly one Customer.

---

## BR-007

Inactive Customers cannot create new RFQs.

---

## BR-008

Customer Contact must be assigned before RFQ submission.

---

# Product Rules

## BR-009

Every RFQ must contain at least one Product Line.

---

## BR-010

Every Product Line requires Quantity.

---

## BR-011

Every Product Line requires Unit of Measure.

---

## BR-012

Duplicate Product Lines are prohibited unless technically justified.

---

# Engineering Rules

## BR-013

Engineering Review is mandatory before supplier invitation.

---

## BR-014

Incomplete technical specifications prevent RFQ approval.

---

## BR-015

Mandatory datasheets must be attached before submission.

---

## BR-016

Engineering revisions must be frozen after approval.

---

# Supplier Rules

## BR-017

RFQs may only be sent to Approved Suppliers.

---

## BR-018

Preferred Suppliers receive invitation priority.

---

## BR-019

Supplier blacklist prevents RFQ invitation.

---

## BR-020

Supplier response deadlines are mandatory.

---

# Procurement Rules

## BR-021

Strategic RFQs require Procurement Manager approval.

---

## BR-022

Emergency RFQs bypass competitive bidding only with approval.

---

## BR-023

Competitive RFQs should invite at least three suppliers.

---

## BR-024

Budget approval is required before issuing high-value RFQs.

---

## BR-025

RFQ revisions require version history preservation.

---

# Commercial Rules

## BR-026

Currency must be specified before supplier invitation.

---

## BR-027

Payment Terms must be defined.

---

## BR-028

Incoterm must be specified.

---

## BR-029

Commercial conditions become read-only after approval.

---

# Evaluation Rules

## BR-030

Technical evaluation precedes commercial evaluation.

---

## BR-031

Supplier quotations cannot be modified after submission.

---

## BR-032

Award recommendation requires evaluation completion.

---

## BR-033

Award decision requires authorized approval.

---

# AI Rules

## BR-034

AI supplier recommendations are advisory only.

---

## BR-035

AI Risk Score cannot override Compliance decisions.

---

## BR-036

AI recommendations must be traceable.

---

## BR-037

Embeddings regenerate after major RFQ revisions.

---

# Audit Rules

## BR-038

Every RFQ change must be audited.

---

## BR-039

Soft Delete only.

Physical deletion is prohibited.

---

## BR-040

Closed RFQs become read-only except for audit metadata.

---

# Enterprise Rule Summary

The RFQ governance framework ensures:

- Procurement transparency
- Engineering validation
- Supplier compliance
- Commercial consistency
- AI governance
- ERP synchronization
- Complete auditability

---

# Long-Term Vision

The RFQ Business Rules establish a governed procurement workflow that transforms customer demand into compliant sourcing decisions while preserving complete enterprise traceability.