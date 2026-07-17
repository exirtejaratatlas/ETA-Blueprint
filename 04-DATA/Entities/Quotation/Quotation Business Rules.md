---
document_id: ETA-ENT-QTN-004
title: Quotation Business Rules
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Business Rules

## Purpose

This document defines the enterprise business rules governing supplier quotations throughout the ETA Enterprise Procurement Ecosystem.

These rules ensure technical compliance, commercial transparency, procurement governance, AI-assisted decision making, and complete auditability.

---

# Identity Rules

## BR-001

Every quotation shall have one globally unique Quotation ID.

---

## BR-002

Quotation Number must be unique.

---

## BR-003

Each quotation must reference exactly one RFQ.

---

## BR-004

Each quotation belongs to exactly one Supplier.

---

## BR-005

Quotation Type is mandatory.

---

# Submission Rules

## BR-006

Suppliers may only submit quotations before the RFQ deadline.

---

## BR-007

Late quotations require Procurement Manager approval.

---

## BR-008

Required documents must be attached before submission.

---

## BR-009

Commercial and Technical proposals must be submitted together unless explicitly separated by the RFQ.

---

# Technical Rules

## BR-010

Engineering Review is mandatory before commercial evaluation.

---

## BR-011

Technical compliance must be evaluated for every quoted product.

---

## BR-012

Technical deviations shall be documented.

---

## BR-013

Engineering approval is required before award.

---

# Commercial Rules

## BR-014

Currency is mandatory.

---

## BR-015

Payment Terms must be specified.

---

## BR-016

Incoterm must be specified.

---

## BR-017

Lead Time must be provided.

---

## BR-018

Warranty period is mandatory where applicable.

---

# Evaluation Rules

## BR-019

Technical evaluation always precedes commercial evaluation.

---

## BR-020

Evaluation scores must be recorded.

---

## BR-021

Award recommendation requires completed evaluation.

---

## BR-022

Rejected quotations remain read-only.

---

# Negotiation Rules

## BR-023

Negotiation creates a new quotation revision.

---

## BR-024

Previous revisions remain immutable.

---

## BR-025

Negotiation history shall never be deleted.

---

# Award Rules

## BR-026

Only approved quotations may be awarded.

---

## BR-027

Award generates Purchase Order(s).

---

## BR-028

Split awards are allowed only when approved.

---

## BR-029

Cancelled quotations cannot be reactivated.

---

# AI Rules

## BR-030

AI recommendations are advisory only.

---

## BR-031

AI ranking cannot override Engineering approval.

---

## BR-032

AI Risk Score cannot override Compliance decisions.

---

## BR-033

Every AI recommendation must be traceable.

---

# Audit Rules

## BR-034

Every quotation modification shall be audited.

---

## BR-035

Soft Delete only.

Physical deletion is prohibited.

---

## BR-036

Awarded quotations become read-only except audit metadata.

---

# Enterprise Rule Summary

The quotation governance framework ensures:

- Engineering compliance
- Commercial transparency
- Supplier fairness
- Negotiation traceability
- AI governance
- ERP synchronization
- Complete procurement auditability

---

# Long-Term Vision

The Quotation Business Rules establish a governed supplier evaluation process that transforms quotations into transparent, measurable, AI-assisted procurement decisions while preserving complete enterprise traceability.