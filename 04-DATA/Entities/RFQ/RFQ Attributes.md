---
document_id: ETA-ENT-RFQ-002
title: RFQ Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# RFQ Attributes

## Purpose

This document defines every enterprise attribute belonging to the RFQ entity.

These attributes serve as the authoritative definition for:

- PostgreSQL
- Odoo Enterprise
- REST APIs
- AI Procurement
- Analytics
- Procurement Workflow

---

# RFQ Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| RFQ ID | rfq_id | UUID |
| RFQ Number | rfq_number | String |
| Customer RFQ Number | customer_rfq_number | String |
| Internal Reference | internal_reference | String |
| Opportunity ID | opportunity_id | UUID |
| Project ID | project_id | UUID |
| RFQ Type | rfq_type | Enum |
| RFQ Status | rfq_status | Enum |
| Priority | priority | Enum |
| Revision | revision | Integer |
| Version | version | Integer |
| Active | active | Boolean |

---

# Customer Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Customer ID | customer_id | Reference |
| Customer Name | customer_name | String |
| End User | end_user | String |
| Consultant | consultant | String |
| EPC Contractor | epc_contractor | String |
| Customer Contact | customer_contact | Reference |
| Customer Email | customer_email | Email |
| Customer Phone | customer_phone | Phone |

---

# General Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| RFQ Title | rfq_title | String |
| Subject | subject | String |
| Description | description | Text |
| Scope of Supply | scope_of_supply | Text |
| Industry | industry | Enum |
| Business Unit | business_unit | String |
| Company | company | Company |
| Procurement Owner | procurement_owner | User |
| Engineering Owner | engineering_owner | User |

---

# Schedule

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| RFQ Date | rfq_date | Date |
| Submission Deadline | submission_deadline | DateTime |
| Customer Deadline | customer_deadline | DateTime |
| Required Delivery Date | required_delivery_date | Date |
| Expected Award Date | expected_award_date | Date |
| RFQ Valid Until | valid_until | Date |
---

# Product Lines

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product ID | product_id | Reference |
| Product Code | product_code | String |
| Product Name | product_name | String |
| Line Number | line_number | Integer |
| Quantity | quantity | Decimal |
| Unit of Measure | uom | UOM |
| Estimated Budget | estimated_budget | Decimal |
| Currency | currency | Currency |
| Preferred Manufacturer | preferred_manufacturer | Reference |
| Preferred Supplier | preferred_supplier | Reference |
| Alternative Manufacturer | alternative_manufacturer | Array |
| Alternative Supplier | alternative_supplier | Array |

---

# Technical Requirements

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Technical Specification | technical_specification | Text |
| Datasheet Required | datasheet_required | Boolean |
| GA Drawing Required | ga_required | Boolean |
| Material Requirement | material_requirement | String |
| Standard Requirement | standard_requirement | String |
| Inspection Requirement | inspection_required | Boolean |
| Test Requirement | test_required | Boolean |
| Certification Requirement | certification_required | Boolean |
| Warranty Requirement | warranty_requirement | String |
| Packing Requirement | packing_requirement | Text |
| Preservation Requirement | preservation_requirement | Text |
| Tagging Requirement | tagging_requirement | Text |

---

# Engineering Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Engineering Review Status | engineering_review_status | Enum |
| Engineering Approval | engineering_approval | Boolean |
| Engineering Notes | engineering_notes | Text |
| Technical Risk Level | technical_risk_level | Enum |
| Approved Revision | approved_revision | String |
| Engineering Documents | engineering_documents | Array |
| Datasheet Version | datasheet_version | String |
| Drawing Revision | drawing_revision | String |
| Engineering Completion Date | engineering_completion_date | DateTime |
---

# Supplier Selection

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invited Suppliers | invited_suppliers | Array |
| Approved Suppliers | approved_suppliers | Array |
| Supplier Count | supplier_count | Integer |
| Preferred Supplier | preferred_supplier | Reference |
| Supplier Response Count | supplier_response_count | Integer |
| Non-Responsive Suppliers | non_responsive_suppliers | Array |
| Winning Supplier | winning_supplier | Reference |
| Supplier Recommendation | supplier_recommendation | Text |

---

# Commercial Terms

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Incoterm | incoterm | Enum |
| Delivery Location | delivery_location | String |
| Delivery Address | delivery_address | Text |
| Payment Terms | payment_terms | Enum |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Validity Period | validity_period | Integer |
| Delivery Requirement | delivery_requirement | Text |
| Partial Delivery Allowed | partial_delivery_allowed | Boolean |
| Split Award Allowed | split_award_allowed | Boolean |
| Commercial Notes | commercial_notes | Text |

---

# Procurement Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Procurement Category | procurement_category | String |
| Strategic Procurement | strategic_procurement | Boolean |
| Emergency Procurement | emergency_procurement | Boolean |
| Competitive Bidding | competitive_bidding | Boolean |
| Single Source | single_source | Boolean |
| Budget Approved | budget_approved | Boolean |
| Budget Amount | budget_amount | Decimal |
| Cost Center | cost_center | String |
| Profit Center | profit_center | String |
| Buyer | buyer | User |
| Procurement Manager | procurement_manager | User |
| Procurement Notes | procurement_notes | Text |

---

# Compliance

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Compliance Review | compliance_review | Boolean |
| Export Control | export_control | Boolean |
| Sanction Screening | sanction_screening | Boolean |
| Country Restrictions | country_restrictions | Array |
| Compliance Status | compliance_status | Enum |
| Compliance Notes | compliance_notes | Text |
---

# Quotation Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Quotation Count | quotation_count | Integer |
| Lowest Price | lowest_price | Decimal |
| Highest Price | highest_price | Decimal |
| Average Price | average_price | Decimal |
| Selected Quotation | selected_quotation | Reference |
| Award Recommendation | award_recommendation | Text |
| Commercial Evaluation Score | commercial_score | Decimal |
| Technical Evaluation Score | technical_score | Decimal |
| Final Evaluation Score | final_score | Decimal |
| Evaluation Status | evaluation_status | Enum |

---

# AI Procurement

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Supplier Recommendation | ai_supplier_recommendation | Text |
| AI Manufacturer Recommendation | ai_manufacturer_recommendation | Text |
| AI Alternative Products | ai_alternative_products | Array |
| AI Cost Estimation | ai_cost_estimation | Decimal |
| AI Lead Time Prediction | ai_lead_time_prediction | Integer |
| AI Risk Score | ai_risk_score | Decimal |
| AI Procurement Score | ai_procurement_score | Decimal |
| AI Summary | ai_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# Workflow Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Current Workflow Step | workflow_step | String |
| Workflow Status | workflow_status | Enum |
| Pending Approval | pending_approval | Boolean |
| Current Approver | current_approver | User |
| Approval Level | approval_level | Integer |
| Approval Deadline | approval_deadline | DateTime |
| Final Approval Date | final_approval_date | DateTime |

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