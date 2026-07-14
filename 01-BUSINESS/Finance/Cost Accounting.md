---
document_id: ETA-BUS-FIN-013
title: Cost Accounting
version: 1.0
status: Approved
owner: Exir Tejarat Atlas
website: https://exiratlas.com
classification: Internal
domain: Finance, Accounting, Tax & Compliance
last_updated: 2026
depends_on:
  - Chart of Accounts Strategy
  - Budget & Forecasting
  - Cash Flow Management
---

# Cost Accounting

# Purpose

This document defines the Enterprise Cost Accounting framework for the ETA Enterprise Business Operating System.

ETA operates as a B2B trading company specializing in:

- Oil & Gas Equipment
- Petrochemical Equipment
- Rotating Equipment
- Static Equipment
- Steel Products
- Industrial Procurement
- Import
- Export
- EPC Projects

The Cost Accounting framework provides complete visibility into the actual cost and profitability of every transaction.

---

# Objectives

The framework aims to:

- Calculate true procurement cost
- Measure project profitability
- Allocate indirect costs
- Support pricing decisions
- Improve procurement optimization
- Enable AI-driven cost analysis
- Support executive decision-making

---

# Cost Categories

## Direct Costs

Include:

- Purchase Price
- Freight
- Customs Duties
- Insurance
- Inspection
- Packaging
- Transportation
- Installation
- Commission

---

## Indirect Costs

Include:

- Administration
- Finance
- Marketing
- IT
- Office Expenses
- Management
- Utilities

---

## Financial Costs

Include:

- Bank Charges
- LC Costs
- TT Charges
- Financing Cost
- Exchange Loss
- Guarantee Fees

---

## Tax Costs

Include:

- VAT (when non-recoverable)
- Customs Taxes
- Import Duties
- Withholding Taxes

---

# Cost Objects

ETA allocates costs to:

- Customer
- Supplier
- Product
- Product Family
- Project
- Contract
- Purchase Order
- Sales Order
- Business Unit

---

# Cost Centers

Supported Cost Centers:

- Procurement
- Sales
- Finance
- Engineering
- Projects
- Logistics
- Administration
- Marketing
- AI Platform
- IT

---

# Cost Allocation

Indirect costs may be allocated using:

- Revenue
- Purchase Value
- Labor Hours
- Project Hours
- Weight
- Quantity
- Volume
- Fixed Percentage
- Custom Formula

---

# Landed Cost

For imported goods ETA calculates:

Purchase Price

+

International Freight

+

Insurance

+

Customs Duties

+

Port Charges

+

Customs Clearance

+

Domestic Transportation

+

Inspection

=

Landed Cost

---

# Product Cost

Each product stores:

- Purchase Cost
- Landed Cost
- Inventory Cost
- Selling Price
- Gross Margin
- Net Margin
- Cost History

---

# Project Cost

Projects track:

- Procurement Cost
- Logistics Cost
- Engineering Cost
- Financial Cost
- Tax Cost
- External Services
- Internal Labor

---

# Contract Cost

Each contract contains:

- Contract Value
- Procurement Cost
- Operating Cost
- Financial Cost
- Tax Cost
- Margin

---

# Customer Cost Analysis

The system measures:

- Revenue
- Direct Cost
- Indirect Cost
- Gross Profit
- Net Profit
- Lifetime Profitability

---

# Supplier Cost Analysis

Tracks:

- Purchase Volume
- Logistics Cost
- Customs Cost
- Payment Cost
- Financial Cost
- Total Procurement Cost

---

# Profitability Analysis

ETA calculates:

Gross Profit

=

Revenue

-

Direct Cost

---

Operating Profit

=

Gross Profit

-

Operating Expenses

---

Net Profit

=

Operating Profit

-

Financial Costs

-

Taxes

---

# AI Cost Analysis

The AI Cost Agent performs:

- Cost anomaly detection
- Supplier comparison
- Landed cost optimization
- Margin prediction
- Cost forecasting
- Procurement optimization
- Project profitability prediction

---

# Dashboards

Executive Dashboard

- Gross Margin
- Net Margin
- Product Margin
- Customer Profitability
- Supplier Profitability
- Project Margin
- Landed Cost Analysis
- Cost Trend

Procurement Dashboard

- Purchase Cost
- Freight Cost
- Customs Cost
- Supplier Cost Ranking

Project Dashboard

- Budget
- Actual Cost
- Margin
- Cost Breakdown

---

# KPIs

- Gross Margin %
- Net Margin %
- Landed Cost Accuracy
- Procurement Cost Variance
- Project Cost Variance
- Product Profitability
- Customer Profitability
- Supplier Profitability
- Cost Allocation Accuracy
- Cost per Purchase Order

---

# Business Rules

Example:

IF

Actual Procurement Cost >

Approved Budget

THEN

Notify Procurement Manager

AND

Notify Finance

---

IF

Gross Margin < Minimum Margin

THEN

Require Executive Approval

---

IF

Supplier Cost Increased > 10%

THEN

Trigger Supplier Review

---

# Integration

Cost Accounting integrates with:

- Procurement
- CRM
- Inventory
- Logistics
- Treasury
- Accounting
- Projects
- Contracts
- AI Platform
- Business Rules Engine
- Odoo ERP
- Microsoft Dynamics CRM

---

# Future Enhancements

Future releases will include:

- Activity-Based Costing (ABC)
- Standard Costing
- Predictive Cost Optimization
- AI Cost Copilot
- ESG Cost Allocation
- Multi-company Cost Consolidation
- Real-Time Margin Simulation