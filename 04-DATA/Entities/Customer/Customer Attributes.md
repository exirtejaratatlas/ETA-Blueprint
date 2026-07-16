---
document_id: ETA-ENT-CUSTOMER-002
title: Customer Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Customer Attributes

## Purpose

This document defines every attribute belonging to the Customer entity across the ETA Enterprise Ecosystem.

The attributes defined here serve as the authoritative specification for:

- Database Design
- Odoo ERP
- REST APIs
- AI Knowledge Graph
- Enterprise Search
- Reporting
- Data Warehouse

---

# Attribute Standards

Each attribute contains:

- Business Name
- Technical Name
- Data Type
- Required
- Unique
- Default Value
- Odoo Mapping
- API Name
- Description

---

# Identity Attributes

| Business Name | Technical Name | Type | Required | Unique | Odoo Mapping | API |
|---------------|---------------|------|----------|--------|--------------|-----|
| Customer ID | customer_id | UUID | Yes | Yes | x_customer_id | customerId |
| Customer Code | customer_code | String(30) | Yes | Yes | ref | customerCode |
| ERP ID | erp_id | Integer | No | Yes | id | erpId |
| External ID | external_id | String | No | Yes | x_external_id | externalId |
| Legacy ID | legacy_id | String | No | No | x_legacy_id | legacyId |

---

# Company Information

| Business Name | Technical Name | Type | Required |
|---------------|---------------|------|----------|
| Company Name | company_name | String(255) | Yes |
| Legal Name | legal_name | String(255) | Yes |
| Short Name | short_name | String(100) | No |
| Display Name | display_name | String(255) | Yes |
| Native Name | native_name | String(255) | No |
| English Name | english_name | String(255) | No |

---

# Customer Classification

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Customer Type | customer_type | Enum |
| Customer Category | customer_category | Enum |
| Industry | industry | Enum |
| Market Segment | market_segment | Enum |
| Ownership Type | ownership_type | Enum |
| Organization Size | organization_size | Enum |
| Business Model | business_model | Enum |

---

# Customer Status

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Status | status | Enum |
| Lifecycle Stage | lifecycle_stage | Enum |
| Active | is_active | Boolean |
| Approved | is_approved | Boolean |
| Preferred Customer | is_preferred | Boolean |
| Strategic Customer | is_strategic | Boolean |
| VIP Customer | is_vip | Boolean |

---

# Registration Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Registration Number | registration_number | String |
| National ID | national_id | String |
| Economic Code | economic_code | String |
| Tax Number | tax_number | String |
| VAT Number | vat_number | String |
| Chamber Membership | chamber_membership | String |

---

# Geographic Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Country | country | Reference |
| Province | province | Reference |
| City | city | Reference |
| Address | address | Text |
| Postal Code | postal_code | String |
| Latitude | latitude | Decimal |
| Longitude | longitude | Decimal |

---

# Enterprise Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Company | company_id | Reference |
| Business Unit | business_unit | Reference |
| Created By | created_by | User |
| Created Date | created_date | DateTime |
| Modified By | modified_by | User |
| Modified Date | modified_date | DateTime |
| Version | version | Integer |
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# Contact Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Primary Contact | primary_contact | String |
| Contact Person | contact_person | String |
| Job Title | job_title | String |
| Department | department | String |
| Email | email | Email |
| Secondary Email | email_secondary | Email |
| Mobile | mobile | String |
| Phone | phone | String |
| Fax | fax | String |
| Website | website | URL |
| LinkedIn | linkedin | URL |

---

# Commercial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Sales Region | sales_region | Reference |
| Sales Manager | sales_manager | User |
| Account Manager | account_manager | User |
| Customer Segment | customer_segment | Enum |
| Industry Sector | industry_sector | Enum |
| Customer Priority | customer_priority | Enum |
| Annual Revenue | annual_revenue | Decimal |
| Employee Count | employee_count | Integer |
| Procurement Volume | procurement_volume | Decimal |
| Strategic Account | strategic_account | Boolean |

---

# Financial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Currency | currency | Reference |
| Payment Term | payment_term | Reference |
| Incoterm Preference | incoterm | Reference |
| Credit Limit | credit_limit | Decimal |
| Available Credit | available_credit | Decimal |
| Outstanding Balance | outstanding_balance | Decimal |
| Tax Office | tax_office | String |
| Tax Status | tax_status | Enum |
| Financial Rating | financial_rating | Enum |
| Customer Score | customer_score | Decimal |

---

# Banking Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Bank Name | bank_name | String |
| Branch | bank_branch | String |
| Account Holder | account_holder | String |
| Account Number | account_number | String |
| IBAN | iban | String |
| SWIFT | swift | String |
| Currency Account | bank_currency | Reference |

---

# Credit Management

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Credit Status | credit_status | Enum |
| Credit Risk | credit_risk | Enum |
| Last Credit Review | credit_review_date | Date |
| Credit Reviewer | credit_reviewer | User |
| Payment Performance | payment_performance | Enum |
| Overdue Amount | overdue_amount | Decimal |
| Average Payment Delay | payment_delay_days | Integer |

---

# Procurement Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Preferred Supplier Type | preferred_supplier_type | Enum |
| Preferred Brands | preferred_brands | Multi Select |
| Preferred Country | preferred_country | Multi Select |
| Typical Products | typical_products | Multi Select |
| Procurement Category | procurement_category | Multi Select |
| Tender Participant | tender_participant | Boolean |
| EPC Customer | epc_customer | Boolean |
| Framework Agreement | framework_agreement | Boolean |

---

# Project Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Active Projects | active_projects | Integer |
| Completed Projects | completed_projects | Integer |
| Largest Project Value | largest_project_value | Decimal |
| Last Project Date | last_project_date | Date |
| Current Project Manager | project_manager | User |

---

# Sales Statistics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| First Opportunity Date | first_opportunity_date | Date |
| First Order Date | first_order_date | Date |
| Last Order Date | last_order_date | Date |
| Total Orders | total_orders | Integer |
| Total Sales | total_sales | Decimal |
| Average Order Value | average_order_value | Decimal |
| Win Rate | win_rate | Percentage |
| Customer Lifetime Value | customer_lifetime_value | Decimal |

---

# AI Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Summary | ai_summary | Text |
| AI Classification | ai_classification | Enum |
| AI Confidence | ai_confidence | Decimal |
| AI Customer Score | ai_customer_score | Decimal |
| AI Risk Score | ai_risk_score | Decimal |
| AI Opportunity Score | ai_opportunity_score | Decimal |
| AI Recommendation | ai_recommendation | Text |
| AI Last Analysis | ai_last_analysis | DateTime |

---

# Enterprise Search

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Search Title | search_title | String |
| Search Keywords | search_keywords | Text |
| Search Tags | search_tags | Multi Select |
| Search Category | search_category | String |
| Search Weight | search_weight | Integer |
| Full Text Index | full_text_index | Text |
| AI Embedding ID | embedding_id | UUID |

---

# Compliance

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Sanction Status | sanction_status | Enum |
| Compliance Status | compliance_status | Enum |
| AML Status | aml_status | Enum |
| KYC Status | kyc_status | Enum |
| Last Compliance Review | compliance_review_date | Date |
| Compliance Reviewer | compliance_reviewer | User |

---

# ESG Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| ESG Rating | esg_rating | Enum |
| Sustainability Score | sustainability_score | Decimal |
| Environmental Certification | environmental_certification | Boolean |
| ISO Certifications | iso_certifications | Multi Select |

---

# Enterprise Risk

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Business Risk | business_risk | Enum |
| Financial Risk | financial_risk | Enum |
| Political Risk | political_risk | Enum |
| Country Risk | country_risk | Enum |
| Procurement Risk | procurement_risk | Enum |
| Overall Risk Score | overall_risk_score | Decimal |

---

# AI Knowledge Graph

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Knowledge Node ID | knowledge_node_id | UUID |
| Graph Cluster | graph_cluster | String |
| Related Customers | related_customers | Multi Reference |
| Related Suppliers | related_suppliers | Multi Reference |
| Related Projects | related_projects | Multi Reference |

---

# Enterprise Integration

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| CRM Sync Status | crm_sync_status | Enum |
| ERP Sync Status | erp_sync_status | Enum |
| API Sync Status | api_sync_status | Enum |
| Last Synchronization | last_sync | DateTime |
| Integration Version | integration_version | String |

---

# Extension Fields

Reserved enterprise fields for future expansion.

| Technical Name | Type |
|---------------|------|
| custom_field_01 | Text |
| custom_field_02 | Text |
| custom_field_03 | Text |
| custom_field_04 | Text |
| custom_field_05 | Text |
| custom_field_06 | Text |
| custom_field_07 | Text |
| custom_field_08 | Text |
| custom_field_09 | Text |
| custom_field_10 | Text |

---

# Summary

The Customer entity contains approximately:

- 90+ Enterprise Attributes
- Complete commercial profile
- Financial profile
- Procurement profile
- Project profile
- AI profile
- Compliance profile
- Search profile
- Knowledge Graph metadata

This specification serves as the master reference for:

- PostgreSQL Schema
- Odoo ERP (res.partner)
- REST APIs
- GraphQL
- AI Knowledge Graph
- Enterprise Reporting
- Business Intelligence
- Search Index