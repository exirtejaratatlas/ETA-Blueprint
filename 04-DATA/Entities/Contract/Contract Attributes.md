---
document_id: ETA-ENT-CON-002
title: Contract Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Contract Attributes

## Purpose

This document defines every enterprise attribute belonging to the Contract entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Procurement
- Sales
- Legal
- Finance
- ERP
- AI
- REST APIs

---

# Contract Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Contract ID | contract_id | UUID |
| Contract Number | contract_number | String |
| External Contract Number | external_contract_number | String |
| Framework Agreement Number | framework_agreement_number | String |
| Parent Contract | parent_contract | Reference |
| Revision | revision | Integer |
| Version | version | Integer |
| Contract Type | contract_type | Enum |
| Contract Status | contract_status | Enum |
| Priority | priority | Enum |
| Active | active | Boolean |

---

# Contract Parties

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Customer ID | customer_id | Reference |
| Customer Name | customer_name | String |
| Supplier ID | supplier_id | Reference |
| Supplier Name | supplier_name | String |
| Manufacturer ID | manufacturer_id | Reference |
| Manufacturer Name | manufacturer_name | String |
| Company | company | Company |
| Business Unit | business_unit | String |
| Contract Owner | contract_owner | User |
| Legal Owner | legal_owner | User |

---

# General Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Subject | subject | String |
| Contract Title | contract_title | String |
| Scope of Work | scope_of_work | Text |
| Executive Summary | executive_summary | Text |
| Commercial Summary | commercial_summary | Text |
| Technical Summary | technical_summary | Text |
| Internal Notes | internal_notes | Text |
| Governing Law | governing_law | String |
| Governing Country | governing_country | Country |
| Contract Language | contract_language | String |

---

# Contract Dates

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Contract Date | contract_date | Date |
| Effective Date | effective_date | Date |
| Start Date | start_date | Date |
| End Date | end_date | Date |
| Renewal Date | renewal_date | Date |
| Expiration Date | expiration_date | Date |
| Signed Date | signed_date | Date |
| Last Amendment Date | last_amendment_date | Date |
---

# Commercial Terms

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Contract Value | contract_value | Decimal |
| Estimated Value | estimated_value | Decimal |
| Minimum Order Value | minimum_order_value | Decimal |
| Maximum Order Value | maximum_order_value | Decimal |
| Incoterm | incoterm | Enum |
| Payment Terms | payment_terms | Enum |
| Delivery Terms | delivery_terms | Text |
| Warranty Period | warranty_period | Integer |
| Warranty Description | warranty_description | Text |
| Commercial Notes | commercial_notes | Text |

---

# Financial Terms

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Advance Payment | advance_payment | Decimal |
| Retention Percentage | retention_percentage | Decimal |
| Performance Bond Required | performance_bond_required | Boolean |
| Advance Payment Guarantee | advance_payment_guarantee | Boolean |
| Performance Guarantee | performance_guarantee | Boolean |
| Bank Guarantee Amount | bank_guarantee_amount | Decimal |
| Credit Period | credit_period | Integer |
| Tax Rules | tax_rules | Text |
| Penalty Rules | penalty_rules | Text |
| Liquidated Damages | liquidated_damages | Decimal |

---

# Legal Conditions

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Governing Law | governing_law | String |
| Jurisdiction | jurisdiction | String |
| Arbitration Required | arbitration_required | Boolean |
| Arbitration Location | arbitration_location | String |
| Confidentiality Required | confidentiality_required | Boolean |
| NDA Reference | nda_reference | String |
| Force Majeure Clause | force_majeure_clause | Boolean |
| Intellectual Property Clause | intellectual_property_clause | Boolean |
| Compliance Requirements | compliance_requirements | Text |
| Legal Notes | legal_notes | Text |

---

# Contract Duration

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Initial Duration | initial_duration | Integer |
| Renewal Allowed | renewal_allowed | Boolean |
| Renewal Period | renewal_period | Integer |
| Auto Renewal | auto_renewal | Boolean |
| Maximum Renewals | maximum_renewals | Integer |
| Notice Period | notice_period | Integer |
---

# Deliverables

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Deliverable ID | deliverable_id | UUID |
| Deliverable Name | deliverable_name | String |
| Deliverable Description | deliverable_description | Text |
| Deliverable Quantity | deliverable_quantity | Decimal |
| Deliverable Unit | deliverable_unit | UOM |
| Delivery Milestone | delivery_milestone | String |
| Planned Delivery Date | planned_delivery_date | Date |
| Actual Delivery Date | actual_delivery_date | Date |
| Deliverable Status | deliverable_status | Enum |
| Acceptance Status | acceptance_status | Enum |

---

# Contract Obligations

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Supplier Obligations | supplier_obligations | Text |
| Customer Obligations | customer_obligations | Text |
| ETA Obligations | eta_obligations | Text |
| Milestone Obligations | milestone_obligations | Text |
| Reporting Requirements | reporting_requirements | Text |
| Documentation Requirements | documentation_requirements | Text |
| Training Requirements | training_requirements | Text |
| Support Requirements | support_requirements | Text |

---

# Compliance

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Compliance Status | compliance_status | Enum |
| Regulatory Compliance | regulatory_compliance | Text |
| HSE Compliance | hse_compliance | Boolean |
| ISO Compliance | iso_compliance | Boolean |
| Quality Compliance | quality_compliance | Boolean |
| Export Compliance | export_compliance | Boolean |
| Sanctions Compliance | sanctions_compliance | Boolean |
| Compliance Notes | compliance_notes | Text |

---

# Amendments

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Amendment Number | amendment_number | String |
| Amendment Date | amendment_date | Date |
| Amendment Reason | amendment_reason | Text |
| Amendment Description | amendment_description | Text |
| Previous Version | previous_version | Integer |
| Current Version | current_version | Integer |
| Amendment Approved By | amendment_approved_by | User |
| Amendment Status | amendment_status | Enum |

---

# Contract Documents

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Signed Contract | signed_contract | Array |
| Commercial Annex | commercial_annex | Array |
| Technical Annex | technical_annex | Array |
| Drawings | drawings | Array |
| Specifications | specifications | Array |
| Certificates | certificates | Array |
| Amendment Files | amendment_files | Array |
| Legal Attachments | legal_attachments | Array |
| Other Documents | other_documents | Array |
---

# Risk Management

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Contract Risk Level | contract_risk_level | Enum |
| Commercial Risk | commercial_risk | Decimal |
| Legal Risk | legal_risk | Decimal |
| Financial Risk | financial_risk | Decimal |
| Technical Risk | technical_risk | Decimal |
| Delivery Risk | delivery_risk | Decimal |
| Compliance Risk | compliance_risk | Decimal |
| Overall Risk Score | overall_risk_score | Decimal |
| Risk Mitigation Plan | risk_mitigation_plan | Text |
| Risk Notes | risk_notes | Text |

---

# AI Contract Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Contract Score | ai_contract_score | Decimal |
| AI Compliance Score | ai_compliance_score | Decimal |
| AI Renewal Prediction | ai_renewal_prediction | Date |
| AI Renewal Probability | ai_renewal_probability | Decimal |
| AI Risk Prediction | ai_risk_prediction | Decimal |
| AI Clause Analysis | ai_clause_analysis | Text |
| AI Recommendation | ai_recommendation | Text |
| AI Executive Summary | ai_executive_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# KPI Metrics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Contract Utilization | contract_utilization | Decimal |
| Purchase Order Count | purchase_order_count | Integer |
| Delivery Performance | delivery_performance | Decimal |
| Invoice Performance | invoice_performance | Decimal |
| Payment Performance | payment_performance | Decimal |
| Supplier Performance | supplier_performance | Decimal |
| Compliance Index | compliance_index | Decimal |
| Amendment Count | amendment_count | Integer |
| Renewal Success Rate | renewal_success_rate | Decimal |
| Contract Savings | contract_savings | Decimal |

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
| Closed By | closed_by | User |
| Closed Date | closed_date | DateTime |
| Archived Date | archived_date | DateTime |
| Version | version | Integer |
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# Enterprise Summary

| Category | Count |
|----------|------:|
| Identity | 11 |
| Parties | 10 |
| General | 10 |
| Dates | 8 |
| Commercial | 12 |
| Financial | 10 |
| Legal | 10 |
| Duration | 6 |
| Deliverables | 10 |
| Obligations | 8 |
| Compliance | 8 |
| Amendments | 8 |
| Documents | 9 |
| Risk | 10 |
| AI | 10 |
| KPI | 10 |
| Audit | 13 |

**Total Enterprise Attributes: ~173**

---

# Long-Term Vision

The Contract entity serves as the legal and commercial governance foundation of ETA, integrating procurement, supplier management, finance, logistics, compliance, ERP, and AI into a single enterprise contract management model with complete lifecycle traceability.