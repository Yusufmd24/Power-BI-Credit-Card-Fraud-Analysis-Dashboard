# Credit Card Fraud Risk Intelligence System
### Power BI · DAX · Power Query · Excel

![Tool](https://img.shields.io/badge/Tool-Power%20BI-F2C811?style=flat&logo=powerbi&logoColor=black)
![Domain](https://img.shields.io/badge/Domain-BFSI%20%7C%20Risk%20Analytics-blue?style=flat)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=flat)

---

## Problem Statement

In digital payment systems, fraud rarely announces itself through volume — it hides in patterns.
With a fraud rate of just **0.17%**, blanket detection rules fail. This project builds a
**pattern-based fraud intelligence system** that identifies *when*, *where*, and *how* fraud
concentrates — enabling risk teams to allocate monitoring resources with surgical precision
rather than broad filtering.

---

## Dataset

| Attribute | Detail |
|---|---|
| Source | Anonymized credit card transaction records |
| Granularity | Hourly transaction-level |
| Key Dimensions | Time, Category, Merchant, Fraud Indicator |
| Class Imbalance | 0.17% fraud — extreme imbalance, pattern-first approach required |

---

## Technical Architecture

![Technical Architecture](https://github.com/user-attachments/assets/fdce39d4-bf28-4d7b-a9bd-afff455ec6bb)

---

## Business Questions Answered

1. When does fraud activity peak — and why does that window matter operationally?
2. Which transaction categories and merchants carry disproportionate fraud risk?
3. How should a risk team prioritize limited monitoring resources given a low base fraud rate?

---

## Analytical Approach

- Time-series fraud trend analysis (hourly bucketing)
- Merchant-level fraud concentration ranking
- Category risk segmentation with volume-adjusted fraud rates
- DAX-driven KPI modeling (fraud rate, risk index, trend flags)
- Interactive slicer/drilldown design for operational use

---

## Dashboard

![Dashboard Overview](Images/Dashboard.png)

**Features:** Dynamic KPI cards · Time-trend visuals · Merchant risk ranking · Category segmentation · Executive summary view

---

## Key KPIs

| KPI | Value |
|---|---|
| Overall Fraud Rate | 0.17% |
| Peak Risk Window | 12 AM – 4 AM |
| Highest Risk Category | Grocery (~55% of fraud cases) |
| Top Risk Merchants | Swiggy, Zomato |
| Fraud Concentration Type | Time-targeted & Merchant-clustered |

---

## Key Findings

### Time-Based Concentration
Fraud activity is **heavily concentrated between 12 AM and 4 AM**, suggesting deliberate
exploitation of low-monitoring windows — not random occurrence.

> **Implication:** Fraud is behaviorally timed. Detection models must weight time-of-day as a
> primary risk signal, not a secondary filter.

---

### Category Skew
The **Grocery category accounts for ~55% of all fraud cases** — a rate far exceeding its
likely transaction share — indicating either weaker validation mechanisms or higher exposure
to stolen credentials in this category.

> **Implication:** Category-level risk controls should be calibrated independently, not applied uniformly.

---

### Merchant Clustering
**Swiggy and Zomato** emerge as the leading merchant contributors to fraudulent transactions —
consistent with high-frequency, low-friction transaction environments where velocity is high
and review windows are short.

> **Implication:** Merchant-specific risk scoring should feed real-time decisioning, not just
> periodic review.

---

## Business Recommendations (Priority-Ordered)

| Priority | Action | Target |
|---|---|---|
| 🔴 High | Deploy real-time anomaly alerts for 12 AM – 4 AM window | Ops / Risk team |
| 🔴 High | Implement adaptive authentication for Grocery category | Product / Payments |
| 🟡 Medium | Apply dynamic risk scoring to Swiggy & Zomato transactions | Merchant Risk |
| 🟡 Medium | Shift detection logic to time + category + merchant signal combination | Analytics |
| 🟢 Low | Build transaction-level drillthrough for investigator workflows | Fraud Ops |

Estimated impact: Precision-targeted controls on the top risk window + category could
intercept a disproportionate share of fraud volume while minimizing friction for legitimate
users.

---

## Business Impact

This system equips fraud and risk teams to:

- **Reduce false positive rates** by replacing broad rules with precision-targeted signals
- **Concentrate monitoring resources** on the 12 AM – 4 AM window where fraud ROI is highest
- **Prioritize merchant review queues** based on dynamic risk concentration, not static lists
- **Support executive reporting** with a self-serve dashboard requiring no SQL access

---

## Repo Structure
````
credit-card-fraud-intelligence/
│
├── Data/
│   └── transactions.csv               # Raw transaction dataset
│
├── Images/
│   └── Dashboard.png                  # Dashboard screenshot
│
├── PowerBI/
│   └── fraud_intelligence.pbix        # Power BI report file
│
├── Docs/
│   └── dax-measures.md                # Full DAX measure reference
│
└── README.md
````
---

## Tools & Technologies

| Tool | Role |
|---|---|
| Power BI | Dashboard development & interactive visualization |
| DAX | KPI measures, risk index calculation, dynamic filtering |
| Power Query | Data cleaning, type casting, time-bucket derivation |
| Excel / CSV | Raw data source |

---

## Future Scope

- Real-time transaction scoring via streaming pipeline (Azure Event Hub / Kafka)
- ML-based anomaly detection layer (Isolation Forest / XGBoost) to complement rule-based flags
- Dynamic fraud risk score surfaced as a calculated column for operational use
- Cloud deployment with scheduled refresh and automated alert distribution

---

## Author

**Md Yusuf ** · [LinkedIn](#) · [Portfolio](#) · [GitHub](#)

Data Analyst with a background in operational leadership across manufacturing and events —
bringing a business-problem-first lens to analytics. Focused on BFSI risk intelligence,
operational analytics, and end-to-end BI delivery.
