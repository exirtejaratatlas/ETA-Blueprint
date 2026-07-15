---
document_id: ETA-DATA-001
title: Enterprise Data Dictionary
version: 1.0
status: Draft
owner: Exir Tejarat Atlas
---

# Enterprise Data Dictionary

## Purpose

## Naming Standards

## Core Enterprise Entities
---

# Customer

## Description

Represents any organization or legal entity that purchases products or services from ETA.

## Entity Type

Master Data

## Owner Domain

CRM

## Primary Identifier

Customer ID

## Core Attributes

- Customer ID
- Customer Code
- Legal Name
- Commercial Name
- Registration Number
- National ID
- Tax Number
- Industry
- Country
- City
- Address
- Postal Code
- Website
- Phone
- Email
- Status
- Customer Category
- Credit Limit
- Currency
- Payment Terms
- Incoterms
- Sales Owner
- Risk Level

## Relationships

Customer
→ Opportunities

Customer
→ Quotations

Customer
→ Contracts

Customer
→ Projects

Customer
→ Invoices

Customer
→ Payments

## Created By

CRM

## Read By

Procurement

Finance

Projects

AI

Reporting

## Update Rules

Only CRM can modify Customer Master Data.

## Business Rules

- Customer Code must be unique.
- Legal Name cannot be empty.
- One Tax Number per Customer.
- Customer Status controls transaction availability.

## AI Usage

- Customer Scoring
- Sales Prediction
- Opportunity Recommendation
- Risk Analysis
- Customer Insights

### Customer

### Supplier

### Manufacturer

### Product

### RFQ

### Quotation

### Purchase Order

### Contract

### Warehouse

### Inventory

### Invoice

### Payment

### Tax

### Project

### User

### Role

### Permission

### AI Knowledge

## Relationships

## Master Data

## Transaction Data

## Reference Data

## Data Ownership

## Data Lifecycle

## Data Quality Rules