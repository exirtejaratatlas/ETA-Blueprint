---
document_id: ETA-ENT-SUPPLIER-004
title: Supplier Business Rules
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier Business Rules

## Purpose

This document defines the enterprise business rules governing Supplier records throughout the ETA Enterprise Ecosystem.

These rules ensure supplier data integrity, procurement compliance, financial governance, and AI readiness.

---

# Identity Rules

## BR-001

Every Supplier must have one unique Supplier ID.

---

## BR-002

Supplier Code must be unique across the enterprise.

---

## BR-003

Duplicate Legal Company Names are prohibited.

---

## BR-004

A Supplier cannot be both Active and Archived.

---

# Registration Rules

## BR-005

Supplier must specify Supplier Type.

---

## BR-006

Country is mandatory.

---

## BR-007

Company Name is mandatory.

---

## BR-008

Registration Number is mandatory for corporate suppliers.

---

## BR-009

Tax Number is required when local regulations apply.

---

# Procurement Rules

## BR-010

Only Approved Suppliers may receive RFQs.

---

## BR-011

Only Active Suppliers may receive Purchase Orders.

---

## BR-012

Inactive Suppliers cannot submit Quotations.

---

## BR-013

Suspended Suppliers cannot receive new Contracts.

---

## BR-014

Supplier performance affects sourcing priority.

---

# Financial Rules

## BR-015

Suppliers exceeding financial risk thresholds require Finance approval.

---

## BR-016

Payment Terms must exist before Purchase Orders are approved.

---

## BR-017

Outstanding Balance cannot become negative.

---

## BR-018

Currency must be defined for international suppliers.

---

# Compliance Rules

## BR-019

KYC approval is required before activation.

---

## BR-020

AML screening must pass before contract execution.

---

## BR-021

Sanctioned suppliers cannot become Active.

---

## BR-022

Expired certifications generate Compliance alerts.

---

## BR-023

Compliance reviews must occur periodically.

---

# Contract Rules

## BR-024

Supplier Contracts require Legal approval.

---

## BR-025

Expired Contracts cannot generate Purchase Orders.

---

# AI Rules

## BR-026

Every Active Supplier must maintain an AI Summary.

---

## BR-027

AI Risk Score cannot overwrite Compliance decisions.

---

## BR-028

AI Recommendations are advisory only.

---

# Audit Rules

## BR-029

Every Supplier modification is audited.

---

## BR-030

Supplier deletion is prohibited.

Only Soft Delete (Archive) is allowed.

---

# Enterprise Rule Summary

Critical enterprise rules include:

- Unique Supplier Code
- Mandatory KYC
- Mandatory Compliance
- Procurement Approval
- Financial Validation
- Contract Governance
- Complete Audit Trail

---

# Long-Term Vision

Business rules ensure that Supplier data remains trusted, auditable, compliant, AI-ready, and fully aligned with enterprise procurement governance across ETA.