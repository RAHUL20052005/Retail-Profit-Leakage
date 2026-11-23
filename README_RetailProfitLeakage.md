# 🛒 Retail Chain Profit Leakage & Demand Optimization

Data analytics project that finds where a retail chain loses profit (discounts, cancellations, returns, below-cost sales), which vendors and stores cause problems, and which products are worth promoting. Built with **SQL, Python, Power BI and Tableau**.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge&logo=postgresql&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Tableau](https://img.shields.io/badge/Tableau-E97627?style=for-the-badge&logo=tableau&logoColor=white)

---

## 📌 Business Problem
A multi-store retail chain was losing margin without knowing exactly where. The goal was to quantify profit leakage, spot unreliable vendors and stockout hotspots, and recommend which SKUs to promote.

## 🎯 Objectives
- Clean and validate the sales, returns, purchase order and inventory data
- Quantify the main sources of profit leakage
- Evaluate vendor delivery performance against SLA
- Identify stockout hotspots by SKU and store
- Rank SKUs by margin and return rate to guide promotions
- Deliver an operational dashboard (Power BI) and an executive dashboard (Tableau)

## 🔍 Key Findings

### Top 5 loss drivers
| Loss Driver | Amount (Rs) |
|---|---|
| Discounts given | 3,555,856 |
| Cancelled orders (lost sales) | 1,657,152 |
| Approved returns / refunds | 1,538,469 |
| Sold below cost (margin destroyed) | 863,839 |
| Refunds with no matching sale | 53,827 |

**Discounts are the largest leak**, followed by cancelled orders and approved returns.

### Worst 3 vendors (by SLA breach)
| Vendor | POs | Avg Delay (days) | SLA Breach % |
|---|---|---|---|
| VEND0026 | 226 | 1.1 | 38.16% |
| VEND0018 | 241 | 1.1 | 36.59% |
| VEND0056 | 263 | 0.94 | 36.40% |

### Stockout hotspots
SKU00503 (PUN01), SKU00566 (BEN01), SKU01164 (DEL01), SKU00734 (AHM05) and SKU00727 (DEL05), each with 2 stockout days.

### Best 5 SKUs to promote
| SKU | Name | Category | Margin % | Return Rate % |
|---|---|---|---|---|
| SKU00581 | Nestora Frozen Veg 750ml | Frozen | 28.14 | 0.00 |
| SKU01127 | AquaFizz Cheese Combo | Dairy | 25.47 | 0.00 |
| SKU01187 | FrostBite Diapers 250g | Baby Care | 28.59 | 1.56 |
| SKU00297 | FrostBite Frozen Snacks 2L | Frozen | 27.36 | 1.35 |
| SKU00006 | FreshCo Edible Oil 1L | Groceries | 26.78 | 1.49 |

## ✅ Recommendations
1. Review discount policy, since discounts are the biggest source of leakage
2. Investigate cancelled orders to recover lost sales
3. Tighten return approval and check refunds that have no matching sale
4. Stop or reprice items sold below cost
5. Put the three worst vendors on performance improvement plans
6. Rebalance stock at stockout hotspot stores
7. Promote high-margin, low-return SKUs

## 🧰 Workflow
```
Excel dataset → Python (clean, validate, analyse) → SQL (schema + queries)
             → Power BI (operational dashboard) → Tableau (executive dashboard)
```

> 📷 Add dashboard screenshots here, e.g. `![Power BI Dashboard](images/powerbi_dashboard.png)`

## 📁 Repository Structure
```
Retail-Profit-Leakage/
├── data/            # source dataset
├── python/          # cleaning and analysis notebooks
├── sql/             # schema and queries
├── powerbi/         # .pbix file
├── tableau/         # .twbx file
├── images/          # dashboard screenshots
├── reports/         # executive summary PDF
└── README.md
```
*(Adjust the folder names to match your repository.)*

## 🛠 Tools Used
Python (Pandas) · SQL · Power BI Desktop · Tableau

## 👤 Author
**Battu Rahul Sai**
🌐 [Portfolio](https://rahul20052005.github.io) · 💼 [LinkedIn](YOUR_LINKEDIN_URL) · 💻 [GitHub](https://github.com/RAHUL20052005)
