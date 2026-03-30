# AI/ML Technical Challenge: Mobile App Security Predictive Analysis

## **Overview**
This challenge evaluates your ability to explore an unknown security dataset, perform complex data engineering, and build predictive models that translate raw technical metrics into global security insights. 

You are provided with **`archive.zip`**. There is no supplemental documentation. Your first task is to explore the data structures and determine how to link app-level findings to geographic and category-level metadata.

---

## **The Tasks**

You are required to submit **two separate Python notebooks** (`.ipynb`) addressing the following objectives:

### **Task 1: Geo-Security Risk Modeling**
**Objective:** Predict the security posture of a country/region based on the apps that interact with it.
* **Discovery:** Identify how to map applications to specific countries (e.g., via network telemetry, GeoIP, or developer metadata).
* **Metrics:** Derive a "Country Security Score." You must decide how to weight this (e.g., by traffic volume, app prevalence, or severity of findings).
* **Modeling:** Build a temporal model to forecast these scores. 
* **Requirement:** Perform a 10-week forecast and visualize the **Accuracy Degradation** (how the model's error compounds as the forecast horizon extends).

### **Task 2: App Category & Market Dynamics**
**Objective:** Predict individual app security scores using category identity and market influence.
* **Discovery:** Locate the features defining an app's "Category" (e.g., Social, Finance, Games) and its "Rank" or "Reach."
* **Cross-Sectional Modeling:** Predict specific app scores using category and ranking as primary features.
* **Temporal Modeling:** Track and predict how category-level security benchmarks evolve week-over-week.
* **Requirement:** Use feature importance analysis to determine if an app's **Category** is a stronger predictor of security than its **Market Rank**.

---

## **Submission Requirements**
1.  **Exploratory Data Analysis (EDA):** Your notebooks must clearly show your process for discovering the relationships between the files in `archive.zip`.
2.  **Feature Engineering:** Demonstrate how you handled temporal data (lags, rolling averages) and categorical variables.
3.  **Validation:** Ensure your training/testing splits respect the chronological order of the data (no future-leakage).
4.  **Executive Summary:** A brief write-up at the end of each notebook explaining your data mapping choices and the "Why" behind your model's predictions.
