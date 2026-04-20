# Actuarial Mortality Benchmarking & Risk Sensitivity Engine
### Analyzing the Transition from RP-2014 to PubG-2010

## 📌 Executive Summary
This project quantifies the financial and demographic impact of updating mortality assumptions from the legacy **RP-2014** (private sector) to the modern **PubG-2010** (public sector) standards. 

Using Python, I developed a valuation engine that stitches distinct life-stage datasets to create a continuous Age 18–120 mortality profile. The model identifies significant longevity gains in public-sector populations and evaluates portfolio sensitivity to interest rate and mortality shocks.

## 🛠️ Technical Implementation
* **Table Stitching:** Merged Employee and Retiree datasets at Age 50 to resolve the "Healthy Worker Effect" and data availability floors.
* **Actuarial Metrics:** Vectorized calculation of survivors ($l_x$), life expectancy ($e_x$), and Net Single Premiums ($A_x$).
* **Stress Testing:** Conducted a 45-scenario sensitivity analysis across interest rate shifts (±200bps) and mortality loading (±20%).

## 📊 Key Insights
### 1. The Longevity Gap
The survival curve ($l_x$) comparison indicates that public sector employees (PubG-2010) exhibit higher longevity than the private sector baseline. 
**Impact:** A **7-9% increase** in required reserves ($A_x$) for retirement-age cohorts.

<img width="880" height="549" alt="curve" src="https://github.com/user-attachments/assets/5ac34cff-dece-489c-97e6-14f52d483cf3" />


### 2. Risk Sensitivity
The multivariate heatmap shows that **Interest Rate Risk** is the primary driver of liability volatility.
**Impact:** A **100bps drop** in interest rates creates a **15x greater financial liability** than a **10% surge** in mortality.

<img width="921" height="645" alt="heatmap" src="https://github.com/user-attachments/assets/6584df8d-c7df-45f7-81fc-57be5f6a29f0" />


## 🚀 Conclusion
For the modeled block of business, longevity risk is increasing, but market risk (interest rates) remains the dominant threat to solvency. This project demonstrates the critical need for robust Asset-Liability Matching (ALM) alongside updated mortality assumptions.

---
**Tech Stack:** Python (Pandas, NumPy, Seaborn, Matplotlib)
**Data Source:** Society of Actuaries (SOA) MORT Database
