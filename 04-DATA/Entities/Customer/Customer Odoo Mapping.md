---
document_id: ETA-ENT-CUSTOMER-006
title: Customer Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Customer Odoo Mapping

## Purpose

This document maps the ETA Customer entity to the corresponding Odoo Enterprise models.

The objective is to maximize compatibility with Odoo while extending it with ETA-specific enterprise capabilities.

---

# Primary Odoo Model

ETA Entity

↓

Customer

↓

Odoo Model

↓

res.partner

---

# Core Field Mapping

| ETA Field | Odoo Field | Notes |
|------------|------------|------|
| customer_id | x_customer_id | Custom UUID |
| customer_code | ref | Business Code |
| company_name | name | Standard |
| legal_name | x_legal_name | Custom |
| customer_type | company_type | Extended |
| email | email | Standard |
| mobile | mobile | Standard |
| phone | phone | Standard |
| website | website | Standard |
| country | country_id | Standard |
| province | state_id | Standard |
| city | city | Standard |
| address | street | Standard |
| postal_code | zip | Standard |

---

# Commercial Mapping

| ETA | Odoo |
|------|-------|
| account_manager | user_id |
| payment_term | property_payment_term_id |
| currency | property_purchase_currency_id |
| sales_region | x_sales_region |
| strategic_account | x_strategic_account |

---

# Financial Mapping

| ETA | Odoo |
|------|-------|
| credit_limit | credit_limit |
| vat_number | vat |
| tax_number | x_tax_number |
| outstanding_balance | x_outstanding_balance |
| financial_rating | x_financial_rating |

---

# Compliance Mapping

| ETA | Odoo |
|------|-------|
| sanction_status | x_sanction_status |
| aml_status | x_aml_status |
| kyc_status | x_kyc_status |
| compliance_status | x_compliance_status |

---

# AI Extensions

The following fields are ETA custom extensions.

| ETA | Odoo |
|------|-------|
| ai_summary | x_ai_summary |
| ai_risk_score | x_ai_risk_score |
| ai_customer_score | x_ai_customer_score |
| ai_recommendation | x_ai_recommendation |
| embedding_id | x_embedding_id |

---

# Related Odoo Models

Customer interacts with:

- crm.lead
- sale.order
- purchase.order
- account.move
- account.payment
- project.project
- documents.document
- mail.activity
- sign.request

---

# Required Custom Modules

ETA extends Odoo using custom modules.

Examples

- eta_customer
- eta_ai
- eta_procurement
- eta_projects
- eta_compliance

---

# Synchronization Rules

Customer data synchronizes:

ETA

↓

Odoo

↓

External APIs

↓

AI Platform

Synchronization is event-driven.

---

# Custom Fields Prefix

All ETA custom fields use:

```
x_
```

Example

```
x_customer_id

x_ai_summary

x_strategic_account
```

---

# Long-Term Vision

ETA uses the native Odoo Partner model as the enterprise customer master while extending it with AI intelligence, procurement metadata, compliance controls, and enterprise-scale commercial capabilities.