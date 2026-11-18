# Pharmaceutical Stock Management & Supply Chain Analytics Dashboard

[![Excel Version](https://img.shields.io/badge/Excel-365%2F2021-green.svg)](https://microsoft.com)
[![Domain](https://img.shields.io/badge/Domain-Health%20Supply%20Chain-blue.svg)]()
[![Status](https://img.shields.io/badge/Status-Completed-success.svg)]()

## 📋 Project Overview
This project simulates an advanced national pharmaceutical supply chain and inventory analytics system inspired by operational realities in public health supply chains (e.g., regional medical stores, district health pharmacies, and integrated health centers). 

Built entirely in **Microsoft Excel (Advanced)**, this decision-support tool enables supply chain managers to monitor stock levels, detect stock-outs and overstocks, track product expiration dates using **FEFO (First Expired, First Out)** principles, evaluate supplier performance, and generate automated alerts.

---

## 🏗️ System Architecture & Data Model
The workbook is structured around 10 fully interconnected modules:
1. **README**: Project overview and user guide.
2. **PRODUCTS**: Product master catalog (International Nonproprietary Names, therapeutic categories, unit prices).
3. **FACILITIES**: Facility master data (Central warehouse, regional depots, district pharmacies, CSI).
4. **STOCK_DATA**: Real-time snapshot of stock quantities (On-hand, reserved, damaged, expired, available, in-transit).
5. **TRANSACTIONS**: Complete audit trail of stock movements (receipts, issues, adjustments).
6. **CONSUMPTION**: Monthly consumption tracking and reporting status by facility.
7. **SUPPLY_ORDERS**: Order management, supplier fulfillment rates, and delivery lead times.
8. **EXPIRY_TRACKING**: Lot-level expiration monitoring and FEFO risk priority scoring.
9. **ALERTS**: Automated anomaly detection system using multi-tier status criteria.
10. **KPI_DASHBOARD**: Executive interactive dashboard with dynamic charts and slicers.

---

## 📊 Key Performance Indicators (KPIs)
* **Stock Availability Rate**: **96.59%** across all facility lines.
* **Stock-out Lines**: **88 lines** (requiring emergency redistribution or transfers).
* **Inventory Value**: **125,023,111 XOF** (FCFA) total capital tied up in stock.
* **Months of Stock (MOS)**: Average coverage of **2.49 months**.
* **Order Fill Rate**: **6.65%** (highlighting critical upstream supplier bottlenecks).
* **Expiry Risks**: **230 lots** flagged under high/medium FEFO priority, with **34 expired lots** isolated in quarantine.

---

## 🚨 Automated Alert Logic (5-Tier Color Coding)
To prevent conflicting rules, stock status is classified using strict hierarchical evaluation:
* 🔴 **RED (Stock-out)**: Available quantity = 0. Immediate emergency replenishment required.
* 🔵 **BLUE (Overstock)**: Available quantity > Maximum stock threshold. Freeze new orders; redistribute surplus.
* 🟠 **ORANGE (Critical Low)**: Available quantity < Minimum stock threshold. Prioritize dispatch.
* 🟡 **JAUNE (Vigilance)**: Available quantity $\le$ Safety/Alert threshold. Close monitoring of consumption.
* 🟢 **VERT (Normal)**: Stock levels within normal operating parameters.

---

## 🛠️ Advanced Excel Techniques Used
* **Data Modeling & Power Query**: Relational data structuring and automated ETL pipelines.
* **Advanced Formulas**: `XLOOKUP` / `RECHERCHEX`, `SUMIFS` / `SOMME.SI.ENS`, `COUNTIFS` / `NB.SI.ENS`, `IFS` / `SI.CONDITIONS`, `FILTER` / `FILTRE`.
* **Dynamic Visualization**: Pivot Tables, Pivot Charts, and interactive Slicers connected across multiple data sources.
* **Conditional Formatting**: Automated multi-rule formatting for instant visual risk identification.

---

## 📈 Strategic Recommendations
1. **Mitigate Stock-outs**: Implement emergency inter-facility transfers from regional depots with surplus stock (`BLEU`) to deficit districts (`ROUGE`).
2. **Enforce FEFO Compliance**: Immediately quarantine and securely dispose of expired lots; ensure warehouse staff strictly issue goods based on expiration dates rather than arrival dates.
3. **Supplier Performance Management**: Address low order fill rates by establishing strict supplier scorecards, penalizing delivery delays, and building a central buffer stock.
4. **Optimize Working Capital**: Halt procurement on overstocked therapeutic categories to reallocate funds toward essential medicines with high consumption velocity.

---

## 👤 Author
**Data Analyst & Pharmaceutical Supply Chain Specialist**  
*Portfolio Project designed for international organizations (WHO, UNICEF, UNFPA, Global Fund).*