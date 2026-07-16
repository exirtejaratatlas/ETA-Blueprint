---
document_id: ETA-ENT-PRODUCT-002
title: Product Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Product Attributes

## Purpose

This document defines every enterprise attribute belonging to the Product entity.

These attributes are the master definition for:

- PostgreSQL
- Odoo
- REST APIs
- AI Knowledge Graph
- Enterprise Search
- Business Intelligence

---

# Product Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Product ID | product_id | UUID |
| Product Code | product_code | String |
| Internal SKU | sku | String |
| Product Name | product_name | String |
| Product Short Name | short_name | String |
| Commercial Name | commercial_name | String |
| Technical Name | technical_name | String |
| Product Category | category | Reference |
| Product Subcategory | subcategory | Reference |
| Product Type | product_type | Enum |
| Product Family | product_family | String |
| Brand | brand | String |
| Model | model | String |
| Variant | variant | String |
| Revision | revision | String |
| Version | version | String |
| Lifecycle Status | lifecycle_status | Enum |
| Active | active | Boolean |

---

# Classification

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| UNSPSC Code | unspsc_code | String |
| HS Code | hs_code | String |
| CPC Code | cpc_code | String |
| Industry | industry | Enum |
| Segment | segment | Enum |
| Commodity Group | commodity_group | String |
| Engineering Discipline | engineering_discipline | Enum |
| Criticality | criticality | Enum |
| Strategic Item | strategic_item | Boolean |
| Spare Part | spare_part | Boolean |

---

# Manufacturer Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Primary Manufacturer | manufacturer_id | Reference |
| Manufacturer Part Number | manufacturer_part_number | String |
| OEM Code | oem_code | String |
| Country of Origin | country_of_origin | Country |
| Factory | factory | String |
| Manufacturer Brand | manufacturer_brand | String |
| Warranty Period | warranty_months | Integer |
| Lead Time | lead_time_days | Integer |
| Production Status | production_status | Enum |
| Preferred Manufacturer | preferred_manufacturer | Boolean |

---

# Technical Specifications

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Description | description | Text |
| Technical Description | technical_description | Text |
| Specification | specification | Text |
| Technical Standard | technical_standard | String |
| Material | material | String |
| Grade | grade | String |
| Size | size | String |
| Diameter | diameter | Decimal |
| Thickness | thickness | Decimal |
| Length | length | Decimal |
| Width | width | Decimal |
| Height | height | Decimal |
| Weight | weight | Decimal |
| Weight Unit | weight_unit | UOM |
| Unit of Measure | uom | UOM |
| Pressure Rating | pressure_rating | String |
| Temperature Rating | temperature_rating | String |
| Voltage | voltage | Decimal |
| Power | power | Decimal |
| Frequency | frequency | Decimal |
| Speed | speed | Decimal |
| Capacity | capacity | Decimal |
| Flow Rate | flow_rate | Decimal |
| Head | head | Decimal |
| Efficiency | efficiency | Decimal |
| Connection Type | connection_type | String |
| Mounting Type | mounting_type | String |
| Color | color | String |
| Finish | finish | String |

---

# Engineering Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Engineering Revision | engineering_revision | String |
| Drawing Number | drawing_number | String |
| GA Drawing | ga_drawing | Document |
| Datasheet | datasheet | Document |
| Manual | manual | Document |
| Test Report | test_report | Document |
| Certificate | certificate | Document |
| Engineering Notes | engineering_notes | Text |
| Interchangeable Item | interchangeable_item | Boolean |
| Custom Manufactured | custom_manufactured | Boolean |
---

# Supplier Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Primary Supplier | supplier_id | Reference |
| Alternate Suppliers | alternate_suppliers | Array |
| Supplier Part Number | supplier_part_number | String |
| Supplier Catalog Number | supplier_catalog_number | String |
| Supplier Country | supplier_country | Country |
| Authorized Distributor | authorized_distributor | Boolean |
| Supplier Status | supplier_status | Enum |
| Minimum Order Quantity | moq | Decimal |
| Supplier Lead Time | supplier_lead_time | Integer |
| Preferred Supplier | preferred_supplier | Boolean |

---

# Procurement Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Procurement Category | procurement_category | String |
| Strategic Item | strategic_item | Boolean |
| Critical Spare | critical_spare | Boolean |
| Procurement Method | procurement_method | Enum |
| Contract Required | contract_required | Boolean |
| Framework Agreement | framework_agreement | Boolean |
| Preferred Incoterm | preferred_incoterm | Enum |
| Preferred Payment Term | payment_term | Enum |
| Standard Delivery Time | standard_delivery_days | Integer |
| Procurement Notes | procurement_notes | Text |

---

# Pricing Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Standard Cost | standard_cost | Decimal |
| Currency | currency | Currency |
| Target Purchase Price | target_purchase_price | Decimal |
| Last Purchase Price | last_purchase_price | Decimal |
| Estimated Sales Price | estimated_sales_price | Decimal |
| Market Price | market_price | Decimal |
| Discount Group | discount_group | String |
| Tax Category | tax_category | String |
| Price Valid From | price_valid_from | Date |
| Price Valid Until | price_valid_until | Date |

---

# Commercial Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Export Control | export_control | Boolean |
| Country Restriction | country_restriction | Boolean |
| Sanction Sensitive | sanction_sensitive | Boolean |
| Commercial Status | commercial_status | Enum |
| Sales Region | sales_region | String |
| Availability | availability | Enum |
| Stock Policy | stock_policy | Enum |
| Commercial Notes | commercial_notes | Text |
---

# Inventory Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inventory Item | inventory_item | Boolean |
| Stock Keeping Unit | stock_keeping_unit | String |
| Warehouse | warehouse | Reference |
| Warehouse Zone | warehouse_zone | String |
| Storage Location | storage_location | String |
| Safety Stock | safety_stock | Decimal |
| Reorder Point | reorder_point | Decimal |
| Maximum Stock | maximum_stock | Decimal |
| Current Stock | current_stock | Decimal |
| Reserved Stock | reserved_stock | Decimal |
| Available Stock | available_stock | Decimal |
| Inventory Status | inventory_status | Enum |

---

# Warehouse Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Bin Location | bin_location | String |
| Shelf Number | shelf_number | String |
| Rack Number | rack_number | String |
| Storage Method | storage_method | Enum |
| Temperature Controlled | temperature_controlled | Boolean |
| Hazardous Material | hazardous_material | Boolean |
| Shelf Life | shelf_life_days | Integer |
| Expiration Tracking | expiration_tracking | Boolean |

---

# Logistics Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Package Type | package_type | String |
| Package Weight | package_weight | Decimal |
| Package Volume | package_volume | Decimal |
| Gross Weight | gross_weight | Decimal |
| Net Weight | net_weight | Decimal |
| Shipping Class | shipping_class | String |
| Country of Shipment | shipment_country | Country |
| Export Classification | export_classification | String |
| Dangerous Goods | dangerous_goods | Boolean |
| Incoterm | incoterm | Enum |
| Preferred Carrier | preferred_carrier | String |
| Logistics Notes | logistics_notes | Text |

---

# Quality Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inspection Required | inspection_required | Boolean |
| QA Status | qa_status | Enum |
| QC Status | qc_status | Enum |
| Inspection Frequency | inspection_frequency | Enum |
| Certificate Required | certificate_required | Boolean |
| Traceability Required | traceability_required | Boolean |
| Serial Number Tracking | serial_tracking | Boolean |
| Batch Tracking | batch_tracking | Boolean |

---

# AI Metadata

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Summary | ai_summary | Text |
| AI Product Score | ai_product_score | Decimal |
| AI Procurement Score | ai_procurement_score | Decimal |
| AI Risk Score | ai_risk_score | Decimal |
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
| Product Identity | 18 |
| Classification | 10 |
| Manufacturer Information | 10 |
| Technical Specifications | 30 |
| Engineering Information | 10 |
| Supplier Information | 10 |
| Procurement Information | 10 |
| Pricing Information | 10 |
| Commercial Information | 8 |
| Inventory Information | 12 |
| Warehouse Information | 8 |
| Logistics Information | 12 |
| Quality Information | 8 |
| AI Metadata | 9 |
| Enterprise Search | 5 |
| Audit Metadata | 11 |
| Integration Metadata | 6 |

**Total Enterprise Attributes: ~177**

---

# Long-Term Vision

The Product entity is the central knowledge object of the ETA Enterprise Ecosystem. It provides a unified model for engineering, procurement, inventory, logistics, finance, AI, analytics, ERP integration, and enterprise search, ensuring that every business process operates on a single authoritative product definition.