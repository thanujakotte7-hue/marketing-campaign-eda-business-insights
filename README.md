# 📊 Marketing Campaign EDA: Business Insights Report

Exploratory Data Analysis (EDA) on a marketing campaign dataset to understand **why** some channels perform better than others, and to recommend where the marketing budget should go based on **ROI**.

> **Internship Task 04** | SkillCraft Technology

---

## 🎯 Objective

Instead of building a Machine Learning model, this project focuses on the **"Why"** behind campaign performance:

- Clean and prepare the raw marketing data
- Visualize the marketing funnel
- Compare channels using ROI, CPA, and CTR
- Recommend which channels should receive more (or less) budget

---

## 📁 Project Structure

```
marketing-campaign-eda-business-insights/
│
├── data/
│   └── marketing_campaign_dataset.csv
├── notebook/
│   └── marketing_eda.ipynb
├── images/
│   ├── funnel.png
│   ├── roi.png
│   ├── spend_revenue.png
│   └── cpa.png
├── report/
│   └── Business_Insights_Report.pdf
├── requirements.txt
└── README.md
```

---

## 🗂️ Dataset

| Detail | Info |
|---|---|
| File | `marketing_campaign_dataset.csv` |
| Rows | 200000 |
| Columns | 18 |
| Key columns | Campaign_Type, Channel_Used, Acquisition_Cost, ROI, Clicks, Impressions, Conversion_Rate, Engagement_Score |

**Derived columns:**
- `conversions = clicks × conversion_rate`
- `revenue = acquisition_cost × (1 + ROI)`

---

## 🧹 Data Cleaning

- Standardized column names
- Converted `Acquisition_Cost` (`$16,174.00`) and `Duration` (`30 days`) to numeric
- Parsed `Date` column to datetime
- Removed duplicate rows
- Handled missing values
- Removed invalid rows (cost ≤ 0, clicks > impressions)
- Standardized channel names (trim + title case)

---

## 📈 Analysis Performed

1. Data overview and summary statistics
2. Channel-wise metrics: **CTR, CPA, ROI, Spend Share**
3. Funnel analysis: Impressions → Clicks → Conversions
4. Spend vs Revenue comparison
5. Correlation analysis
6. Campaign-type performance comparison

📄 Full 1-page report: [`report/Business_Insights_Report.pdf`](report/Business_Insights_Report.pdf)

---

## 🛠️ Tech Stack

- Python 3
- Pandas, NumPy
- Matplotlib, Seaborn, Plotly
- Jupyter Notebook / Google Colab

---

## ▶️ How to Run

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/marketing-campaign-eda-business-insights.git
cd marketing-campaign-eda-business-insights

# 2. Install dependencies
pip install -r requirements.txt

# 3. Open the notebook
jupyter notebook notebook/marketing_eda.ipynb
```

---

## 📝 Assumptions

- Revenue was derived from ROI and acquisition cost, as the dataset has no direct revenue column.
- Conversions were estimated as clicks × conversion rate.

---

## 👤 Author

Thanuja
---

⭐ If you found this useful, consider giving the repo a star!
