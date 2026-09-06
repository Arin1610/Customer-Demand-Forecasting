# Customer Demand & Revenue Forecasting — Business Recommendations
**Arin Lale | Data Analytics Graduate Project**  
**Dataset: Online Retail II (UCI) | 2009–2011 | £17.37M Total Revenue**

---

## Executive Summary

This project analysed 17.37 million pounds of transactional retail data across 5,878 customers and 36,900+ orders. Using time-series forecasting, customer segmentation, and trend analysis, seven actionable business recommendations are identified below. Each finding is grounded in data and translated into strategic decisions relevant to insurance and financial services contexts — where customer lifetime value, retention, and demand forecasting are equally critical.

---

## Recommendation 1 — Prioritise Q4 Capacity Planning (September Trigger)

**Finding:** Revenue spikes dramatically from September onwards every year. October and November are consistently the highest revenue months across both 2010 and 2011:
- September 2010: £829,014 → November 2010: £1,166,460 (+40.7%)
- September 2011: £950,690 → November 2011: £1,156,206 (+21.6%)
- Q4 accounts for approximately 35–40% of annual revenue

**Recommendation:** Operational capacity planning should begin no later than **August** each year. This applies to staffing, inventory, logistics, and customer service resourcing. In an insurance context, this mirrors the need to pre-position claims handling and underwriting capacity ahead of known seasonal peaks (e.g. winter weather events, holiday travel).

**Action:** Set an automated September alert in forecasting dashboards to trigger resource scaling reviews.

---

## Recommendation 2 — Re-engage the Lost Customer Segment Immediately

**Finding:** The **Lost segment is the largest by customer count (1,646 customers — 28% of the base)** with an average recency of 492 days. These customers have not purchased in over 16 months. Their combined monetary value, if recovered even partially, represents significant upside.

**Recommendation:** Launch a targeted re-engagement campaign for Lost customers with:
- Personalised outreach referencing their last purchase category
- Time-limited incentive (discount or loyalty reward)
- A/B test two messaging approaches to identify what drives re-activation

**In insurance terms:** This is equivalent to lapsed policy re-engagement — a well-documented high-ROI activity since the cost of re-acquiring a lapsed customer is significantly lower than acquiring a new one.

**Target:** Even a 10% re-activation rate on 1,646 Lost customers = 164 returning customers.

---

## Recommendation 3 — Protect and Reward Loyal Customers

**Finding:** The **Loyal segment (876 customers — 15% of base) drives 60.85% of total revenue (£11.36M)**. Their average recency is just 38 days and average order frequency is 23 orders — significantly higher than any other segment.

**Recommendation:** Implement a formal loyalty programme for this segment:
- Early access to new products
- Dedicated account management or priority service
- Quarterly business reviews for top 100 customers by revenue

**Risk alert:** Losing even 10% of Loyal customers would cost approximately £1.1M in revenue. A churn early-warning model (using recency drift) should be built to flag Loyal customers showing signs of disengagement before they move to At-Risk.

---

## Recommendation 4 — Intervene on the At-Risk Segment Before They Become Lost

**Finding:** **At-Risk customers (1,494) have an average recency of 103 days** — they are still reachable but trending toward the Lost segment. Their average frequency (1.84 orders) suggests they are largely one-or-two-time buyers who have not returned.

**Recommendation:** Deploy a 60-day intervention window for At-Risk customers:
- Trigger automated outreach at the 60-day mark of no activity
- Offer a second-purchase incentive tied to their first purchase category
- Monitor weekly movement between segments using the RFM dashboard

**This is directly analogous** to insurance mid-term adjustment outreach — contacting customers before renewal lapse, not after.

---

## Recommendation 5 — Focus International Expansion on EIRE and Netherlands

**Finding:** After the United Kingdom (£14.39M), the top international markets are:
- EIRE: £616,571
- Netherlands: £554,038
- Germany: £425,020
- France: £348,769

EIRE and Netherlands are significantly ahead of other markets and show strong organic demand without dedicated market investment.

**Recommendation:** Prioritise EIRE and Netherlands for:
- Localised marketing and currency/language optimisation
- Dedicated account managers for top customers in these regions
- Investigate whether Netherlands growth is driven by a small number of large B2B buyers (which would indicate wholesale opportunity)

**For Allianz specifically:** This mirrors international market prioritisation decisions in insurance — where regulatory environment, existing brand presence, and organic demand signals guide expansion sequencing.

---

## Recommendation 6 — Use Forecasting Model to Drive Procurement Decisions

**Finding:** The Prophet time-series model achieved a **MAPE of 9.91%** on an 8-week holdout — meaning forecasts are accurate to within ~10% on average. The model captures both the overall upward trend and the Q4 seasonal spike reliably.

**Recommendation:** Integrate weekly revenue forecasts into procurement and inventory planning cycles:
- Use the 12-week forward forecast as the baseline for stock ordering
- Flag weeks where forecast exceeds the upper confidence band as high-demand alerts
- Re-train the model quarterly with fresh data to maintain accuracy

**Model Performance Summary:**

| Metric | Value |
|--------|-------|
| MAE | £33,804 |
| RMSE | £64,884 |
| MAPE | 9.91% |
| Forecast horizon | 12 weeks |

A MAPE below 10% is considered strong for weekly retail forecasting and is suitable for operational decision-making.

---

## Recommendation 7 — Investigate February and April Revenue Dips

**Finding:** February is consistently the weakest month across all years:
- February 2010: £504,559 (lowest of the year)
- February 2011: £446,085 (lowest of the year)

April also shows a consistent dip relative to March, suggesting a post-quarter-end slowdown.

**Recommendation:** Use the February and April dips as opportunities for:
- Promotional campaigns to stimulate demand during low periods
- Staff training and development activities when operational load is lowest
- Annual planning and strategy cycles timed to low-revenue periods to minimise disruption

---

## Summary Table

| # | Recommendation | Segment / Area | Priority |
|---|----------------|----------------|----------|
| 1 | Begin Q4 capacity planning in August | Operations | 🔴 High |
| 2 | Re-engage 1,646 Lost customers | Lost Segment | 🔴 High |
| 3 | Protect Loyal customers with formal programme | Loyal Segment | 🔴 High |
| 4 | 60-day intervention for At-Risk customers | At-Risk Segment | 🟠 Medium |
| 5 | Expand into EIRE and Netherlands | International | 🟠 Medium |
| 6 | Integrate forecast model into procurement | Operations | 🟠 Medium |
| 7 | Run promotions in February and April | Marketing | 🟡 Low |

---

## Methodology Summary

| Component | Tool / Method |
|-----------|--------------|
| Data Cleaning | Python, Pandas |
| Exploratory Analysis | Plotly, Seaborn, Matplotlib |
| Time-Series Forecasting | Facebook Prophet (multiplicative seasonality) |
| Customer Segmentation | RFM Analysis + K-Means Clustering (k=4) |
| Trend Analysis | Seasonal decomposition, YoY analysis |
| Dashboard | Power BI (4-page interactive report) |
| Dataset | Online Retail II — UCI Machine Learning Repository |

---

*This analysis was conducted as part of a data analytics portfolio project demonstrating end-to-end data pipeline skills including data engineering, machine learning, and business intelligence reporting.*
