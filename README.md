# Ecommerce-RFM-Customer-Segmentation

**Project:** End-to-end customer segmentation using RFM analysis and K-Means clustering on e-commerce data.

**Author / Repository:** Harmanjot26 — *Ecommerce-RFM-Customer-Segmentation*

---

## Table of Contents

1. [Overview](#overview)
2. [Objective](#objective)
3. [Analysis Approach](#analysis-approach)
4. [Methodology](#methodology)
5. [Tools & Libraries](#tools--libraries)
6. [Project Structure](#project-structure)
7. [Results & Insights](#results--insights)
8. [Recommendations](#recommendations)
9. [Extending the Project](#extending-the-project)
10. [Contributing](#contributing)
11. [License & Contact](#license--contact)

---

## Overview

Olist is a newly launched e-commerce startup in Portugal that experienced rapid growth during the COVID-19 pandemic due to a surge in online shopping. However, Olist’s marketing strategy is not yet optimized — the company is not running **targeted marketing campaigns**, which increases costs as only a fraction of users return to the website.

This project demonstrates how **customer segmentation** can be applied to optimize marketing efforts and improve retention.

## Objective

The objective of this project is to help Olist increase its **marketing conversion rate** by applying **targeted marketing** strategies. By segmenting customers into meaningful groups, Olist can:

* Personalize communication
* Reduce marketing costs
* Improve retention and customer lifetime value (CLV)

## Analysis Approach

Customer segmentation is a powerful marketing tool that enables a business to better understand its customers and design personalized strategies for each group.

This project applies a two-step segmentation approach:

1. **RFM Analysis** — based on Recency, Frequency, and Monetary value of transactions.
2. **K-Means Clustering** — to identify natural clusters within RFM features and validate them with **Silhouette Analysis**.

## Methodology

The end-to-end process includes:

1. **Data Cleaning**

   * Handling missing values
   * Removing duplicates and cancelled transactions
   * Converting dates and fixing datatypes

2. **Exploratory Data Analysis (EDA)**

   * Understanding data distribution
   * Identifying top customers, sales trends, and anomalies
   * Visualizing transaction frequency, spending distribution, etc.

3. **RFM Analysis**

   * **Recency (R):** Number of days since the last purchase
   * **Frequency (F):** Number of transactions per customer
   * **Monetary (M):** Total spending per customer
   * Assigning scores (1–5) for R, F, and M, then creating an RFM table

4. **Clustering (K-Means)**

   * Applying K-Means clustering on scaled RFM values
   * Determining optimal cluster number using Elbow Method & Silhouette Score
   * Assigning customers to clusters

5. **Interpretation & Insights**

   * Labeling clusters (e.g., Champions, Loyal, At-Risk, Lost)
   * Analyzing segment characteristics
   * Recommending targeted marketing strategies

## Tools & Libraries

* **Python** (Google Colab environment)
* **Pandas** — data manipulation
* **NumPy** — numerical computations
* **Matplotlib & Seaborn** — data visualization
* **Scikit-learn** — clustering & scaling
* **SciPy** — statistical analysis
* **Silhouette Analysis** — cluster evaluation

## Project Structure

```
Ecommerce-RFM-Customer-Segmentation/
├─ data/                      # raw & cleaned datasets
├─ notebooks/                 # Jupyter notebooks
│  ├─ 01_data_cleaning.ipynb
│  ├─ 02_eda.ipynb
│  ├─ 03_rfm_analysis.ipynb
│  ├─ 04_kmeans_clustering.ipynb
│  └─ 05_insights_recommendations.ipynb
├─ reports/                   # visualizations & results
├─ requirements.txt
└─ README.md
```

## Results & Insights

After RFM scoring and K-Means clustering, customers were grouped into distinct segments:

* **Champions (High R, High F, High M):** Recently active, frequent buyers, top spenders.
* **Loyal Customers:** Frequent buyers with moderate to high spending.
* **Potential Loyalists:** New or recent customers showing promise.
* **At-Risk Customers:** Used to spend a lot but have not purchased recently.
* **Hibernating / Lost:** Long inactive customers with low frequency and spending.

## Recommendations

* **Champions:** Reward loyalty with exclusive offers, VIP programs, and upselling campaigns.
* **Loyal Customers:** Maintain engagement through newsletters, product recommendations, and referral programs.
* **Potential Loyalists:** Encourage repeat purchases with discounts or personalized suggestions.
* **At-Risk Customers:** Win-back campaigns, special discounts, and reminders.
* **Hibernating / Lost:** Low-cost reactivation campaigns, surveys to understand disengagement.

## Extending the Project

* Build an automated pipeline for **real-time RFM updates**.
* Use **advanced clustering (HDBSCAN, Gaussian Mixture Models)** for better segmentation.
* Integrate customer demographics and behavioral features.
* Deploy results into a **marketing dashboard (Streamlit/Power BI/Tableau)**.

## Contributing

Contributions are welcome. Suggested workflow:

1. Fork the repository
2. Create a new branch for your feature/fix
3. Commit changes with clear messages
4. Open a Pull Request

## License & Contact

This project is licensed under the MIT License. See `LICENSE` for details.

For questions, issues, or suggestions, please open an issue on GitHub.

---

*This README documents the complete process of customer segmentation with RFM and K-Means for e-commerce. It is designed for both reproducibility and extension for real-world marketing applications.*
