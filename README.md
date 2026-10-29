# Procurement Performance Dashboard

An interactive Excel dashboard that analyzes 777 purchase orders across 5 suppliers to track cost savings, supplier compliance, delivery lead time, and order status, and turns the results into prioritized recommendations.

![Procurement Performance Dashboard](main-interface.png)

## Business Questions Answered

- How much are we saving through supplier negotiations?
- Which suppliers deliver fastest, and which are slowest?
- How compliant are our purchase orders, and where are the gaps?
- How is spending distributed across suppliers and item categories?

## Key Metrics

| Metric | Value |
|---|---|
| Purchase orders analyzed | 777 |
| Total quantity ordered | 850,551 units |
| Total cost savings (excluding cancelled orders) | 3,638,920 |
| Average negotiated saving vs. list price | ~8.0% |
| Average delivery lead time | 10.8 days |
| Compliant purchase orders | 82.4% (640 of 777) |
| Delivered orders | 560 of 777 (72%) |

## Key Insights

![Key Insights & Recommendations](key insight.png)

### 1. Cost Optimization
Negotiated prices are lower than list prices across every supplier, an average saving of about 8.0%. Beta Supplies delivers the highest total savings (about 831K), while Alpha Inc delivers the lowest (about 622K). By category, MRO produces the largest savings (about 880K).

### 2. Delivery Performance
Average delivery lead time ranges from 10.19 days (Gamma Co) to 11.27 days (Beta Supplies, the slowest). The gap between suppliers is small, so improvements are likely to come from planning and coordination rather than switching suppliers.

### 3. Supplier & Category Analysis
Purchasing volume is not evenly distributed: Delta Logistics receives the most orders (171) and Alpha Inc the fewest (141), across five item categories (Electronics, MRO, Office Supplies, Packaging, Raw Materials). This highlights opportunities to optimize sourcing and supplier allocation.

### 4. Compliance Monitoring
137 purchase orders (17.6%) are marked non-compliant. The problem is concentrated in one supplier: Delta Logistics has 67 non-compliant orders (compliance of about 61%), while Epsilon Group has only 3 (about 98%).

## Recommendations

| Priority | Recommendation | Action |
|---|---|---|
| **High** | Strengthen compliance controls | Investigate non-compliant purchase orders, identify recurring control gaps, and reinforce procurement verification. |
| **Medium** | Improve delivery efficiency | Review suppliers with longer lead times and improve planning, coordination, and delivery performance. |
| **Medium** | Optimize supplier negotiations | Prioritize negotiations by total cost-saving potential, while considering reliability, delivery performance, and quality. |
| **Low** | Optimize sourcing strategy | Monitor purchasing concentration and evaluate alternative sourcing options to reduce dependency risk. |

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

- **Dashboard:** KPI cards, interactive charts, an Item Category slicer, and a timeline slicer.
- **Key Insights:** findings and prioritized recommendations.
- **Procurement KPI Analysis Dataset:** the data with the calculated columns above.
- **Pivot tables (hidden sheet):** the summaries that feed the dashboard charts.

## Tools & Skills

Microsoft Excel · PivotTables & PivotCharts · Slicers & Timelines · Formulas · KPI Reporting · Data Cleaning & Validation

## Repository Files

| File | Description |
|---|---|
| `PROCUREMENT_PERFORMANCE_DASHBOARD.xlsx` | The Excel workbook |
| `main-interface.png` | Dashboard screenshot |
| `key insight.png` | Key Insights & Recommendations screenshot |

## How to Use

1. Download `PROCUREMENT_PERFORMANCE_DASHBOARD.xlsx`.
2. Open it in Excel 2013 or later (the timeline slicer requires it).
3. Use the slicers on the Dashboard sheet to filter by item category and date range.

> Please do not move or resize the slicers and charts on the Dashboard sheet.

## Author

**Lara Kashmeri**, Data Analyst & MIS Professional

[Portfolio](https://larakashmeri.github.io/) · [LinkedIn](https://www.linkedin.com/in/lara-kashmeri-158951244) · [GitHub](https://github.com/Larakashmeri)
