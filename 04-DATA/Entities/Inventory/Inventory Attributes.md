---
document_id: ETA-ENT-INV-002
title: Inventory Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Inventory Attributes

## Purpose

This document defines every enterprise attribute belonging to the Inventory entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Warehouse
- Procurement
- Logistics
- Finance
- ERP
- AI
- REST APIs

---

# Inventory Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inventory ID | inventory_id | UUID |
| Inventory Number | inventory_number | String |
| SKU | sku | String |
| Product ID | product_id | Reference |
| Product Code | product_code | String |
| Product Name | product_name | String |
| Product Category | product_category | Enum |
| Inventory Type | inventory_type | Enum |
| Inventory Status | inventory_status | Enum |
| Priority | priority | Enum |
| Active | active | Boolean |

---

# Warehouse Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Warehouse ID | warehouse_id | Reference |
| Warehouse Code | warehouse_code | String |
| Warehouse Name | warehouse_name | String |
| Storage Location | storage_location | String |
| Bin Location | bin_location | String |
| Zone | zone | String |
| Aisle | aisle | String |
| Rack | rack | String |
| Shelf | shelf | String |
| Position | position | String |

---

# Stock Quantities

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| On Hand Quantity | on_hand_quantity | Decimal |
| Available Quantity | available_quantity | Decimal |
| Reserved Quantity | reserved_quantity | Decimal |
| Allocated Quantity | allocated_quantity | Decimal |
| Incoming Quantity | incoming_quantity | Decimal |
| Outgoing Quantity | outgoing_quantity | Decimal |
| Damaged Quantity | damaged_quantity | Decimal |
| Quarantine Quantity | quarantine_quantity | Decimal |
| Safety Stock Quantity | safety_stock_quantity | Decimal |
| Reorder Quantity | reorder_quantity | Decimal |

---

# Units of Measure

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Base UOM | base_uom | UOM |
| Purchase UOM | purchase_uom | UOM |
| Sales UOM | sales_uom | UOM |
| Inventory UOM | inventory_uom | UOM |
| Conversion Factor | conversion_factor | Decimal |
---

# Batch Management

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Batch Number | batch_number | String |
| Batch Status | batch_status | Enum |
| Batch Quantity | batch_quantity | Decimal |
| Batch Creation Date | batch_creation_date | Date |
| Manufacturing Date | manufacturing_date | Date |
| Production Line | production_line | String |
| Supplier Batch Number | supplier_batch_number | String |
| Internal Batch Number | internal_batch_number | String |

---

# Lot Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Lot Number | lot_number | String |
| Lot Status | lot_status | Enum |
| Lot Quantity | lot_quantity | Decimal |
| Lot Owner | lot_owner | String |
| Lot Notes | lot_notes | Text |

---

# Serial Number Management

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Serial Number | serial_number | String |
| Serial Status | serial_status | Enum |
| Asset Tag | asset_tag | String |
| Equipment Number | equipment_number | String |
| IMEI / Device ID | device_identifier | String |
| QR Code | qr_code | String |
| RFID Tag | rfid_tag | String |

---

# Expiration & Shelf Life

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Expiration Date | expiration_date | Date |
| Shelf Life | shelf_life | Integer |
| Remaining Shelf Life | remaining_shelf_life | Integer |
| Best Before Date | best_before_date | Date |
| Inspection Due Date | inspection_due_date | Date |
| Calibration Due Date | calibration_due_date | Date |

---

# Traceability

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Shipment ID | shipment_id | Reference |
| Purchase Order ID | purchase_order_id | Reference |
| Supplier ID | supplier_id | Reference |
| Manufacturer ID | manufacturer_id | Reference |
| Contract ID | contract_id | Reference |
| Country of Origin | country_of_origin | Country |
| Certificate Number | certificate_number | String |
| Traceability Status | traceability_status | Enum |
| Full Traceability | full_traceability | Boolean |
| Traceability Notes | traceability_notes | Text |

---

# Quality Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Quality Status | quality_status | Enum |
| Inspection Result | inspection_result | Enum |
| Inspection Date | inspection_date | Date |
| Inspector | inspector | User |
| NCR Number | ncr_number | String |
| Quality Remarks | quality_remarks | Text |
---

# Inventory Valuation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Costing Method | costing_method | Enum |
| Unit Cost | unit_cost | Decimal |
| Average Cost | average_cost | Decimal |
| Standard Cost | standard_cost | Decimal |
| FIFO Cost | fifo_cost | Decimal |
| Last Purchase Cost | last_purchase_cost | Decimal |
| Inventory Value | inventory_value | Decimal |
| Currency | currency | Currency |
| Exchange Rate | exchange_rate | Decimal |
| Valuation Date | valuation_date | Date |

---

# Stock Movement

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Movement ID | movement_id | UUID |
| Movement Type | movement_type | Enum |
| Movement Date | movement_date | DateTime |
| Source Warehouse | source_warehouse | Reference |
| Destination Warehouse | destination_warehouse | Reference |
| Source Location | source_location | String |
| Destination Location | destination_location | String |
| Quantity Moved | quantity_moved | Decimal |
| Movement Reason | movement_reason | Enum |
| Movement Reference | movement_reference | String |

---

# Reservation

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Reservation ID | reservation_id | UUID |
| Reservation Status | reservation_status | Enum |
| Reserved For | reserved_for | Reference |
| Reservation Date | reservation_date | DateTime |
| Reserved Quantity | reserved_quantity | Decimal |
| Allocation Date | allocation_date | DateTime |
| Release Date | release_date | DateTime |
| Reservation Notes | reservation_notes | Text |

---

# Replenishment

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Reorder Point | reorder_point | Decimal |
| Safety Stock | safety_stock | Decimal |
| Minimum Stock | minimum_stock | Decimal |
| Maximum Stock | maximum_stock | Decimal |
| Economic Order Quantity | economic_order_quantity | Decimal |
| Lead Time | lead_time | Integer |
| Replenishment Method | replenishment_method | Enum |
| Replenishment Status | replenishment_status | Enum |
| Next Replenishment Date | next_replenishment_date | Date |
| Preferred Supplier | preferred_supplier | Reference |

---

# Warehouse Operations

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Put Away Strategy | putaway_strategy | Enum |
| Picking Strategy | picking_strategy | Enum |
| Cycle Count Required | cycle_count_required | Boolean |
| Last Cycle Count | last_cycle_count | Date |
| Next Cycle Count | next_cycle_count | Date |
| Warehouse Remarks | warehouse_remarks | Text |
---

# Inventory Documents

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Receiving Documents | receiving_documents | Array |
| Inspection Reports | inspection_reports | Array |
| Quality Certificates | quality_certificates | Array |
| Packing List | packing_list | Array |
| Batch Certificates | batch_certificates | Array |
| Calibration Certificates | calibration_certificates | Array |
| Inventory Attachments | inventory_attachments | Array |
| Other Documents | other_documents | Array |

---

# AI Inventory Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI Demand Forecast | ai_demand_forecast | Decimal |
| AI Reorder Prediction | ai_reorder_prediction | Date |
| AI Inventory Score | ai_inventory_score | Decimal |
| AI Overstock Risk | ai_overstock_risk | Decimal |
| AI Stockout Risk | ai_stockout_risk | Decimal |
| AI Slow Moving Score | ai_slow_moving_score | Decimal |
| AI Dead Stock Score | ai_dead_stock_score | Decimal |
| AI Warehouse Recommendation | ai_warehouse_recommendation | Text |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# KPI Metrics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inventory Turnover | inventory_turnover | Decimal |
| Stock Accuracy | stock_accuracy | Decimal |
| Warehouse Utilization | warehouse_utilization | Decimal |
| Fill Rate | fill_rate | Decimal |
| Average Inventory | average_inventory | Decimal |
| Days of Inventory | days_of_inventory | Decimal |
| Inventory Carrying Cost | inventory_carrying_cost | Decimal |
| Cycle Count Accuracy | cycle_count_accuracy | Decimal |
| Inventory Availability KPI | inventory_availability_kpi | Decimal |
| Warehouse Performance KPI | warehouse_performance_kpi | Decimal |

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
| Last Counted By | last_counted_by | User |
| Last Count Date | last_count_date | DateTime |
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
| Warehouse | 10 |
| Stock Quantities | 10 |
| Units of Measure | 5 |
| Batch | 8 |
| Lot | 5 |
| Serial Numbers | 7 |
| Expiration | 6 |
| Traceability | 10 |
| Quality | 6 |
| Valuation | 10 |
| Stock Movement | 10 |
| Reservation | 8 |
| Replenishment | 10 |
| Warehouse Operations | 6 |
| Documents | 8 |
| AI | 10 |
| KPI | 10 |
| Audit | 13 |

**Total Enterprise Attributes: ~173**

---

# Long-Term Vision

The Inventory entity provides the operational inventory backbone of ETA by integrating procurement, warehouse management, logistics, valuation, finance, ERP, AI forecasting, and complete inventory traceability across the enterprise ecosystem.