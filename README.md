# clipboardhealth

# 📊 Clipboard Health Shift Marketplace Analysis

This project analyzes ~19,900 healthcare shift offers from Clipboard Health’s two-sided marketplace, connecting healthcare facilities (demand) with workers (supply). The goal is to evaluate marketplace efficiency, worker reliability, and identify key friction points—such as shift deletions and low claim rates—that impact liquidity and revenue.

---

## 📌 Problem Statement

Clipboard Health aims to match healthcare workers with open shifts. Despite a strong worker reliability rate, the platform faces liquidity issues, particularly:

- **Only 64.3% of shifts are claimed**
- **18.5% of shifts are deleted before being filled**, representing lost revenue and potential inefficiencies

This project investigates root causes behind these numbers and provides actionable insights to improve claim rates and reduce deletions.

---

## 🧠 Key Questions Answered

- What drives shift deletions and how much revenue is lost due to them?
- How does lead time, pay rate, time of day, and shift type affect claim success?
- Can we build predictive models to identify which shifts are unlikely to be claimed?
- What patterns of worker behavior signal missed engagement opportunities?

---

## 📈 Summary of Key Findings

- **Lead Time Matters:** Shifts posted 1–2 days in advance perform best (76.5% claim rate).
- **Shift Type Matters:** NOC shifts perform better than AM/PM, possibly due to higher pay or less competition.
- **Pay Drives Claim Rate:** Shifts paying >$35/hr have an 83.2% claim rate vs. just 50.2% under $20/hr.
- **More Offers ≠ More Claims:** Shifts sent to fewer workers are more likely to be filled.

---

## 🔍 Predictive Modeling

Multiple models were trained to predict the likelihood of a shift being claimed:

- **Logistic Regression**  
  AUC: `0.771`

- **Random Forest**  
  AUC: `0.797`

- **XGBoost**  
  AUC: `0.817`

Top predictive features:
- Pay Rate
- Lead Time
- Shift Hour
- Offer Count
- Workplace Claim History

---

## 💡 Product Insights & Recommendations

- **Engage High-Deletion Facilities:** Target accounts that post and delete most of their shifts.
- **Pay-Based Nudges:** Encourage facilities to raise pay for shifts with low claim likelihood.
- **Optimize Offer Strategy:** Reduce over-broadcasting; fewer targeted offers improve urgency.
- **Retarget 'Lurker' Workers:** Identify workers who view shifts but never claim, and experiment with nudges or incentives.
- **Highlight NOC Shift Success:** Learn from higher engagement and apply to weaker PM shift strategies.

---

## 🛠️ Tools & Technologies

- Python (Pandas, NumPy, Scikit-learn, XGBoost)
- Data Visualization: Seaborn, Matplotlib
- Jupyter/Google Colab for experimentation
- Excel export for business stakeholder review

---

## 🧪 Reproducibility

To reproduce this analysis:

1. Clone the repo  
   ```bash
   git clone https://github.com/your-username/clipboard-health-analysis.git
   cd clipboard-health-analysis
