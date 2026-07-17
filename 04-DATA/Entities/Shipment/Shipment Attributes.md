---
document_id: ETA-ENT-SHP-002
title: Shipment Attributes
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
classification: Internal
last_updated: 2026
---

# Shipment Attributes

## Purpose

This document defines every enterprise attribute belonging to the Shipment entity.

These attributes are the authoritative source for:

- PostgreSQL
- Odoo Enterprise
- Logistics
- Procurement
- Warehouse
- Finance
- ERP
- AI
- REST APIs

---

# Shipment Identity

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Shipment ID | shipment_id | UUID |
| Shipment Number | shipment_number | String |
| Tracking Number | tracking_number | String |
| Bill of Lading | bill_of_lading | String |
| Air Waybill | air_waybill | String |
| Container Number | container_number | String |
| Customs Declaration Number | customs_declaration_number | String |
| Shipment Type | shipment_type | Enum |
| Shipment Status | shipment_status | Enum |
| Priority | priority | Enum |
| Active | active | Boolean |

---

# Shipment Header

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Purchase Order ID | purchase_order_id | Reference |
| Contract ID | contract_id | Reference |
| Supplier ID | supplier_id | Reference |
| Manufacturer ID | manufacturer_id | Reference |
| Company | company | Company |
| Business Unit | business_unit | String |
| Shipment Owner | shipment_owner | User |
| Logistics Coordinator | logistics_coordinator | User |
| Carrier | carrier | String |
| Freight Forwarder | freight_forwarder | String |

---

# Transportation Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Transport Mode | transport_mode | Enum |
| Incoterm | incoterm | Enum |
| Origin Country | origin_country | Country |
| Origin Port | origin_port | String |
| Loading Port | loading_port | String |
| Destination Country | destination_country | Country |
| Destination Port | destination_port | String |
| Final Delivery Location | final_delivery_location | String |
| Warehouse | warehouse | Reference |
| Route Description | route_description | Text |

---

# Shipment Dates

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Booking Date | booking_date | Date |
| Dispatch Date | dispatch_date | Date |
| Estimated Departure | estimated_departure | DateTime |
| Actual Departure | actual_departure | DateTime |
| Estimated Arrival | estimated_arrival | DateTime |
| Actual Arrival | actual_arrival | DateTime |
| Customs Clearance Date | customs_clearance_date | Date |
| Receiving Date | receiving_date | Date |
---

# Cargo Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Cargo Description | cargo_description | Text |
| Cargo Category | cargo_category | Enum |
| Product Count | product_count | Integer |
| Total Quantity | total_quantity | Decimal |
| Total Weight | total_weight | Decimal |
| Net Weight | net_weight | Decimal |
| Gross Weight | gross_weight | Decimal |
| Total Volume | total_volume | Decimal |
| Dangerous Goods | dangerous_goods | Boolean |
| Hazard Class | hazard_class | String |

---

# Container Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Container Type | container_type | Enum |
| Container Size | container_size | Enum |
| Number of Containers | container_count | Integer |
| Seal Number | seal_number | String |
| Container Owner | container_owner | String |
| Container Status | container_status | Enum |
| Refrigerated | refrigerated | Boolean |
| Temperature Requirement | temperature_requirement | Decimal |

---

# Packaging

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Package Type | package_type | Enum |
| Number of Packages | package_count | Integer |
| Packaging Standard | packaging_standard | String |
| Pallet Count | pallet_count | Integer |
| Crate Count | crate_count | Integer |
| Wooden Packaging | wooden_packaging | Boolean |
| Export Packaging | export_packaging | Boolean |
| Packaging Notes | packaging_notes | Text |

---

# Tracking Events

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Current Location | current_location | String |
| Current Country | current_country | Country |
| Tracking Status | tracking_status | Enum |
| Last Tracking Update | last_tracking_update | DateTime |
| GPS Latitude | gps_latitude | Decimal |
| GPS Longitude | gps_longitude | Decimal |
| Delay Days | delay_days | Integer |
| Delay Reason | delay_reason | Text |
| Last Event | last_event | String |
| Next Milestone | next_milestone | String |

---

# Carrier Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Carrier Name | carrier_name | String |
| Carrier Reference | carrier_reference | String |
| Vessel Name | vessel_name | String |
| Voyage Number | voyage_number | String |
| Flight Number | flight_number | String |
| Truck Number | truck_number | String |
| Driver Name | driver_name | String |
| Driver Contact | driver_contact | String |
---

# Customs Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Customs Broker | customs_broker | String |
| Customs Office | customs_office | String |
| Customs Status | customs_status | Enum |
| Customs Clearance Number | customs_clearance_number | String |
| Customs Clearance Date | customs_clearance_date | Date |
| Import License | import_license | String |
| Export License | export_license | String |
| Duties Amount | duties_amount | Decimal |
| Customs Fees | customs_fees | Decimal |
| Customs Notes | customs_notes | Text |

---

# Receiving Information

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Receiving Warehouse | receiving_warehouse | Reference |
| Receiving Status | receiving_status | Enum |
| Receiving User | receiving_user | User |
| Receiving Date | receiving_date | DateTime |
| Received Quantity | received_quantity | Decimal |
| Accepted Quantity | accepted_quantity | Decimal |
| Rejected Quantity | rejected_quantity | Decimal |
| Inspection Required | inspection_required | Boolean |
| Inspection Status | inspection_status | Enum |
| Receiving Notes | receiving_notes | Text |

---

# Inventory Integration

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Inventory Transaction | inventory_transaction | Reference |
| Inventory Status | inventory_status | Enum |
| Warehouse Location | warehouse_location | String |
| Batch Number | batch_number | String |
| Serial Numbers | serial_numbers | Array |
| Stock Updated | stock_updated | Boolean |
| Inventory Posting Date | inventory_posting_date | Date |
| Inventory Notes | inventory_notes | Text |

---

# Shipment Cost

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Freight Cost | freight_cost | Decimal |
| Insurance Cost | insurance_cost | Decimal |
| Customs Cost | customs_cost | Decimal |
| Handling Cost | handling_cost | Decimal |
| Transportation Cost | transportation_cost | Decimal |
| Other Cost | other_cost | Decimal |
| Total Shipment Cost | total_shipment_cost | Decimal |
| Currency | currency | Currency |

---

# Shipment Documents

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Bill of Lading File | bill_of_lading_file | Array |
| Air Waybill File | air_waybill_file | Array |
| Packing List | packing_list | Array |
| Commercial Invoice | commercial_invoice | Array |
| Certificate of Origin | certificate_of_origin | Array |
| Inspection Certificate | inspection_certificate | Array |
| Insurance Certificate | insurance_certificate | Array |
| Customs Documents | customs_documents | Array |
| Delivery Note | delivery_note | Array |
| Other Attachments | other_attachments | Array |
---

# AI Logistics Intelligence

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| AI ETA Prediction | ai_eta_prediction | DateTime |
| AI Delay Probability | ai_delay_probability | Decimal |
| AI Carrier Score | ai_carrier_score | Decimal |
| AI Customs Risk | ai_customs_risk | Decimal |
| AI Route Optimization | ai_route_optimization | Text |
| AI Logistics Recommendation | ai_logistics_recommendation | Text |
| AI Shipment Summary | ai_shipment_summary | Text |
| AI Risk Score | ai_risk_score | Decimal |
| Embedding ID | embedding_id | UUID |
| Knowledge Graph Node | knowledge_graph_node | UUID |

---

# KPI Metrics

| Business Name | Technical Name | Type |
|---------------|---------------|------|
| Transit Time | transit_time | Integer |
| Delivery Performance | delivery_performance | Decimal |
| On-Time Delivery | on_time_delivery | Boolean |
| Customs Clearance Duration | customs_clearance_duration | Integer |
| Receiving Duration | receiving_duration | Integer |
| Inventory Posting Duration | inventory_posting_duration | Integer |
| Damage Rate | damage_rate | Decimal |
| Delay Frequency | delay_frequency | Decimal |
| Logistics Cost KPI | logistics_cost_kpi | Decimal |
| Carrier Performance KPI | carrier_performance_kpi | Decimal |

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
| Shipment Header | 10 |
| Transportation | 10 |
| Dates | 8 |
| Cargo | 10 |
| Containers | 8 |
| Packaging | 8 |
| Tracking | 10 |
| Carrier | 8 |
| Customs | 10 |
| Receiving | 10 |
| Inventory | 8 |
| Cost | 8 |
| Documents | 10 |
| AI | 10 |
| KPI | 10 |
| Audit | 13 |

**Total Enterprise Attributes: ~172**

---

# Long-Term Vision

The Shipment entity provides the operational logistics backbone of ETA by integrating transportation, customs, warehouse receiving, inventory synchronization, ERP, finance, AI logistics intelligence, and complete end-to-end shipment traceability across the enterprise procurement ecosystem.