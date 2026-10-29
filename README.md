# Procurement Performance Dashboard

An interactive Excel dashboard that analyzes 777 purchase orders across 5 suppliers to track cost savings, supplier compliance, delivery lead time, and order status.

![Procurement Performance Dashboard](main-interface.png)

## Key Metrics

| Metric | Value |
|---|---|
| Purchase orders analyzed | 777 |
| Total quantity ordered | 850,551 units |
| Total cost savings (excluding cancelled orders) | 3,638,920 |
| Average negotiated saving vs. list price | ~8.0% |
| Average delivery lead time | 10.8 days |
| Compliant purchase orders | 82.4% (640 of 777) |

## Key Findings

- **Compliance gap:** 137 purchase orders (17.6%) are non-compliant. Delta Logistics accounts for the most (67 of its 171 orders), while Epsilon Group has only 3 of 166.
- **Delivery performance:** average lead time ranges from 10.19 days (Gamma Co) to 11.27 days (Beta Supplies, the slowest).
- **Cost savings:** negotiated prices are lower than list prices across all suppliers. Beta Supplies delivers the highest total savings, and MRO is the top-saving item category.
- **Sourcing patterns:** purchasing volume is spread across suppliers and item categories in different proportions, which points to opportunities to rebalance supplier allocation.

## Recommendations

1. **Strengthen compliance controls:** investigate non-compliant purchase orders, identify recurring control gaps, and reinforce procurement verification.
2. **Improve delivery efficiency:** review suppliers with longer lead times and improve planning and coordination.
3. **Optimize supplier negotiations:** prioritize negotiations by total cost-saving potential, while considering reliability, delivery performance, and quality.
4. **Optimize sourcing strategy:** monitor purchasing concentration and evaluate alternative sourcing options to reduce dependency risk.

## About the Dataset

The workbook contains 777 purchase orders placed between January 2022 and January 2024.

| Column | Description |
|---|---|
| `PO_ID` | Purchase order ID |
| `Supplier` | Supplier name (5 suppliers) |
| `Order_Date`, `Delivery_Date` | Order and delivery dates |
| `Item_Category` | Electronics, MRO, Office Supplies, Packaging, Raw Materials |
| `Order_Status` | Delivered, Pending, Partially Delivered, Cancelled |
| `Quantity` | Units ordered |
| `Unit_Price`, `Negotiated_Price` | List price and negotiated price per unit |
| `Defective_Units` | Number of defective units received |
| `Compliance` | Whether the order followed procurement rules (Yes/No) |

### Calculated columns

| Column | Formula |
|---|---|
| `Avg. Delivery Lead Time` | `Delivery_Date - Order_Date` (days) |
| `Saving Per unit` | `Unit_Price - Negotiated_Price` |
| `Saving Percentage` | `Saving Per unit / Unit_Price` |
| `Total Cost Savings` | `Quantity x Saving Per unit` |

## What's Inside the Workbook

- **Dashboard:** KPI cards, interactive charts, and an Item Category slicer plus a timeline slicer.
- **Key Insights:** findings and prioritized recommendations.
- **Procurement KPI Analysis Dataset:** the cleaned data with the calculated columns above.
- **Pivot tables (hidden sheet):** the summaries that feed the dashboard charts.

## Tools & Skills

Microsoft Excel · PivotTables & PivotCharts · Slicers & Timelines · Formulas · KPI Reporting · Data Cleaning & Validation

## How to Use

1. Download `PROCUREMENT_PERFORMANCE_DASHBOARD.xlsx`.
2. Open it in Excel 2013 or later (the timeline slicer requires it).
3. Use the slicers on the Dashboard sheet to filter by item category and date range.

> Please do not move or resize the slicers and charts on the Dashboard sheet.

## Author

**Lara Kashmeri**, Data Analyst & MIS Professional

[Portfolio](https://larakashmeri.github.io/) · [LinkedIn](https://www.linkedin.com/in/lara-kashmeri-158951244) · [GitHub](https://github.com/Larakashmeri)
