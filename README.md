# Ad Campaign Effectiveness: A/B Test Analysis

## 📌 Project Overview
This project analyzes the effectiveness of a digital marketing campaign using a dataset of **588,000 users**. The goal was to determine if the ads were driving actual conversions or if high conversion rates were simply a result of user activity levels ("Activity Bias").

Using **Python (Pandas, Seaborn)**, I performed an A/B test analysis comparing an exposed group (Ads) vs. a control group (PSA).

## ❓ The Business Problem
The marketing team needs to know:
1.  **ROI:** Are the ads actually causing people to buy, or would they have bought anyway?
2.  **Fatigue:** At what point do ads become annoying and stop working?
3.  **Optimization:** Which days and hours offer the best conversion opportunities?

## 📊 Key Insights & Findings

### 1. The "Whale" Effect (44% Lift)
My analysis revealed a massive **Activity Bias**. Users who spend more time on the platform naturally convert more often, regardless of ads.
* **Low Activity (<20 ads):** The ads have **zero impact**. The conversion rate for the Ad Group is identical to the Control Group.
* **High Activity (100+ ads):** The ads act as a multiplier. While the Control Group converted at **11.88%**, the Ad Group converted at **17.13%**.
* **Conclusion:** Targeting power users aggressively yields a **44% Relative Lift**, proving we are not fatiguing our best customers.

### 2. Temporal optimization
Initial analysis suggested a massive conversion spike (6%) on Saturdays at 5 AM.
* **Deep Dive:** Upon checking sample sizes, this was proven to be statistical noise ($n=18$).
* **Actionable Insight:** The reliable "Gold Zone" for ad spend is actually **Monday afternoons** and **Tuesday evenings**, where volume and conversion rates are stable.

## 🛠️ Tech Stack
* **Python:** Data cleaning and logic.
* **Pandas:** Grouping, aggregation, and pivot tables.
* **Matplotlib / Seaborn:** Visualization (Heatmaps, Lift Charts).
* **Stats:** Logic for causation vs. correlation.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/serafimk3/marketing-ab-test.git](https://github.com/yourusername/marketing-ab-test.git)
    ```
2.  Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```
3.  Run the notebook:
    ```bash
    jupyter notebook ad_analysis.ipynb
    ```

## 📈 Visuals
*(Note: These are generated in the notebook)*
* **Lift Chart:** Visualizes the divergence between Ad and PSA groups as activity increases.
* **Conversion Heatmap:** A temporal view of conversion rates by Day/Hour.

---
**Author:** Serafim Krastev
