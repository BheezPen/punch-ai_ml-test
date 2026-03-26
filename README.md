# Technical Challenge: Mobile App Security Predictive Analysis

## **Overview**
This challenge evaluates an AI/ML engineer's ability to process raw security data, perform feature engineering, and build predictive models that translate technical metrics into business insights. You will be analyzing a dataset of mobile application security audits to predict security postures across global markets and app categories.

---

## **Dataset Information**
The provided **`Security Data.zip`** contains granular security metrics for thousands of iOS and Android applications. Key data points include:

* **App Metadata:** `app_name`, `bundle_id`, `category` (Social, Productivity, Finance, etc.), `os`.
* **Geographic Data:** `country_origin` (US, China, France, etc.), `data_residency_region`.
* **Security Metrics:** `num_dangerous_permissions`, `uses_encryption` (Bool), `vulnerability_count`, `tracker_count`.
* **Target Variable:** `security_score` (Numerical 0–100, where 100 is most secure).

---

## **The Tasks**

You are required to submit **two separate Python notebooks** (`.ipynb`) addressing the following objectives:

### **Task 1: Predictive Modeling by Country**
**Objective:** Predict the `security_score` based on an app's country of origin and regional data handling.
* **EDA:** Visualize the distribution of security scores across key regions (focus on **US, China, and France**).
* **Feature Engineering:** Encode categorical country data and identify if regional regulations (e.g., GDPR) correlate with higher scores.
* **Modeling:** Build a regression or classification model (e.g., Random Forest, XGBoost).
* **Insight:** Identify which countries consistently produce the highest and lowest security risks.

### **Task 2: Predictive Modeling by App Category**
**Objective:** Predict the `security_score` based on the App Store category.
* **Category Analysis:** Compare security benchmarks for sectors like **Entertainment, Music, Social, and Productivity**.
* **Data Imbalance:** Address discrepancies in sample sizes (e.g., "Games" vs. "Finance").
* **Modeling:** Train a model to find category-specific vulnerabilities (e.g., do Social apps leak more PII via permissions?).
* **Insight:** Determine if an app’s category is a statistically significant predictor of risk regardless of geography.

---

## **Submission Requirements**
1.  **Code Quality:** Clean, commented Python code in Jupyter Notebook format.
2.  **Visualizations:** Use `matplotlib` or `seaborn` to illustrate feature importance and error distributions.
3.  **Executive Summary:** A brief write-up at the end of **each** notebook explaining:
    * Which features were the most predictive?
    * How you would improve the model with live telemetry data.
    * Any surprising trends
