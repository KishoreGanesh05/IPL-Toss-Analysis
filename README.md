 IPL Toss Decision Analysis: Strategy vs Outcome
## Overview

This project analyzes whether **winning the toss provides a measurable advantage in IPL matches** and evaluates whether teams make **optimal toss decisions (bat vs field)** across different venues.

The analysis goes beyond basic statistics by comparing:

* **What teams prefer (decision choice)**
* **What actually works (win outcomes)**
* **Whether differences are statistically significant**

---

##  Objectives

* Determine if winning the toss impacts match outcomes
* Analyze **bat vs field decision effectiveness**
* Identify **venue-specific strategies**
* Detect **decision-making inefficiencies**

---

##  Dataset

* IPL match dataset

* Key features used:

  * `venue`
  * `toss_decision` (bat/field)
  * `toss_match_win` (1 = win after toss, 0 = loss)

* Filter applied:

  > Only venues with **≥ 25 matches** considered for reliability

---

##  Methodology

### 1. Exploratory Data Analysis

* Overall toss win percentage
* Venue-wise performance trends

---

### 2. Decision Analysis

* **Decision Win %**
  → Probability of winning after choosing bat/field

* **Decision Choice %**
  → Frequency of choosing bat/field

---

### 3. Strategy–Outcome Gap


gap = win % − choice %

* Positive → underused but effective
* Negative → overused but less effective

---

### 4. Statistical Validation

* One-sample t-test against 50% baseline
* Conducted:

  * Overall
  * Per venue

---

##  Key Findings

### 1. Toss Impact is Not Statistically Significant

* Mean win rate after toss: **~52%**
* Median: **~51.9%**
* **p-value: 0.28**

> No significant evidence that winning the toss improves match outcomes.

---

### 2. Strong Bias Toward Fielding First

* Most venues show **>60% preference for fielding**
* Example: **M Chinnaswamy Stadium** (~90% field)

> Teams consistently favor chasing, regardless of statistical support.

---

### 3. Strategy vs Outcome Mismatch

At **M Chinnaswamy Stadium**:

* Field chosen ≈ **90%**, win ≈ **54%**
* Bat chosen ≈ **9%**, win ≈ **44%**

 Interpretation:

* Fielding has **higher absolute win rate**
* But is **heavily overused**
* Batting is **underutilized relative to usage**

> Indicates **decision bias**, not purely data-driven strategy

---

### 4. Venue-Specific Strategy Variation

* **Sawai Mansingh Stadium** → Fielding relatively more effective
* **MA Chidambaram Stadium** → Minimal difference between decisions

> Optimal strategy is **context-dependent**, not universal

---

### 5. No Venue Shows Statistical Significance

* All venue-level p-values **> 0.05**
* Closest: **Rajiv Gandhi International Stadium** (~0.061)

> Toss advantage is not statistically reliable even at individual venues

---

##  Key Insight

> While toss outcome itself is not a strong predictor of match success, teams exhibit consistent behavioral biases—often preferring fielding—despite limited statistical evidence supporting it.

---

##  Important Clarification

* A higher gap does **not** mean one decision is absolutely better
* It reflects **relative efficiency vs usage**, not direct superiority

---

## Limitations

* Does not include:

  * Pitch conditions (dew, surface type)
  * Team strength or player performance
* Uneven distribution of decisions (bat vs field)
* Multiple hypothesis testing across venues

---

##  Future Work

* Incorporate weather and pitch conditions
* Include team strength metrics
* Build predictive models for toss decision optimization

---

##  Tools & Technologies

* Python
* Pandas
* Seaborn / Matplotlib
* Folium (for venue visualization)

---

##  Conclusion

> Winning the toss does not provide a statistically significant advantage in IPL matches. However, teams display strong and consistent decision biases, often favoring fielding first, even in scenarios where it may not be the most efficient strategy. This highlights the importance of **data-driven, context-aware decision-making**.

---

##  Visualizations

* Strategy vs Outcome Heatmap
  <img width="1259" height="715" alt="image" src="https://github.com/user-attachments/assets/e1e8558c-97ee-4782-8ef9-6a65f1c27846" />

* Venue-wise Toss Decision Map
  <img width="1800" height="1200" alt="venue_toss_winrate" src="https://github.com/user-attachments/assets/69dd6f74-8ded-4b64-8ffb-3762552d207b" />



---

## Connect

If you’re interested in sports analytics, data-driven decision-making, or have feedback, feel free to connect!

---

