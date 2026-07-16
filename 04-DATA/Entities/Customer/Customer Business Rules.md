---
document_id: ETA-ENT-CUSTOMER-004
title: Customer Business Rules
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Customer Business Rules

## Purpose

This document defines all enterprise business rules governing the Customer entity within the ETA Enterprise Ecosystem.

These rules are independent of implementation and must be enforced consistently across ERP, APIs, AI agents, workflows, and integrations.

---

# Identity Rules

## BR-001

Every Customer must have exactly one unique Customer ID.

---

## BR-002

Customer Code must be unique across the entire enterprise.

---

## BR-003

Customer IDs are immutable after creation.

---

## BR-004

A Customer cannot be physically deleted once referenced by any business transaction.

Soft Delete must be used.

---

# Registration Rules

## BR-005

Legal Name is mandatory.

---

## BR-006

Country is mandatory.

---

## BR-007

Customer Type must be selected before activation.

---

## BR-008

Status defaults to Draft upon creation.

---

# Activation Rules

## BR-009

A Customer cannot become Active until mandatory fields are completed.

Mandatory fields include:

- Company Name
- Legal Name
- Country
- Customer Type
- Sales Manager

---

## BR-010

Only authorized users may activate a Customer.

---

# CRM Rules

## BR-011

A Lead may create only one Customer.

---

## BR-012

Won Opportunities must reference an Active Customer.

---

## BR-013

Customer ownership belongs to one Account Manager.

---

# Procurement Rules

## BR-014

RFQs require an Active Customer.

---

## BR-015

Purchase Requests inherit Customer information from the originating Opportunity or Project.

---

# Contract Rules

## BR-016

Contracts cannot exist without an Active Customer.

---

## BR-017

Archived Customers retain historical Contracts permanently.

---

# Project Rules

## BR-018

Projects require exactly one Customer.

---

## BR-019

Project ownership never changes Customer ownership.

---

# Finance Rules

## BR-020

Invoices require an Active Customer.

---

## BR-021

Payment Terms are mandatory before invoicing.

---

## BR-022

Credit Limit must be approved by Finance.

---

## BR-023

Outstanding Balance cannot exceed approved Credit Limit unless overridden by authorized Finance personnel.

---

# Compliance Rules

## BR-024

Sanctioned Customers cannot receive Purchase Orders.

---

## BR-025

Failed KYC prevents activation.

---

## BR-026

Compliance review expires after the configured review period.

---

# AI Rules

## BR-027

Every Active Customer must have an AI Summary.

---

## BR-028

AI recommendations never override human approval.

---

## BR-029

AI Risk Score must be recalculated after significant commercial events.

---

# Security Rules

## BR-030

Every modification is fully audited.

---

## BR-031

Customer ownership controls record-level access.

---

## BR-032

Sensitive financial fields require Finance permissions.

---

# Integration Rules

## BR-033

Customer synchronization with ERP is asynchronous.

---

## BR-034

Duplicate Customers must be detected before synchronization.

---

## BR-035

External IDs must remain stable after synchronization.

---

# Lifecycle Rules

Draft

↓

Review

↓

Approved

↓

Active

↓

Inactive

↓

Archived

Transitions outside this lifecycle are prohibited.

---

# Long-Term Vision

Customer Business Rules ensure that customer information remains consistent, secure, compliant, and enterprise-ready across every ETA module while enabling AI-assisted decision making without compromising governance.