---
document_id: ETA-ENT-PRODUCT-004
title: Product Business Rules
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product Business Rules

## Purpose

This document defines the enterprise business rules governing Product records throughout the ETA Enterprise Ecosystem.

These rules ensure engineering integrity, procurement consistency, inventory accuracy, commercial governance, ERP compliance, and AI readiness.

---

# Identity Rules

## BR-001

Every Product must have one unique Product ID.

---

## BR-002

Product Code must be unique across the enterprise.

---

## BR-003

Duplicate Product Codes are prohibited.

---

## BR-004

Product lifecycle status must always be defined.

---

## BR-005

Archived Products cannot become Active without approval.

---

# Engineering Rules

## BR-006

Every Product must belong to one Product Category.

---

## BR-007

Every Product must reference one Primary Manufacturer.

---

## BR-008

Engineering specifications are mandatory before Approval.

---

## BR-009

Products requiring certification must contain valid certificates.

---

## BR-010

Every engineering revision must be version controlled.

---

## BR-011

Changing technical specifications creates a new revision.

---

## BR-012

Obsolete Products cannot be assigned to new projects.

---

# Manufacturer Rules

## BR-013

Only Approved Manufacturers may produce Products.

---

## BR-014

Preferred Manufacturers receive sourcing priority.

---

## BR-015

Manufacturer replacement requires Engineering approval.

---

# Supplier Rules

## BR-016

Products may have multiple Suppliers.

---

## BR-017

Only Approved Suppliers may receive RFQs.

---

## BR-018

Supplier Lead Time must be maintained.

---

# Procurement Rules

## BR-019

Products marked Strategic require Procurement approval.

---

## BR-020

Critical Spare Parts require Safety Stock.

---

## BR-021

Preferred Supplier selection follows Procurement Policy.

---

## BR-022

Procurement prices must preserve history.

---

## BR-023

Contract-controlled Products require valid contracts.

---

# Inventory Rules

## BR-024

Inventory tracking is mandatory for Stock Items.

---

## BR-025

Serialized Products require Serial Tracking.

---

## BR-026

Batch-controlled Products require Batch Tracking.

---

## BR-027

Negative Inventory is prohibited unless explicitly approved.

---

## BR-028

Reorder Point must not exceed Maximum Stock.

---

# Commercial Rules

## BR-029

Commercial pricing requires valid currency.

---

## BR-030

Expired price records cannot be used.

---

## BR-031

Export-controlled Products require Compliance approval.

---

# AI Rules

## BR-032

Every Active Product must contain AI Summary.

---

## BR-033

AI Recommendations are advisory only.

---

## BR-034

AI Risk Score never overrides Compliance.

---

## BR-035

Embeddings are regenerated after major specification changes.

---

# Audit Rules

## BR-036

Every Product modification is audited.

---

## BR-037

Soft Delete only.

Physical deletion is prohibited.

---

## BR-038

Revision history must be preserved permanently.

---

## BR-039

Every Product must maintain complete traceability.

---

## BR-040

Business Rule violations prevent Product activation.

---

# Enterprise Rule Summary

Critical governance includes:

- Unique Product Code
- Engineering Approval
- Manufacturer Validation
- Supplier Validation
- Inventory Integrity
- Commercial Governance
- AI Readiness
- Complete Audit Trail

---

# Long-Term Vision

The Product business rules establish a trusted enterprise product model that guarantees consistency across engineering, procurement, inventory, logistics, finance, AI, and ERP while preserving complete lifecycle traceability.