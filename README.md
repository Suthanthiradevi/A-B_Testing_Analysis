# Eniac-s_A_B_Test
A data-driven A/B/C/D test analysis using Python and Chi-Square contingency testing to optimize homepage CTA button design, color, and conversion funnel engagement for an online retailer.
# Eniac Homepage CTA Optimization: A/B/C/D Test Analysis

## 📌 Project Overview
This repository contains a rigorous statistical analysis of an A/B/C/D experiment conducted on Eniac's e-commerce homepage. The goal of the project was to optimize the primary banner's Call-to-Action (CTA) button by resolving a business challenge: the original white "SHOP NOW" button occupied prime digital real estate but only yielded a ~2% Click-Through Rate (CTR).

Through user survey research, the UX team hypothesized that direct language felt like too strong of an upfront commitment. We designed and ran a 14-day multi-variant experiment testing four specific combinations of color and text framing.

### Tested Variants
*   **Version A (Control):** White "SHOP NOW"
*   **Version B:** Red "SHOP NOW"
*   **Version C:** White "SEE DEALS"
*   **Version D:** Red "SEE DEALS"

---

## 🛠️ Tech Stack & Methodology
*   **Language:** Python 3
*   **Libraries Used:** `pandas`, `numpy`, `scipy.stats`, `itertools`
*   **Statistical Tests:**
    *   **Omnibus Test:** Chi-Square Test of Independence ($\alpha = 0.05$)
    *   **Post-Hoc Analysis:** Pairwise Chi-Square tests utilizing the **Bonferroni Adjustment** ($\alpha_{\text{adjusted}} = 0.0083$) to counteract Type I Errors across 6 unique comparisons.

---

## 📊 Experimental Results

### 1. Global (Omnibus) Analysis
The initial global Chi-Square test rejected the Null Hypothesis ($H_0$). The differences in user click distributions across the versions were mathematically significant and could not be attributed to random noise.

### 2. Pairwise Post-Hoc Discoveries
The automated pairwise script isolated the following trends:
*   **Color Impact:** Both red variants (**B** and **D**) experienced a severe performance drop compared to white variations ($p < 0.0083$). Red is an ineffective anchor color for the Eniac homepage banner.
*   **The Text Framing Tie:** The head-to-head match between **Version A** (White "SHOP NOW") and **Version C** (White "SEE DEALS") yielded a $p\text{-value}$ of **0.46**. This significantly exceeded our adjusted significance threshold ($0.0083$), indicating a statistical tie in absolute upfront traffic draw.

### 3. Funnel Ingestion & Engagement (Tie-Breaker Metrics)
Because upfront CTR performance was matched, the evaluation was expanded to down-funnel behavioral analytics to select the true business asset:


| Performance Metric | Version A ("SHOP NOW") | Version C ("SEE DEALS") | Status |
| :--- | :---: | :---: | :---: |
| **Upfront CTR** | ~2.02% | ~2.11% | **Statistically Tied** |
| **Drop-Off Rate** | 38% | **24%** | **Version C Wins** |
| **Homepage-Return Rate** | 21% | **13%** | **Version C Wins** |

---

## 🏆 Final Business Recommendation
**Implement Version C (White "SEE DEALS") as the permanent homepage banner CTA.**

**Justification:** While both white buttons pull identical traffic volumes, **Version C** acts as a much cleaner funnel filter. Users interacting with "SEE DEALS" show a **14% absolute reduction in funnel drop-off** and an **8% lower rate of bouncing back** to the homepage. Low-commitment text framing manages user expectations accurately, yielding higher-quality, deep-funnel intent.
Use code with caution.
