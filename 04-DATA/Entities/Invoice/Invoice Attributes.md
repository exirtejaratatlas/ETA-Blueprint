---
document_id: ETA-ENT-INVC-002
title: Invoice Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Invoice Attributes

## Purpose

This document defines every enterprise attribute belonging to the Invoice entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Accounting
- Finance
- Procurement
- ERP
- AI
- REST APIs

---

# Invoice Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice ID | invoice_id | UUID |
| Invoice Number | invoice_number | String |
| Supplier Invoice Number | supplier_invoice_number | String |
| Customer Invoice Number | customer_invoice_number | String |
| Invoice Type | invoice_type | Enum |
| Invoice Status | invoice_status | Enum |
| Priority | priority | Enum |
| Company | company | Company |
| Active | active | Boolean |

---

# Invoice Header

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice Date | invoice_date | Date |
| Due Date | due_date | Date |
| Posting Date | posting_date | Date |
| Accounting Period | accounting_period | String |
| Fiscal Year | fiscal_year | Integer |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Payment Terms | payment_terms | String |
| Payment Method | payment_method | Enum |
| Payment Status | payment_status | Enum |

---

# Supplier Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Supplier ID | supplier_id | Reference |
| Supplier Name | supplier_name | String |
| Supplier Tax ID | supplier_tax_id | String |
| Supplier Address | supplier_address | Text |
| Supplier Contact | supplier_contact | String |

---

# Customer Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Customer ID | customer_id | Reference |
| Customer Name | customer_name | String |
| Customer Tax ID | customer_tax_id | String |
| Customer Address | customer_address | Text |
| Customer Contact | customer_contact | String |

---

# Procurement References

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| RFQ ID | rfq_id | Reference |
| Quotation ID | quotation_id | Reference |
| Purchase Order ID | purchase_order_id | Reference |
| Contract ID | contract_id | Reference |
| Shipment ID | shipment_id | Reference |
| Inventory Transaction | inventory_transaction | Reference |
---

# Invoice Lines

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Line ID | line_id | UUID |
| Product ID | product_id | Reference |
| Product Code | product_code | String |
| Product Description | product_description | Text |
| Quantity | quantity | Decimal |
| Unit of Measure | uom | UOM |
| Unit Price | unit_price | Decimal |
| Line Discount | line_discount | Decimal |
| Line Total | line_total | Decimal |
| Cost Center | cost_center | Reference |

---

# Tax Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Tax Code | tax_code | String |
| Tax Category | tax_category | Enum |
| VAT Rate | vat_rate | Decimal |
| VAT Amount | vat_amount | Decimal |
| Withholding Tax | withholding_tax | Decimal |
| Customs Tax | customs_tax | Decimal |
| Other Taxes | other_taxes | Decimal |
| Total Tax | total_tax | Decimal |

---

# Discount Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Header Discount | header_discount | Decimal |
| Discount Type | discount_type | Enum |
| Promotional Discount | promotional_discount | Decimal |
| Contract Discount | contract_discount | Decimal |
| Early Payment Discount | early_payment_discount | Decimal |
| Total Discount | total_discount | Decimal |

---

# Cost Allocation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Project ID | project_id | Reference |
| Department | department | String |
| Business Unit | business_unit | String |
| Cost Center | cost_center | Reference |
| Profit Center | profit_center | Reference |
| GL Account | gl_account | String |
| Allocation Method | allocation_method | Enum |
| Allocation Percentage | allocation_percentage | Decimal |

---

# Financial Totals

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Subtotal | subtotal | Decimal |
| Total Discount Amount | total_discount_amount | Decimal |
| Total Tax Amount | total_tax_amount | Decimal |
| Freight Amount | freight_amount | Decimal |
| Insurance Amount | insurance_amount | Decimal |
| Other Charges | other_charges | Decimal |
| Grand Total | grand_total | Decimal |
| Amount Paid | amount_paid | Decimal |
| Outstanding Balance | outstanding_balance | Decimal |
| Payment Difference | payment_difference | Decimal |
---

# Approval Workflow

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Approval Status | approval_status | Enum |
| Submitted By | submitted_by | User |
| Submitted Date | submitted_date | DateTime |
| Approved By | approved_by | User |
| Approval Date | approval_date | DateTime |
| Approval Level | approval_level | Integer |
| Approval Remarks | approval_remarks | Text |
| Rejection Reason | rejection_reason | Text |

---

# Three-Way Matching

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Purchase Order Match | purchase_order_match | Boolean |
| Goods Receipt Match | goods_receipt_match | Boolean |
| Contract Match | contract_match | Boolean |
| Matching Status | matching_status | Enum |
| Matching Score | matching_score | Decimal |
| Matching Exception | matching_exception | Text |
| Exception Resolution | exception_resolution | Text |

---

# Accounting Integration

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Journal Entry | journal_entry | Reference |
| Journal Number | journal_number | String |
| Posting Status | posting_status | Enum |
| Posted By | posted_by | User |
| Posted Date | posted_date | DateTime |
| Fiscal Document Number | fiscal_document_number | String |
| Accounting Remarks | accounting_remarks | Text |

---

# AI Financial Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Fraud Score | ai_fraud_score | Decimal |
| AI Duplicate Detection | ai_duplicate_detection | Boolean |
| AI Tax Validation | ai_tax_validation | Decimal |
| AI Payment Recommendation | ai_payment_recommendation | Text |
| AI Cost Analysis | ai_cost_analysis | Text |
| AI Invoice Risk | ai_invoice_risk | Decimal |
| AI Financial Summary | ai_financial_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# Invoice Documents

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice PDF | invoice_pdf | Array |
| Supplier Invoice | supplier_invoice | Array |
| Tax Invoice | tax_invoice | Array |
| Commercial Invoice | commercial_invoice | Array |
| Credit Note | credit_note | Array |
| Debit Note | debit_note | Array |
| Supporting Documents | supporting_documents | Array |
| Accounting Attachments | accounting_attachments | Array |
| Other Documents | other_documents | Array |
---

# Financial KPI

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice Accuracy | invoice_accuracy | Decimal |
| Payment Cycle | payment_cycle | Integer |
| Days Payable Outstanding | days_payable_outstanding | Decimal |
| Days Sales Outstanding | days_sales_outstanding | Decimal |
| Matching Accuracy | matching_accuracy | Decimal |
| Tax Compliance Score | tax_compliance_score | Decimal |
| Collection Performance | collection_performance | Decimal |
| Payment Performance | payment_performance | Decimal |
| Invoice Processing Time | invoice_processing_time | Integer |
| Financial KPI Score | financial_kpi_score | Decimal |

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
| Posted By | posted_by | User |
| Posted Date | posted_date | DateTime |
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
| Header | 10 |
| Supplier | 5 |
| Customer | 5 |
| Procurement References | 6 |
| Invoice Lines | 10 |
| Tax | 8 |
| Discount | 6 |
| Cost Allocation | 8 |
| Financial Totals | 10 |
| Approval | 8 |
| Three-Way Matching | 7 |
| Accounting | 7 |
| AI | 9 |
| Documents | 9 |
| KPI | 10 |
| Audit | 13 |

**Total Enterprise Attributes: ~160**

---

# Long-Term Vision

The Invoice entity serves as the enterprise financial documentation layer of ETA by integrating procurement, logistics, inventory, accounting, taxation, ERP, AI validation, payment preparation, and complete financial traceability across the procurement ecosystem.