---
document_id: ETA-ENT-SUPPLIER-002
title: Supplier Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Supplier Attributes

## Purpose

This document defines every enterprise attribute belonging to the Supplier entity.

These attributes serve as the master definition for:

- PostgreSQL
- Odoo
- REST APIs
- AI Knowledge Graph
- Search Engine
- Enterprise Reporting

---

# Company Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Supplier ID | supplier_id | UUID |
| Supplier Code | supplier_code | String |
| Company Name | company_name | String |
| Legal Name | legal_name | String |
| Trade Name | trade_name | String |
| Supplier Type | supplier_type | Enum |
| Industry | industry | Enum |
| Country | country | Reference |
| Province | province | String |
| City | city | String |
| Address | address | Text |
| Postal Code | postal_code | String |
| Website | website | URL |
| Registration Number | registration_number | String |
| Tax Number | tax_number | String |
| VAT Number | vat_number | String |
| Parent Company | parent_company | Reference |
| Company Size | company_size | Enum |
| Establishment Year | establishment_year | Integer |
| Active Status | active | Boolean |

---

# Contact Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Primary Contact | primary_contact | String |
| Position | position | String |
| Email | email | Email |
| Mobile | mobile | Phone |
| Office Phone | office_phone | Phone |
| Emergency Contact | emergency_contact | Phone |
| Procurement Contact | procurement_contact | String |
| Technical Contact | technical_contact | String |
| Finance Contact | finance_contact | String |

---

# Commercial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Sales Manager | sales_manager | User |
| Procurement Manager | procurement_manager | User |
| Incoterms | incoterms | Reference |
| Preferred Currency | preferred_currency | Currency |
| Payment Terms | payment_terms | Reference |
| Lead Time | lead_time_days | Integer |
| Minimum Order Value | minimum_order_value | Decimal |
| Preferred Supplier | preferred_supplier | Boolean |
| Strategic Supplier | strategic_supplier | Boolean |
| Supplier Rating | supplier_rating | Decimal |

---

# Financial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Credit Rating | credit_rating | Enum |
| Financial Rating | financial_rating | Enum |
| Annual Revenue | annual_revenue | Decimal |
| Currency | currency | Currency |
| Tax Category | tax_category | Enum |
| Financial Risk Score | financial_risk_score | Decimal |
| Payment Performance | payment_performance | Decimal |
| Credit Limit | credit_limit | Decimal |
| Outstanding Balance | outstanding_balance | Decimal |
| Financial Status | financial_status | Enum |

---

# Banking Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Bank Name | bank_name | String |
| Bank Branch | bank_branch | String |
| Account Holder | account_holder | String |
| Account Number | account_number | String |
| IBAN | iban | String |
| SWIFT Code | swift_code | String |
| Routing Number | routing_number | String |
| Currency Account | currency_account | Currency |
| International Payments | international_payments | Boolean |

---

# Commercial Performance

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Total RFQs | total_rfqs | Integer |
| Total Quotations | total_quotations | Integer |
| Total Purchase Orders | total_purchase_orders | Integer |
| Total Contracts | total_contracts | Integer |
| Total Shipments | total_shipments | Integer |
| Average Lead Time | average_lead_time | Integer |
| On-Time Delivery Rate | on_time_delivery_rate | Decimal |
| Quality Score | quality_score | Decimal |
| Commercial Score | commercial_score | Decimal |
| Overall Supplier Score | overall_supplier_score | Decimal |

---

# Compliance Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Compliance Status | compliance_status | Enum |
| KYC Status | kyc_status | Enum |
| AML Status | aml_status | Enum |
| Sanction Status | sanction_status | Enum |
| Compliance Review Date | compliance_review_date | Date |
| Compliance Expiry Date | compliance_expiry_date | Date |
| Approved By | approved_by | User |
| Compliance Notes | compliance_notes | Text |

---

# Certifications

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| ISO 9001 | iso_9001 | Boolean |
| ISO 14001 | iso_14001 | Boolean |
| ISO 45001 | iso_45001 | Boolean |
| API Certification | api_certification | Boolean |
| ASME Certification | asme_certification | Boolean |
| CE Certification | ce_certification | Boolean |
| ATEX Certification | atex_certification | Boolean |
| IECEx Certification | iecex_certification | Boolean |
| Manufacturer Authorization | manufacturer_authorization | Boolean |
| Certificate Expiry | certificate_expiry | Date |

---

# Procurement Capabilities

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product Categories | product_categories | Array |
| Supported Brands | supported_brands | Array |
| Manufacturing Capability | manufacturing_capability | Boolean |
| Engineering Capability | engineering_capability | Boolean |
| Logistics Capability | logistics_capability | Boolean |
| Export Capability | export_capability | Boolean |
| Import Capability | import_capability | Boolean |
| Countries Served | countries_served | Array |
| Production Capacity | production_capacity | String |
| Preferred Incoterms | preferred_incoterms | Array |

---

# AI Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Summary | ai_summary | Text |
| AI Risk Score | ai_risk_score | Decimal |
| AI Supplier Score | ai_supplier_score | Decimal |
| AI Recommendation | ai_recommendation | Text |
| AI Classification | ai_classification | Enum |
| AI Confidence | ai_confidence | Decimal |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# Enterprise Search

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Search Title | search_title | String |
| Search Keywords | search_keywords | Array |
| Search Tags | search_tags | Array |
| Business Classification | business_classification | String |
| Full Text Index | full_text_index | Text |

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
| Version | version | Integer |
| Status | status | Enum |
| Company | company | Company |
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# Integration Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| ERP ID | erp_id | String |
| External ID | external_id | String |
| Import Batch | import_batch | String |
| Source System | source_system | String |
| Last Synchronization | last_sync | DateTime |
| Synchronization Status | sync_status | Enum |

---

# Summary

Approximate Attribute Count

| Category | Count |
|----------|------:|
| Company Information | 20 |
| Contact Information | 9 |
| Commercial Information | 10 |
| Financial Information | 10 |
| Banking Information | 9 |
| Compliance Information | 8 |
| Certifications | 10 |
| Procurement Capabilities | 10 |
| AI Metadata | 8 |
| Enterprise Search | 5 |
| Audit Metadata | 11 |
| Integration Metadata | 6 |

**Total Enterprise Attributes: ~116**