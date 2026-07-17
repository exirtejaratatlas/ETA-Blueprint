---
document_id: ETA-ENT-PO-002
title: Purchase Order Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Purchase Order Attributes

## Purpose

This document defines every enterprise attribute belonging to the Purchase Order entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Procurement
- Supply Chain
- Logistics
- Finance
- AI
- REST APIs

---

# Purchase Order Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Purchase Order ID | purchase_order_id | UUID |
| Purchase Order Number | purchase_order_number | String |
| Supplier PO Reference | supplier_po_reference | String |
| RFQ ID | rfq_id | Reference |
| Quotation ID | quotation_id | Reference |
| Contract ID | contract_id | Reference |
| Revision | revision | Integer |
| Version | version | Integer |
| Status | po_status | Enum |
| Purchase Order Type | po_type | Enum |
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
| Purchase Description | purchase_description | Text |
| Internal Notes | internal_notes | Text |
| Procurement Owner | procurement_owner | User |
| Buyer | buyer | User |
| Company | company | Company |
| Cost Center | cost_center | String |
| Profit Center | profit_center | String |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |

---

# Important Dates

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| PO Date | po_date | Date |
| Approval Date | approval_date | Date |
| Supplier Acceptance Date | supplier_acceptance_date | Date |
| Planned Delivery Date | planned_delivery_date | Date |
| Required Delivery Date | required_delivery_date | Date |
| Closing Date | closing_date | Date |
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
| Payment Method | payment_method | Enum |
| Credit Period | credit_period | Integer |
| Advance Payment Percentage | advance_payment_percentage | Decimal |
| Performance Guarantee Required | performance_guarantee_required | Boolean |
| Warranty Period | warranty_period | Integer |
| Warranty Description | warranty_description | Text |
| Commercial Notes | commercial_notes | Text |
| Contract Reference | contract_reference | String |

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
| Partial Delivery Allowed | partial_delivery_allowed | Boolean |
| Split Delivery Allowed | split_delivery_allowed | Boolean |
| Packaging Type | packaging_type | String |
| Preservation Method | preservation_method | String |
| Estimated Delivery Date | estimated_delivery_date | Date |
| Delivery Notes | delivery_notes | Text |

---

# Logistics References

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Warehouse | warehouse | Reference |
| Receiving Site | receiving_site | String |
| Shipping Address | shipping_address | Text |
| Delivery Contact | delivery_contact | String |
| Delivery Phone | delivery_phone | Phone |
---

# Product Line Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product ID | product_id | Reference |
| Product Code | product_code | String |
| Product Name | product_name | String |
| Supplier Product Code | supplier_product_code | String |
| Manufacturer Part Number | manufacturer_part_number | String |
| Ordered Quantity | ordered_quantity | Decimal |
| Unit of Measure | uom | UOM |
| Unit Weight | unit_weight | Decimal |
| Total Weight | total_weight | Decimal |
| Country of Origin | country_of_origin | Country |
| Brand | brand | String |
| Manufacturer | manufacturer | Reference |

---

# Technical Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Technical Specification | technical_specification | Text |
| Datasheet Reference | datasheet_reference | String |
| Drawing Reference | drawing_reference | String |
| Material Specification | material_specification | Text |
| Standard | standard | String |
| Revision Level | revision_level | String |
| Technical Notes | technical_notes | Text |
| Approved Manufacturer | approved_manufacturer | Boolean |
| Approved Brand | approved_brand | Boolean |
| Technical Compliance | technical_compliance | Enum |

---

# Quality Requirements

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Quality Plan Required | quality_plan_required | Boolean |
| Inspection Required | inspection_required | Boolean |
| Factory Acceptance Test | fat_required | Boolean |
| Site Acceptance Test | sat_required | Boolean |
| Third Party Inspection | third_party_inspection | Boolean |
| Inspection Agency | inspection_agency | String |
| Quality Certificates | quality_certificates | Array |
| Test Reports | test_reports | Array |
| Mill Certificates | mill_certificates | Array |
| Compliance Certificates | compliance_certificates | Array |

---

# Inspection Status

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inspection Status | inspection_status | Enum |
| Inspection Date | inspection_date | Date |
| Inspector | inspector | User |
| Inspection Result | inspection_result | Enum |
| Non-Conformance Report | ncr_reference | String |
| Inspection Notes | inspection_notes | Text |
---

# Shipment Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Shipment ID | shipment_id | Reference |
| Shipment Status | shipment_status | Enum |
| Shipment Number | shipment_number | String |
| Carrier | carrier | String |
| Tracking Number | tracking_number | String |
| Bill of Lading | bill_of_lading | String |
| Airway Bill | airway_bill | String |
| Estimated Arrival | estimated_arrival | Date |
| Actual Arrival | actual_arrival | Date |
| Shipment Notes | shipment_notes | Text |

---

# Inventory Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Warehouse Receipt | warehouse_receipt | Boolean |
| Warehouse Receipt Date | warehouse_receipt_date | Date |
| Inventory Status | inventory_status | Enum |
| Stock Location | stock_location | String |
| Quantity Received | quantity_received | Decimal |
| Quantity Remaining | quantity_remaining | Decimal |
| Inventory Notes | inventory_notes | Text |

---

# Invoice Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Invoice ID | invoice_id | Reference |
| Invoice Number | invoice_number | String |
| Invoice Date | invoice_date | Date |
| Invoice Amount | invoice_amount | Decimal |
| Invoice Currency | invoice_currency | Currency |
| Invoice Status | invoice_status | Enum |
| Invoice Attachment | invoice_attachment | Array |

---

# Payment Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Payment ID | payment_id | Reference |
| Payment Status | payment_status | Enum |
| Payment Date | payment_date | Date |
| Amount Paid | amount_paid | Decimal |
| Remaining Balance | remaining_balance | Decimal |
| Payment Method | payment_method | Enum |
| Bank Reference | bank_reference | String |
| Payment Notes | payment_notes | Text |

---

# AI Procurement Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Delivery Prediction | ai_delivery_prediction | Date |
| AI Delay Risk | ai_delay_risk | Decimal |
| AI Supplier Performance | ai_supplier_performance | Decimal |
| AI Cost Monitoring | ai_cost_monitoring | Decimal |
| AI Recommendation | ai_recommendation | Text |
| AI Procurement Summary | ai_procurement_summary | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

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
| Version | version | Integer |
| Active Flag | active_flag | Boolean |
| Deleted Flag | deleted_flag | Boolean |
| Row Version | row_version | Integer |

---

# KPI Metrics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Procurement Cycle Time | procurement_cycle_time | Integer |
| Delivery Performance | delivery_performance | Decimal |
| On-Time Delivery | on_time_delivery | Decimal |
| Cost Saving | cost_saving | Decimal |
| Supplier Performance Index | supplier_performance_index | Decimal |
| Inventory Accuracy | inventory_accuracy | Decimal |
| Payment Performance | payment_performance | Decimal |

---

# Enterprise Summary

| Category | Count |
|----------|------:|
| Identity | 12 |
| Supplier | 9 |
| General | 10 |
| Dates | 6 |
| Pricing | 12 |
| Commercial | 10 |
| Delivery | 12 |
| Product Lines | 12 |
| Technical | 10 |
| Quality | 10 |
| Inspection | 6 |
| Shipment | 10 |
| Inventory | 7 |
| Invoice | 7 |
| Payment | 8 |
| AI | 8 |
| Audit | 12 |
| KPI | 7 |

**Total Enterprise Attributes: ~168**

---

# Long-Term Vision

The Purchase Order entity becomes the operational execution backbone of ETA, connecting procurement, suppliers, logistics, inventory, finance, ERP, and AI into a single enterprise-controlled purchasing process.