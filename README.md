# marketing-campaign-analysis
Marketing campaign targeting rule &amp; coupon decision
# Marketing Campaign Targeting & Coupon Decision

## 📌 Project Overview
This project aims to design an executable targeting rule for marketing campaigns to optimize coupon ROI. Based on the Kaggle Marketing Campaign dataset (2,240 records, baseline response rate: 14.9%), I explored the trade-off between targeting precision and coverage, and how coupon face value affects the optimal decision.

## 🔍 Key Findings
1. **Strong Predictive Signals:** Historical response count (`total_accepted`) and recency (`Recency`) showed strong monotonic relationships with the target response. Users who responded 4 times have a 90.9% response rate, compared to 8.2% for those who never responded.
2. **Rule Performance (Lift):** By scanning 3D threshold combinations, the strictest rule achieved a **73.1% precision** (compared to the 14.9% baseline), yielding a **Lift of 4.90x** for the top 20% targeted audience.
3. **Cost-Driven Decision Reversal:** The optimal rule strictly depends on the coupon face value:
   - **10 RMB Coupon:** The "broad rule" (covering 283 users) yields the highest net profit (2,370 RMB).
   - **50 RMB Coupon:** All broad rules result in significant losses (up to -8,950 RMB). Only the "strict rule" remains profitable. 

## 📁 Repository Structure
- `campaign_analysis.ipynb`: Full Jupyter Notebook containing data cleaning, feature engineering, threshold scanning, and cost-benefit analysis.
- `marketing_campaign.csv`: The raw dataset used for analysis.

## 🛠️ Tech Stack
- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Jupyter Notebook
