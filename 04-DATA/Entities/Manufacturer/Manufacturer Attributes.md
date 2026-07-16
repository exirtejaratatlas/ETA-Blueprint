---
document_id: ETA-ENT-MANUFACTURER-002
title: Manufacturer Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Manufacturer Attributes

## Purpose

This document defines every enterprise attribute belonging to the Manufacturer entity.

These attributes serve as the master definition for:

- PostgreSQL
- Odoo
- REST APIs
- AI Knowledge Graph
- Enterprise Search
- Business Intelligence

---

# Company Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Manufacturer ID | manufacturer_id | UUID |
| Manufacturer Code | manufacturer_code | String |
| Company Name | company_name | String |
| Legal Name | legal_name | String |
| Trade Name | trade_name | String |
| OEM Type | oem_type | Enum |
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
| Establishment Year | establishment_year | Integer |
| Employee Count | employee_count | Integer |
| Active Status | active | Boolean |

---

# Contact Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| CEO | ceo | String |
| Sales Director | sales_director | String |
| Export Manager | export_manager | String |
| Technical Manager | technical_manager | String |
| Engineering Contact | engineering_contact | String |
| Commercial Contact | commercial_contact | String |
| Email | email | Email |
| Office Phone | office_phone | Phone |
| Mobile | mobile | Phone |
| Emergency Contact | emergency_contact | Phone |

---

# Manufacturing Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Factory Count | factory_count | Integer |
| Manufacturing Capability | manufacturing_capability | Boolean |
| Engineering Capability | engineering_capability | Boolean |
| R&D Capability | rnd_capability | Boolean |
| Production Capacity | production_capacity | String |
| Annual Capacity | annual_capacity | Decimal |
| Lead Time | lead_time_days | Integer |
| Product Families | product_families | Array |
| Supported Industries | supported_industries | Array |
| Global Presence | global_presence | Boolean |

---

# Manufacturing Facilities

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Factory Locations | factory_locations | Array |
| Production Lines | production_lines | Integer |
| CNC Capability | cnc_capability | Boolean |
| Casting Capability | casting_capability | Boolean |
| Forging Capability | forging_capability | Boolean |
| Machining Capability | machining_capability | Boolean |
| Assembly Capability | assembly_capability | Boolean |
| Testing Facility | testing_facility | Boolean |
| Quality Laboratory | quality_lab | Boolean |
| Export License | export_license | Boolean |

---

# Financial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Annual Revenue | annual_revenue | Decimal |
| Revenue Currency | revenue_currency | Currency |
| Financial Rating | financial_rating | Enum |
| Credit Rating | credit_rating | Enum |
| Banking Country | banking_country | String |
| International Banking | international_banking | Boolean |
| Financial Risk Score | financial_risk_score | Decimal |
| Insurance Coverage | insurance_coverage | Boolean |
| Warranty Policy | warranty_policy | Text |
| Financial Status | financial_status | Enum |

---

# Commercial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Sales Regions | sales_regions | Array |
| Countries Served | countries_served | Array |
| Exclusive Distributor | exclusive_distributor | Boolean |
| Authorized Supplier Network | authorized_supplier_network | Boolean |
| Strategic Manufacturer | strategic_manufacturer | Boolean |
| Preferred OEM | preferred_oem | Boolean |
| Incoterms | incoterms | Array |
| Preferred Currency | preferred_currency | Currency |
| Standard Lead Time | standard_lead_time | Integer |
| Commercial Score | commercial_score | Decimal |

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
| PED Certification | ped_certification | Boolean |
| Certificate Expiry | certificate_expiry | Date |

---

# Compliance Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Compliance Status | compliance_status | Enum |
| KYC Status | kyc_status | Enum |
| AML Status | aml_status | Enum |
| Sanction Status | sanction_status | Enum |
| Export Control Status | export_control_status | Enum |
| Compliance Review Date | compliance_review_date | Date |
| Compliance Expiry Date | compliance_expiry_date | Date |
| Approved By | approved_by | User |
| Compliance Notes | compliance_notes | Text |

---

# Product Portfolio

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product Categories | product_categories | Array |
| Product Brands | product_brands | Array |
| Product Standards | product_standards | Array |
| OEM Brands | oem_brands | Array |
| Core Technologies | core_technologies | Array |
| Engineering Standards | engineering_standards | Array |
| Custom Manufacturing | custom_manufacturing | Boolean |
| Private Label Capability | private_label | Boolean |
| Export Products | export_products | Boolean |
| Catalog Available | catalog_available | Boolean |

---

# AI Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Summary | ai_summary | Text |
| AI Manufacturer Score | ai_manufacturer_score | Decimal |
| AI Risk Score | ai_risk_score | Decimal |
| AI Capability Score | ai_capability_score | Decimal |
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
| Contact Information | 10 |
| Manufacturing Information | 10 |
| Manufacturing Facilities | 10 |
| Financial Information | 10 |
| Commercial Information | 10 |
| Certifications | 10 |
| Compliance Information | 9 |
| Product Portfolio | 10 |
| AI Metadata | 9 |
| Enterprise Search | 5 |
| Audit Metadata | 11 |
| Integration Metadata | 6 |

**Total Enterprise Attributes: ~120**