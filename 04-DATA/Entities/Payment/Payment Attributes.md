---
document_id: ETA-ENT-PAY-002
title: Payment Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Payment Attributes

## Purpose

This document defines every enterprise attribute belonging to the Payment entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Treasury
- Accounting
- ERP
- Banking
- AI
- REST APIs

---

# Payment Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Payment ID | payment_id | UUID |
| Payment Number | payment_number | String |
| Payment Type | payment_type | Enum |
| Payment Method | payment_method | Enum |
| Payment Status | payment_status | Enum |
| Company | company | Company |
| Branch | branch | Reference |
| Priority | priority | Enum |
| Active | active | Boolean |

---

# Payment Header

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Payment Date | payment_date | Date |
| Value Date | value_date | Date |
| Due Date | due_date | Date |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Payment Reference | payment_reference | String |
| Internal Reference | internal_reference | String |
| Payment Description | payment_description | Text |
| Treasury Status | treasury_status | Enum |

---

# Bank Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Bank Account ID | bank_account_id | Reference |
| Bank Name | bank_name | String |
| Bank Branch | bank_branch | String |
| Account Number | account_number | String |
| IBAN | iban | String |
| SWIFT Code | swift_code | String |
| Routing Number | routing_number | String |
| Beneficiary Name | beneficiary_name | String |
| Beneficiary Account | beneficiary_account | String |
| Beneficiary Bank | beneficiary_bank | String |

---

# Financial References

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Supplier ID | supplier_id | Reference |
| Customer ID | customer_id | Reference |
| Invoice ID | invoice_id | Reference |
| Purchase Order ID | purchase_order_id | Reference |
| Contract ID | contract_id | Reference |
| Accounting Journal | accounting_journal | Reference |
---

# Financial Amounts

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Gross Amount | gross_amount | Decimal |
| Net Amount | net_amount | Decimal |
| Tax Amount | tax_amount | Decimal |
| Discount Amount | discount_amount | Decimal |
| Bank Charges | bank_charges | Decimal |
| Transfer Fees | transfer_fees | Decimal |
| Withholding Tax | withholding_tax | Decimal |
| Total Paid Amount | total_paid_amount | Decimal |
| Outstanding Balance | outstanding_balance | Decimal |
| Settlement Difference | settlement_difference | Decimal |

---

# Currency Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice Currency | invoice_currency | Currency |
| Payment Currency | payment_currency | Currency |
| Functional Currency | functional_currency | Currency |
| Reporting Currency | reporting_currency | Currency |
| Exchange Gain | exchange_gain | Decimal |
| Exchange Loss | exchange_loss | Decimal |
| FX Rate Source | fx_rate_source | String |
| FX Calculation Date | fx_calculation_date | Date |

---

# Settlement Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Settlement Type | settlement_type | Enum |
| Settlement Status | settlement_status | Enum |
| Settlement Date | settlement_date | Date |
| Settlement Reference | settlement_reference | String |
| Reconciliation Status | reconciliation_status | Enum |
| Reconciliation Date | reconciliation_date | Date |
| Clearing Account | clearing_account | String |
| Settlement Remarks | settlement_remarks | Text |

---

# Treasury Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Treasury Account | treasury_account | Reference |
| Treasury Officer | treasury_officer | User |
| Cash Flow Category | cash_flow_category | Enum |
| Cash Flow Direction | cash_flow_direction | Enum |
| Liquidity Impact | liquidity_impact | Decimal |
| Treasury Approval | treasury_approval | Boolean |
| Treasury Approval Date | treasury_approval_date | DateTime |
| Treasury Notes | treasury_notes | Text |
---

# Payment Instruments

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Instrument Type | instrument_type | Enum |
| Cheque Number | cheque_number | String |
| Cheque Date | cheque_date | Date |
| Cheque Bank | cheque_bank | String |
| LC Number | lc_number | String |
| LC Expiry Date | lc_expiry_date | Date |
| TT Number | tt_number | String |
| SWIFT Reference | swift_reference | String |
| Bank Transaction ID | bank_transaction_id | String |
| Payment Gateway Reference | payment_gateway_reference | String |
| POS Reference | pos_reference | String |
| Guarantee Number | guarantee_number | String |

---

# Approval Workflow

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Approval Status | approval_status | Enum |
| Requested By | requested_by | User |
| Requested Date | requested_date | DateTime |
| Approved By | approved_by | User |
| Approval Date | approval_date | DateTime |
| Approval Level | approval_level | Integer |
| Finance Approval | finance_approval | Boolean |
| Treasury Approval | treasury_approval | Boolean |
| Executive Approval | executive_approval | Boolean |
| Approval Remarks | approval_remarks | Text |

---

# AI Financial Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Cash Flow Score | ai_cash_flow_score | Decimal |
| AI Payment Priority | ai_payment_priority | Decimal |
| AI Fraud Score | ai_fraud_score | Decimal |
| AI Currency Risk | ai_currency_risk | Decimal |
| AI Liquidity Forecast | ai_liquidity_forecast | Decimal |
| AI Treasury Recommendation | ai_treasury_recommendation | Text |
| AI Payment Summary | ai_payment_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# Payment Documents

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Payment Voucher | payment_voucher | Array |
| Bank Receipt | bank_receipt | Array |
| SWIFT Copy | swift_copy | Array |
| LC Documents | lc_documents | Array |
| TT Confirmation | tt_confirmation | Array |
| Cheque Scan | cheque_scan | Array |
| Guarantee Documents | guarantee_documents | Array |
| Treasury Documents | treasury_documents | Array |
| Accounting Attachments | accounting_attachments | Array |
| Other Documents | other_documents | Array |
---

# Payment KPI

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Payment Processing Time | payment_processing_time | Integer |
| Average Payment Cycle | average_payment_cycle | Decimal |
| On-Time Payment Rate | on_time_payment_rate | Decimal |
| Cash Flow Accuracy | cash_flow_accuracy | Decimal |
| Treasury Efficiency | treasury_efficiency | Decimal |
| Payment Success Rate | payment_success_rate | Decimal |
| Failed Payment Rate | failed_payment_rate | Decimal |
| Reconciliation Accuracy | reconciliation_accuracy | Decimal |
| FX Cost KPI | fx_cost_kpi | Decimal |
| Treasury KPI Score | treasury_kpi_score | Decimal |

---

# Audit Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Created By | created_by | User |
| Created Date | created_date | DateTime |
| Modified By | modified_by | User |
| Modified Date | modified_date | DateTime |
| Approved By | approved_by | User |
| Approved Date | approved_date | DateTime |
| Executed By | executed_by | User |
| Executed Date | executed_date | DateTime |
| Reconciled By | reconciled_by | User |
| Reconciled Date | reconciled_date | DateTime |
| Archived Date | archived_date | DateTime |
| Version | version | Integer |
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# Enterprise Summary

| Category | Count |
|----------|------:|
| Identity | 9 |
| Header | 9 |
| Banking | 10 |
| Financial References | 6 |
| Financial Amounts | 10 |
| Currency | 8 |
| Settlement | 8 |
| Treasury | 8 |
| Payment Instruments | 12 |
| Approval | 10 |
| AI | 9 |
| Documents | 10 |
| KPI | 10 |
| Audit | 15 |

**Total Enterprise Attributes: ~144**

---

# Long-Term Vision

The Payment entity provides the enterprise treasury and settlement backbone of ETA by integrating procurement, invoices, banking, treasury, accounting, ERP, AI forecasting, liquidity management, and complete financial traceability across the enterprise ecosystem.