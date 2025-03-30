# A/B Testing on Marketing Campaign Data

This project evaluates the effectiveness of a digital ad campaign using A/B testing on a dataset of 580,000+ users. The analysis investigates whether ad exposure increases conversions compared to Public Service Announcements (PSAs), and explores the impact of ad timing and volume.

---

## Objective

To determine whether users exposed to **ads** convert at a significantly higher rate than those exposed to **PSAs**, and identify **when** and **how much ad exposure** maximizes conversion.

---

## Experiment Setup

| Group         | Description                                  |
|---------------|----------------------------------------------|
| Test Group    | Users shown **ads** (`test group = 'ad'`)    |
| Control Group | Users shown **PSAs** (`test group = 'psa'`)  |

---

## Metrics

### Primary Metric
- **Conversion Rate**: Proportion of users who completed a desired action (`converted = True`)

### Secondary Metrics
- `total ads`: Number of ads shown to a user
- `most ads day`: Day when most ads were seen
- `ads time`: Hour (in 12-hour format) of highest ad exposure

---

## Hypotheses

### Primary Hypothesis
- **H₀**: Conversion rate is equal between ad and PSA groups  
- **H₁**: Conversion rate is different between ad and PSA groups

### Secondary Hypotheses
- Conversion varies by day/time of exposure  
- Users who convert see more ads

---

## Statistical Methods

| Test                     | Purpose                                     |
|--------------------------|---------------------------------------------|
| Chi-Squared Test         | Categorical independence (e.g. ad vs PSA)   |
| Shapiro-Wilk Test        | Test for normality of ad exposure           |
| Levene’s Test            | Test for equal variance of `total ads`      |
| Mann–Whitney U Test      | Compare ad volume across converted groups   |

---

## Key Findings

- **Conversion Rate (Ad Group)**: 2.55%  
- **Conversion Rate (PSA Group)**: 1.79%  
- **🔼 Uplift**: **43% relative increase** in conversion rate for ad-exposed users

- 🗓️ **Best Day**: Highest conversion on **Mondays**
- ⏰ **Best Time**: Highest conversion around **4 PM**
- 📺 **Ad Volume**: Users who converted saw more ads (confirmed via Mann–Whitney U test)

---

## Actionable Recommendations

1. **Prioritize Ad Delivery on Mondays**, when conversions peak.
2. **Target peak hours (3–5 PM, 8 PM)** for higher conversion.
3. **Optimize ad frequency** — more exposure increases conversion, but should be tested further to avoid fatigue.
4. **Use PSAs as baseline** in future campaign ROI measurement.
5. **A/B test different creatives** now that format is validated.

---

## Files Included

- `marketing_AB.csv` — dataset
- `marketing_ab_test_notebook.ipynb` — full analysis
- `a-b-testing-on-marketing-data.html` — exported notebook
- `README.md` — project summary

---

## Tools & Libraries

- **Python** (Pandas, NumPy)
- **Seaborn**, **Matplotlib** — for visualization
- **Scipy.stats** — for hypothesis testing

---

## Author

**Sankalp Biswal**  
Data Analyst | Python • SQL • A/B Testing • Statistics  
[LinkedIn](https://www.linkedin.com/in/sankalp-biswal/) | [GitHub](https://github.com/Sankalp20487)

---

