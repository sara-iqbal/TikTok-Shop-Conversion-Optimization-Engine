# TikTok Shop Conversion Optimization Engine

## Project Overview
This project simulates a large-scale A/B test for TikTok Shop. The goal was to determine if adding a "Countdown Timer" to Live Stream Flash Sale notifications increases user conversion rates and Average Order Value (AOV).

## The Scenario
* **Control (A):** Standard push notification.
* **Variant (B):** Notification with an urgency-based countdown timer (copy generated via LLM).

## Technical Implementation
1.  **Power Analysis:** Calculated required sample size using `statsmodels` to ensure the experiment was statistically valid before data collection.
2.  **Data Generation:** Scripted a synthetic dataset of 100,000 sessions to mimic real-world TikTok traffic, including age demographics (Gen Z vs. Millennials) and skewed purchase data.
3.  **Statistical Testing:**
    * **Z-Test:** Used for conversion proportions.
    * **Mann-Whitney U Test:** Used for spend data, accounting for the non-normal distribution of purchase amounts.
4.  **Bias Check:** Performed a segmentation analysis to identify if the "Novelty Effect" was present or if specific age groups drove the majority of the lift.

## Key Findings
* The Countdown Timer resulted in a **2.4% incremental lift** in conversion rates.
* The feature was significantly more effective with the **Gen Z segment** (+3.1% lift).
* At scale, this optimization is projected to generate **£4.2 million in incremental annual revenue** for the UK market.

## Tools Used
* **Python:** Pandas, Scipy, Statsmodels
* **Visualization:** HTML/CSS Dashboard
* **AI:** Synthetic data generation logic
