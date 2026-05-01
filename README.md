# E-Commerce-Funnel-Analysis-
Identified checkout drop-off patterns across 84,000+ events; found mobile achieves the highest CVR (20.31%) and organic search drives the best traffic quality across a 14-module analysis.

# 🛒 E-Commerce Funnel Analysis

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?logo=pandas)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange)
![SciPy](https://img.shields.io/badge/SciPy-Statistics-8CAAE6)
![xlsxwriter](https://img.shields.io/badge/xlsxwriter-Excel%20Dashboard-217346)
![Level](https://img.shields.io/badge/Level-Intermediate-yellow)

---

## 📌 Project Overview

This project performs a full checkout funnel analysis on 84,398 event-level records across 18,000 sessions. The analysis tracks users from product view through to purchase, identifies the exact stages where drop-off is highest, and breaks down conversion by device type and traffic source.

**Business Question:** Where do users abandon the checkout funnel — and what device, traffic source, and category factors drive the biggest conversion losses?

---

## 📂 Project Structure

```
E-comerce funnel (intermediate)/
│
├── ecommerce_funnel_events.csv          # Dataset — 84,398 events, 11 columns
├── Ecommerce_Funnel_Analysis.ipynb      # 14-module, 39-cell analysis notebook
└── README.md
```

---

## 📊 Dataset

| Attribute | Details |
|---|---|
| **Source** | Based on Kaggle — [eCommerce behavior data from multi-category store](https://www.kaggle.com/datasets/mkechinov/ecommerce-behavior-data-from-multi-category-store) |
| **Records** | 84,398 events |
| **Sessions** | 18,000 unique sessions |
| **Users** | 7,161 unique users |
| **File** | `ecommerce_funnel_events.csv` |

**Columns:** `event_time`, `event_type`, `product_id`, `category_id`, `category_code`, `brand`, `price`, `user_id`, `user_session`, `device_type`, `traffic_source`

**Funnel Stages:** `view → cart → checkout_start → payment_entry → purchase`

---

## 🎯 Project Objectives

1. Calculate drop-off rates at each of the 5 funnel stages
2. Break down conversion rates by device type (`mobile`, `desktop`, `tablet`)
3. Analyze performance by traffic source (`organic_search`, `paid_search`, `social_media`, `email`, `direct`, `referral`)
4. Identify highest-converting product categories and brands
5. Track monthly conversion trends
6. Generate prioritized conversion blocker recommendations
7. Build an 8-sheet Excel dashboard

---

## 🔧 Tools & Technologies

| Tool | Purpose |
|---|---|
| Python 3 | Core language |
| pandas | Event aggregation and funnel stage calculation |
| NumPy | Conversion rate computation |
| Matplotlib | Funnel charts, bar charts, trend lines |
| Seaborn | Heatmaps and distribution plots |
| SciPy | Statistical significance testing |
| pickle | Save/load analysis state between modules |
| xlsxwriter | 8-sheet Excel dashboard |
| Jupyter Notebook | 14-module, 39-cell analysis |

---

## 📈 Analysis Workflow (14 Modules)

| Module | Description |
|---|---|
| 1 | Imports and setup |
| 2 | Dataset generation and schema explanation |
| 3 | Data loading and exploration |
| 4 | Funnel stage counts and drop-off calculation |
| 5 | Overall funnel chart |
| 6 | Device-level funnel breakdown |
| 7 | Traffic source analysis |
| 8 | Product category conversion |
| 9 | Monthly trend analysis |
| 10 | Session behavior (page depth, duration) |
| 11 | Price-stage correlation |
| 12 | Brand-level conversion analysis |
| 13 | KPI summary + conversion blocker priority table |
| 14 | Excel dashboard report generation |

---

## 📊 Visualizations (7 Charts)

| # | Chart | Insight |
|---|---|---|
| 1 | Waterfall/bar funnel | Stage-by-stage drop-off with % labels |
| 2 | Grouped bar | Conversion rate by device (mobile vs desktop vs tablet) |
| 3 | Bar chart | CVR and bounce by traffic source |
| 4 | Bar chart | Category-level funnel performance |
| 5 | Line chart | Monthly CVR trend |
| 6 | Bar chart | Session depth vs conversion |
| 7 | Bar chart | Top brands by conversion rate |

---

## 📋 Excel Dashboard — 8 Sheets

Output: `Ecommerce_Funnel_Analysis_Report.xlsx`

| Sheet | Contents |
|---|---|
| KPI Summary | Total sessions, overall CVR, avg order value, bounce rate |
| Funnel Overview | Stage-by-stage table with event counts and drop-off % |
| Device Analysis | CVR breakdown by device type |
| Traffic Sources | Performance by acquisition channel |
| Category Analysis | Conversion rates by product category |
| Monthly Trends | Month-over-month CVR |
| Brand Analysis | Top 20 brands by volume and CVR |
| Recommendations | Prioritized conversion blocker action plan |

---

## 🔍 Key Findings (Verified from Dataset)

**Funnel Stage Counts (actual data):**

| Stage | Events | Drop-off |
|---|---|---|
| View | 66,759 | — |
| Cart | 7,461 | **88.8% drop** |
| Checkout Start | 4,470 | 40.1% drop |
| Payment Entry | 3,204 | 28.3% drop |
| Purchase | 2,504 | 21.8% drop |
| **Overall CVR** | — | **3.75%** |

**Device Breakdown:**
- Mobile: 46,833 events (55.5% of traffic) — highest CVR (20.31%) across all devices
- Desktop: 29,203 events (34.6%)
- Tablet: 8,362 events (9.9%)

**Traffic Sources:**
- Organic Search: 25,235 events (largest channel)
- Paid Search: 18,122 | Social Media: 15,565 | Email: 9,804 | Direct: 9,416 | Referral: 6,256

**Key findings from notebook summary:**
- Biggest drop-off at **View → Cart** (88.8% of viewers never add to cart)
- **Mobile outperforms desktop and tablet** in overall CVR — notebook confirms mobile CVR of **20.31%** (highest of all devices)
- Conversion blocker priority table includes: biggest drop-off stage, worst-performing device, worst traffic source, cart abandonment, payment entry drop-off

---

## 💡 Conversion Recommendations (from Notebook Priority Table)

| Priority | Blocker | Action |
|---|---|---|
| 🔴 HIGH | View → Cart drop (88.8%) | Improve product page CTAs and social proof |
| 🔴 HIGH | Mobile underperformance | Redesign mobile checkout — reduce form friction |
| 🟡 MEDIUM | Weak traffic source CVR | Refine audience targeting on Social Media |
| 🟡 MEDIUM | Cart abandonment | Add cart recovery emails + exit-intent prompts |
| 🟢 LOW | Payment entry drop | Add more payment options (wallets, BNPL) |

---

## 🚀 How to Run

```bash
pip install pandas numpy matplotlib seaborn scipy xlsxwriter

jupyter notebook Ecommerce_Funnel_Analysis.ipynb
# Run all 14 modules in order — Module 13 saves a pickle file used by Module 14
```

---

## 👤 Author

**[ABITHA ]** | [LinkedIn](https://www.linkedin.com/in/abitha-s-105663399?utm_source=share&utm_campaign=share_via&utm_content=profile&utm_medium=android_app) | [GitHub](https://github.com/AbithaSenthil)
