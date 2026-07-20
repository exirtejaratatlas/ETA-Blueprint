---
document_id: ETA-ENT-PAY-006
title: Payment Odoo Mapping
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Payment Odoo Mapping

## Purpose

This document defines the mapping between the ETA Payment entity and Odoo Enterprise Accounting and Treasury models.

ETA extends Odoo by introducing enterprise treasury management, AI-powered payment intelligence, banking integration, liquidity forecasting, and complete financial settlement governance.

---

# Primary Odoo Models

| ETA Entity | Odoo Model |
|------------|------------|
| Payment | account.payment |
| Payment Register | account.payment.register |
| Bank Statement | account.bank.statement |
| Journal Entry | account.move |
| Journal | account.journal |

---

# Core Mapping

| ETA Attribute | Odoo Field |
|---------------|------------|
| Payment ID | x_payment_id |
| Payment Number | name |
| Payment Type | payment_type |
| Partner | partner_id |
| Partner Type | partner_type |
| Company | company_id |
| Journal | journal_id |
| Currency | currency_id |
| Amount | amount |
| Payment Date | date |
| Payment Method | payment_method_line_id |
| State | state |

---

# Treasury Extensions

Custom Fields

- x_treasury_account
- x_cash_flow_category
- x_cash_flow_direction
- x_liquidity_score
- x_treasury_notes
- x_priority_level

---

# Banking Extensions

Custom Fields

- x_bank_reference
- x_swift_reference
- x_tt_reference
- x_lc_reference
- x_cheque_number
- x_guarantee_number

---

# Settlement Extensions

Custom Fields

- x_invoice_reference
- x_contract_reference
- x_purchase_order_reference
- x_reconciliation_status
- x_settlement_status
- x_payment_difference

---

# AI Extensions

Custom Fields

- x_ai_payment_priority
- x_ai_cashflow_forecast
- x_ai_fraud_score
- x_ai_currency_risk
- x_ai_liquidity_prediction
- x_ai_recommendation
- x_embedding_id
- x_knowledge_graph_node

---

# Related Odoo Modules

- Accounting
- Purchase
- Sales
- Inventory
- Documents
- Bank
- Expenses

---

# Security

Supported Roles

- Finance
- Treasury
- Accounting
- Executive
- Auditor
- Administrator

---

# Synchronization Strategy

Synchronization is:

- Real-Time
- Event Driven
- Treasury First
- Financial Consistent
- Audit Logged
- AI Enabled

---

# Upgrade Strategy

ETA extends Odoo exclusively through custom modules.

Native accounting and payment models remain untouched to preserve long-term upgrade compatibility.

---

# Long-Term Vision

ETA transforms Odoo Payments into an enterprise treasury platform supporting payment governance, banking integration, liquidity forecasting, AI financial intelligence, executive treasury analytics, and complete enterprise financial traceability.