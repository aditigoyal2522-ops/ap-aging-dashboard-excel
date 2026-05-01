# Vendor Payment Aging Dashboard
**Excel-based AP Aging Tracker | Finance Operations Portfolio Project**

---

## Overview

This project simulates a real-world Accounts Payable (AP) aging dashboard for a logistics company managing 30 vendors across 5 categories. It was built independently to demonstrate hands-on AP operations and Advanced Excel skills relevant to finance operations roles.

All vendor data is simulated for portfolio purposes. Vendor names are based on publicly known Indian logistics companies.

---

## Workbook Structure

| Sheet | Description |
|---|---|
| `Invoice_Register` | Master data of all 30 invoices with formula-driven status, aging, and outstanding calculations |
| `Aging_Dashboard` | Executive summary — KPI cards, aging bucket analysis, top overdue vendors |
| `Vendor_Summary` | Consolidated vendor-wise payment health across all categories |
| `Category_Analysis` | AP spend and outstanding by category with management commentary |
| `README` | In-file documentation and usage guide |

---

## Key Concepts Demonstrated

- **AP Aging Analysis** — Invoices bucketed into 0-30, 31-60, 61-90, and 90+ days overdue
- **3-Way Matching Logic** — Invoice amount vs. payment vs. outstanding reconciled per vendor
- **Payment Prioritisation** — CRITICAL / HIGH / LOW flags based on days overdue and vendor risk
- **Vendor Management** — Category-wise spend analysis to support vendor relationship decisions
- **Management Commentary** — Key AP insights and recommended actions mirroring real finance deliverables

---

## Formulas and Techniques Used

| Formula / Technique | Application |
|---|---|
| `=G{n}-H{n}` | Outstanding = Invoice Amount − Amount Paid (dynamic) |
| `=IF(Outstanding=0,"PAID",IF(TODAY()>Due Date,"OVERDUE","CURRENT"))` | Auto-status based on today's date |
| `=IF(TODAY()<=Due Date, 0, TODAY()-Due Date)` | Days overdue calculated live |
| Nested `IF` on Days Overdue | Aging bucket assignment (0-30 / 31-60 / 61-90 / 90+) |
| `COUNTIF` / `SUMIF` | Dashboard KPIs and bucket totals pulling from Invoice_Register |
| `SUMIF` on category column | Category-level spend aggregation in Category_Analysis |
| Freeze panes, structured tables | Navigation and readability for large dataset |

---

## How to Update

1. Go to `Invoice_Register` and add new invoice rows following the same format
2. Update the `Amount Paid` column as payments are processed — Outstanding recalculates automatically
3. `Status`, `Days Overdue`, and `Aging Bucket` update automatically based on `TODAY()`
4. `Aging_Dashboard` KPI cards and bucket analysis pull live via `COUNTIF`/`SUMIF` formulas — no manual updates needed

---

## Skills Demonstrated

`Accounts Payable` · `AP Aging Analysis` · `Vendor Management` · `Advanced Excel` · `SUMIF` · `COUNTIF` · `Dynamic Formulas` · `Financial Reporting` · `P2P Operations`

---

## Author

**Aditi Goyal**
MBA Finance | Finance Trainee — CJ Darcl Logistics Ltd

- LinkedIn: [linkedin.com/in/aditi-goyal-219aa3182](https://www.linkedin.com/in/aditi-goyal-219aa3182/)
- Email: aditigoyal2522@gmail.com
