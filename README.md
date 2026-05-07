# 💳 Credit Card Fraud Risk Intelligence & Prevention System

## 📌 Problem Statement

Financial fraud poses a significant challenge for digital payment systems, often occurring in subtle patterns that are difficult to detect through basic reporting.
This project aims to analyze transaction data to uncover **hidden fraud patterns**, identify **high-risk segments**, and deliver **actionable strategies** to minimize fraud exposure.

---

## 📊 Dataset Overview

The dataset contains anonymized credit card transactions with the following key attributes:

* Transaction Time (Hourly granularity)
* Transaction Category (e.g., Grocery, etc.)
* Merchant Information (e.g., Swiggy, Zomato)
* Fraud Indicator (Fraud / Non-Fraud)

The dataset reveals that fraud is **extremely rare (0.17%)**, making detection more challenging and emphasizing the need for **pattern-based analysis rather than volume-based assumptions**.

---
⚙️ Technical Architecture / Workflow

<img width="1536" height="1024" alt="Technical architecture" src="https://github.com/user-attachments/assets/c1f6c04c-139a-4a52-8d2f-c3aa61066e3a" />

---
## 🧠 Analytical Techniques Used

- Time-based fraud trend analysis
- Merchant-level fraud concentration analysis
- Category risk segmentation
- KPI modeling using DAX
- Fraud pattern identification
- Interactive filtering and drilldown analysis
- 
---
## 🎯 Key Business Questions

1. When does fraud activity peak during the day?
2. Which categories and merchants are most vulnerable to fraud?
3. How can fraud risk be reduced despite a very low fraud rate?

---

## 📸 Dashboard Overview

![Dashboard Overview](Images/Dashboard.png)

---

## 🎛️ Dashboard Features

- Interactive slicers and filtering
- Dynamic KPI cards
- Time-based fraud trend analysis
- Merchant-level risk analysis
- Category segmentation visuals
- Executive summary reporting

---
## 📈 Key KPIs

| KPI | Value |
|---|---|
| Fraud Rate | 0.17% |
| Highest Risk Window | 12 AM – 4 AM |
| Highest Risk Category | Grocery |
| Top Risk Merchants | Swiggy, Zomato |
| Fraud Pattern Type | Time & Merchant Concentrated |

---
## 🔍 Key Insights

### ⏱️ Time-Based Fraud Patterns

* Fraud activity is **highly concentrated between 12 AM and 4 AM**
* This suggests fraudsters exploit **low monitoring periods and reduced user vigilance**

👉 Insight:

> Fraud is not random—it is **time-targeted**, indicating behavioral intent rather than coincidence.

---

### 🛒 Category Risk Analysis

* The **Grocery category contributes ~55% of total fraud cases**, making it the most vulnerable segment
* This indicates either:

  * High transaction volume masking fraud
  * OR weaker validation mechanisms in this category

👉 Insight:

> Fraud is **category-concentrated**, not evenly distributed across transactions.

---

### 🏪 Merchant-Level Risk

* Platforms like **Swiggy and Zomato** emerge as **top contributors to fraudulent transactions**
* This suggests:

  * High-frequency usage environments
  * Faster transactions with lower friction

👉 Insight:

> Fraud clusters around **high-velocity, low-friction platforms**

---

### ⚠️ Low Fraud Rate, High Impact

* Overall fraud rate is only **0.17%**, which is extremely low
* However:

  * Fraud is **strategically concentrated**
  * A small subset of transactions drives most of the risk

👉 Insight:

> Fraud detection should focus on **precision targeting**, not broad filtering

---

## 💡 Business Recommendations

### 🔐 Strengthen Monitoring During High-Risk Hours

* Increase fraud detection sensitivity between **12 AM – 4 AM**
* Implement real-time alerts and anomaly detection during this window

---

### 🛒 Apply Category-Based Risk Controls

* Introduce stricter validation for **Grocery transactions**
* Use adaptive authentication for high-risk categories

---

### 🏪 Monitor High-Risk Merchant Platforms

* Flag transactions from **Swiggy and Zomato** for additional verification
* Apply dynamic risk scoring based on merchant behavior

---

### 📊 Shift to Risk-Based Detection Strategy

* Since fraud rate is low (0.17%), avoid blanket rules
* Focus on:

  * Time-based triggers
  * Category-based anomalies
  * Merchant-level risk concentration

---

## 🚀 Business Impact

This solution enables stakeholders to:
- identify high-risk fraud windows,
- prioritize monitoring resources,
- improve fraud detection precision,
- and support proactive risk mitigation strategies through data-driven intelligence.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI | Dashboard Development & Visualization |
| DAX | KPI Measures & Risk Metrics |
| Power Query | Data Cleaning & Transformation |
| Excel / CSV | Raw Data Source |

---
## 🔮 Future Enhancements

- Real-time fraud alert integration
- Machine learning-based anomaly detection
- Dynamic fraud risk scoring
- Cloud-based deployment pipeline
- Transaction-level drillthrough analytics


---
## 📌 Author

**Yusuf M**

Aspiring Data Analyst focused on solving real-world business problems through data-driven insights

---
