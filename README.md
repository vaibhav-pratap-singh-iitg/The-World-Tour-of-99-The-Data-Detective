# Crowd Energy Prediction & Revenue Optimization

This repository contains my solution for **Machine Learning Task 1 (Coding Week, IIT Guwahati)**. The objective is to predict **Crowd Energy (0–100)** for live music shows using noisy, real-world data and to perform **revenue optimization** for a specific venue.

---

## Problem Summary

The band *Electric Omen* plans a comeback tour and wants to:
- Predict crowd energy before shows
- Understand venue-specific behavior
- (Bonus) Find the ticket price that maximizes profit at **V_Gamma (The Snob Pit)**

The dataset is intentionally messy, containing missing values, mixed currencies, sensor glitches, and some insights from the lead singer. The task emphasizes **reasoning ,robustness and our approach**, not just model accuracy.

---

## Approach

- **Data Cleaning:** Currency normalization, date parsing, handling invalid target values, and avoiding data leakage.
- **EDA:** Tested singer’s claims as hypotheses; separated signal from noise (e.g., weather, moon phase).
- **Modeling:** Trained a **Random Forest Regressor** with cross-validation (RMSE ≈ 13.2), chosen for robustness to non-linearity and noise.
- **Feature Engineering:** Weekend indicators, cleaned volume levels, and non-linear price effects.

---

## Bonus: Revenue Optimization

For **V_Gamma**, profit was modeled as:
Profit = Ticket Revenue + Energy-dependent Merch Revenue − Fixed & Variable Costs
- Crowd energy is predicted using the trained ML model.
- Attendance is estimated via a simple linear regression on price and predicted energy.
- A profit-vs-price curve is generated to identify the optimal ticket price.

---

## Tools

Python, pandas, numpy, scikit-learn, matplotlib, seaborn

---

**Author:** Vaibhav Pratap Singh  
IIT Guwahati
