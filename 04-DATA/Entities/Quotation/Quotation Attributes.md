---
document_id: ETA-ENT-QTN-002
title: Quotation Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Quotation Attributes

## Purpose

This document defines every enterprise attribute belonging to the Quotation entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- REST APIs
- Procurement
- Engineering
- AI Evaluation
- Supplier Portal
- Executive Analytics

---

# Quotation Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Quotation ID | quotation_id | UUID |
| Quotation Number | quotation_number | String |
| Supplier Quotation Number | supplier_quote_number | String |
| RFQ ID | rfq_id | Reference |
| RFQ Number | rfq_number | String |
| Revision | revision | Integer |
| Version | version | Integer |
| Status | quotation_status | Enum |
| Quotation Type | quotation_type | Enum |
| Priority | priority | Enum |
| Active | active | Boolean |

---

# Supplier Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Supplier ID | supplier_id | Reference |
| Supplier Name | supplier_name | String |
| Manufacturer ID | manufacturer_id | Reference |
| Manufacturer Name | manufacturer_name | String |
| Sales Contact | sales_contact | Reference |
| Contact Email | contact_email | Email |
| Contact Phone | contact_phone | Phone |
| Supplier Country | supplier_country | Country |
| Supplier Rating | supplier_rating | Decimal |

---

# General Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Subject | subject | String |
| Commercial Proposal | commercial_proposal | Text |
| Technical Proposal | technical_proposal | Text |
| Executive Summary | executive_summary | Text |
| Proposal Notes | proposal_notes | Text |
| Internal Notes | internal_notes | Text |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Proposal Language | proposal_language | String |
| Prepared By | prepared_by | User |

---

# Important Dates

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Submission Date | submission_date | DateTime |
| Valid Until | valid_until | Date |
| Delivery Start | delivery_start | Date |
| Delivery Completion | delivery_completion | Date |
| Evaluation Date | evaluation_date | Date |
| Award Date | award_date | Date |
---

# Pricing Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Unit Price | unit_price | Decimal |
| Total Price | total_price | Decimal |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Discount Percentage | discount_percentage | Decimal |
| Discount Amount | discount_amount | Decimal |
| Tax Amount | tax_amount | Decimal |
| Freight Cost | freight_cost | Decimal |
| Insurance Cost | insurance_cost | Decimal |
| Packing Cost | packing_cost | Decimal |
| Other Charges | other_charges | Decimal |
| Grand Total | grand_total | Decimal |

---

# Commercial Terms

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Incoterm | incoterm | Enum |
| Payment Terms | payment_terms | Enum |
| Credit Period | credit_period | Integer |
| Validity Period | validity_period | Integer |
| Partial Delivery Allowed | partial_delivery_allowed | Boolean |
| Split Delivery Allowed | split_delivery_allowed | Boolean |
| Warranty Period | warranty_period | Integer |
| Warranty Description | warranty_description | Text |
| Performance Guarantee | performance_guarantee | Boolean |
| Commercial Exceptions | commercial_exceptions | Text |

---

# Delivery Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Manufacturing Lead Time | manufacturing_lead_time | Integer |
| Shipping Lead Time | shipping_lead_time | Integer |
| Total Lead Time | total_lead_time | Integer |
| Delivery Location | delivery_location | String |
| Delivery Method | delivery_method | Enum |
| Shipment Type | shipment_type | Enum |
| Packaging Type | packaging_type | String |
| Preservation Method | preservation_method | String |
| Estimated Delivery Date | estimated_delivery_date | Date |
| Delivery Notes | delivery_notes | Text |
---

# Product Line Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product ID | product_id | Reference |
| Product Code | product_code | String |
| Product Name | product_name | String |
| Supplier Product Code | supplier_product_code | String |
| Manufacturer Part Number | manufacturer_part_number | String |
| Offered Quantity | offered_quantity | Decimal |
| Unit of Measure | uom | UOM |
| Country of Origin | country_of_origin | Country |
| Brand | brand | String |
| Manufacturer | manufacturer | Reference |

---

# Technical Compliance

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Technical Compliance | technical_compliance | Enum |
| Compliance Percentage | compliance_percentage | Decimal |
| Datasheet Attached | datasheet_attached | Boolean |
| GA Drawing Attached | ga_drawing_attached | Boolean |
| Certificates Attached | certificates_attached | Boolean |
| Standards Compliance | standards_compliance | Text |
| Material Compliance | material_compliance | Text |
| Inspection Requirement Accepted | inspection_requirement | Boolean |
| Testing Requirement Accepted | testing_requirement | Boolean |
| Technical Exceptions | technical_exceptions | Text |

---

# Engineering Evaluation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Engineering Status | engineering_status | Enum |
| Engineering Score | engineering_score | Decimal |
| Technical Reviewer | technical_reviewer | User |
| Technical Review Date | technical_review_date | DateTime |
| Technical Comments | technical_comments | Text |
| Clarification Required | clarification_required | Boolean |
| Clarification Status | clarification_status | Enum |
| Engineering Approval | engineering_approval | Boolean |
| Approved Revision | approved_revision | String |
| Technical Risk Level | technical_risk_level | Enum |

---

# Documentation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Commercial Attachment | commercial_attachment | Array |
| Technical Attachment | technical_attachment | Array |
| Datasheet | datasheet | Array |
| Drawings | drawings | Array |
| Certificates | certificates | Array |
| Packing List | packing_list | Array |
| Inspection Documents | inspection_documents | Array |
| Other Attachments | other_attachments | Array |
---

# Commercial Evaluation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Commercial Score | commercial_score | Decimal |
| Price Score | price_score | Decimal |
| Delivery Score | delivery_score | Decimal |
| Warranty Score | warranty_score | Decimal |
| Payment Terms Score | payment_terms_score | Decimal |
| Supplier Performance Score | supplier_performance_score | Decimal |
| Overall Evaluation Score | overall_evaluation_score | Decimal |
| Evaluation Status | evaluation_status | Enum |
| Evaluation Comments | evaluation_comments | Text |

---

# Negotiation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Negotiation Required | negotiation_required | Boolean |
| Negotiation Round | negotiation_round | Integer |
| Negotiation Status | negotiation_status | Enum |
| Negotiation Date | negotiation_date | DateTime |
| Negotiated Price | negotiated_price | Decimal |
| Negotiated Delivery | negotiated_delivery | Integer |
| Negotiated Payment Terms | negotiated_payment_terms | String |
| Negotiation Notes | negotiation_notes | Text |

---

# AI Procurement Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Ranking | ai_ranking | Integer |
| AI Supplier Score | ai_supplier_score | Decimal |
| AI Cost Benchmark | ai_cost_benchmark | Decimal |
| AI Lead Time Prediction | ai_lead_time_prediction | Integer |
| AI Risk Score | ai_risk_score | Decimal |
| AI Recommendation | ai_recommendation | Text |
| AI Alternative Supplier | ai_alternative_supplier | Array |
| AI Alternative Product | ai_alternative_product | Array |
| AI Summary | ai_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# Award Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Award Status | award_status | Enum |
| Award Decision | award_decision | Enum |
| Award Date | award_date | Date |
| Awarded By | awarded_by | User |
| Purchase Order ID | purchase_order_id | Reference |
| Contract ID | contract_id | Reference |

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
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# KPI Metrics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Procurement Saving | procurement_saving | Decimal |
| Supplier Response Time | supplier_response_time | Integer |
| Evaluation Duration | evaluation_duration | Integer |
| Negotiation Duration | negotiation_duration | Integer |
| Award Duration | award_duration | Integer |
| AI Accuracy | ai_accuracy | Decimal |
| Procurement Efficiency | procurement_efficiency | Decimal |

---

# Enterprise Summary

Approximate Attribute Count

| Category | Count |
|----------|------:|
| Identity | 11 |
| Supplier | 9 |
| General | 10 |
| Dates | 6 |
| Pricing | 12 |
| Commercial | 10 |
| Delivery | 10 |
| Product Lines | 10 |
| Technical | 10 |
| Engineering | 10 |
| Documents | 8 |
| Commercial Evaluation | 9 |
| Negotiation | 8 |
| AI | 11 |
| Award | 6 |
| Audit | 10 |
| KPI | 7 |

**Total Enterprise Attributes: ~167**

---

# Long-Term Vision

The Quotation entity serves as the enterprise procurement decision engine of ETA, combining supplier proposals, engineering validation, commercial evaluation, AI-assisted scoring, negotiation history, and purchasing decisions into a single authoritative procurement record.