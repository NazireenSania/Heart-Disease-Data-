# ❤️ Heart Disease Analysis – Power BI Dashboard

This project explores the key factors contributing to heart disease using a structured dataset and presents insights through interactive Power BI visualizations. It also builds a simple **Risk Scoring Model** based on normalized data to predict heart disease likelihood.

## 📌 Project Overview

- 📁 **Tool Used:** Microsoft Power BI
- 📄 **Dataset Size:** 1,026 rows × 14 columns
- 📊 **Data Source:** Structured medical dataset containing health metrics and heart disease status

---

## 🎯 Objectives

1. Visualize key health metrics and their correlation with heart disease.
2. Normalize data across different scales to prepare for modeling.
3. Create a risk scoring model using weighted factors and DAX calculations.
4. Identify patterns among age, cholesterol, heart rate, and diagnostic readings.
5. Help predict high-risk individuals based on metric aggregation.

---

## 🧪 Methodology

- Cleaned the dataset (no missing/null values).
- Created **heatmaps, bar charts, and line charts** to analyze:
  - Age groups with high correlation to heart disease (especially ages 40–60)
  - Impact of chest pain types, resting ECG results, and cholesterol
  - Gender-wise and exercise-induced angina impact on heart disease likelihood

### 🧮 Risk Score Calculation

Used DAX to create a **calculated column** aggregating multiple risk factors:
- Age
- Cholesterol
- Resting Blood Pressure
- Maximum Heart Rate Achieved
- Chest Pain Type
- Slope of ST Segment
- Thalassemia
- Resting ECG
- Fasting Blood Sugar
- Exercise-Induced Angina

All numeric factors were **normalized** using the formula:
```DAX
Normalized_Age = ([Age] - MIN([Age])) / (MAX([Age]) - MIN([Age]))
