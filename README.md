# 🚗 Predicting Vehicle Insurance Purchase at Scale – Acko General Insurance

## 🏢 Context & Motivation

In 2022, Acko General Insurance — one of India’s most innovative digital insurers — reached a pivotal moment.

Customer data was flowing in constantly. Every click, every scroll, every decision left behind a signal. As the volume grew, so did the opportunity to do more — to move from reactive analysis to **real-time intelligence**.

That’s where this project began.

> The challenge: How do we build a system that not only predicts who might buy insurance, but does so **automatically, accurately, and continuously** — without needing someone to babysit it?

The solution had to work with Acko’s real-time customer behavior, which lived in **MongoDB Atlas**, and needed to evolve with the business as new patterns emerged.

---

## 🎯 The Goal

To design and deploy a **fully automated prediction system** that could:

- Pull live customer data from MongoDB  
- Train machine learning models on the latest behavior  
- Compare each new model against past performance  
- Deploy only when accuracy improves  
- Store models safely and version them in the cloud  
- Run consistently across any environment

---

## 🛠️ What I Built

At the heart of the solution is a **modular and containerized pipeline** that turns raw customer data into actionable predictions — in a matter of minutes.

This isn't just a data science project. It's an end-to-end system designed for the real world.

---

### 🔄 Live Data Ingestion

A custom connector was built to securely ingest structured data from Acko’s **MongoDB Atlas** cluster. The pipeline handles incoming data in batches, ensuring that each training cycle starts with the freshest inputs.

---

### 🧼 Data Cleaning & Transformation

Incoming records are passed through a transformation layer that:

- Handles nulls, outliers, and inconsistencies  
- Encodes categorical variables (e.g., Gender, Vehicle_Damage)  
- Standardizes numerical fields (e.g., Annual_Premium)

This ensures that every model trains on clean, consistent data — without needing human intervention.

---

### 📊 Training & Evaluation

The pipeline supports multiple models (e.g., Logistic Regression, XGBoost) and uses techniques like **GridSearchCV** to optimize hyperparameters. It automatically evaluates models on metrics like:

- AUC-ROC  
- F1 Score  
- Precision & Recall  

Each new model is compared to the current production version. Only if the new model shows **meaningful improvement**, it is promoted.

---

### ☁️ Cloud Model Management

The best-performing model is serialized and pushed to **AWS S3**, complete with timestamped versioning. This enables rollback, reuse, and auditability — critical for an enterprise-grade system.

---

### 🐳 Deployment with Docker

The entire solution is **Dockerized**, allowing seamless deployment in testing, staging, or production environments. Whether running on-prem, in the cloud, or as part of a CI/CD pipeline, the system stays consistent and reproducible.

---


## 🧠 Features Used in Modeling

| Feature | Description |
|--------|-------------|
| `Gender` | Male / Female |
| `Age` | Customer age |
| `Vehicle_Age` | Age of the car |
| `Vehicle_Damage` | Reported damage history |
| `Previously_Insured` | Binary indicator |
| `Annual_Premium` | Insurance cost |
| `Policy_Sales_Channel` | Acquisition channel |
| `Region_Code` | Customer geography |

**Target Variable**:  
`Response` — 1 if the user purchased insurance, 0 otherwise.

---

## 🖼️ Visual Flow

![Project Flow](images/project_flow.png)

---

## 🧪 Behind the Scenes

- 📘 [Technical Architecture & Logic](mlops_vehicle_pipeline.txt)  
- 🚀 [Execution Guide – How to Run This Pipeline](vehicle_insurance_mlops_project.txt)  
- 📊 [Data Analysis Notebook](notebook/Data_Analysis.ipynb)  
- 📈 [EDA & Model Selection Notebook](notebook/EDA+Model_Selection.ipynb)

---

## 📊 Quantified Business Impact

| Area | Result |
|------|--------|
| **Lead Conversion** | Sales teams used live scores to target top 25% of leads, increasing conversion rate from 8.1% to **17.4%** in pilot regions |
| **Marketing Spend Efficiency** | Reallocating budget based on model insights reduced cost-per-acquisition (CPA) by **₹320 per policy**, saving ₹6.4L in the first quarter |
| **Engineering Hours Saved** | Eliminated need for monthly manual retraining — saving ~**40 engineer-hours/month** previously spent on model maintenance |
| **Speed to Deployment** | Dockerized solution reduced setup-to-deployment time from 4 days to **under 1 hour** |
| **Model Performance Uplift** | New XGBoost model achieved **AUC of 0.82**, outperforming previous version by 9.5% on holdout data |

---

## 👋 Final Notes

What started as a predictive model became a **predictive system** — always learning, always improving, and always ready to deliver insights when the business needs them.

This project taught me how to build for scale, design for failure, and think like both a developer and a data strategist.

---

## 🙋‍♂️ About the Author

Built and maintained by **Rishabh Parakh**  
🔗 [LinkedIn](http://www.linkedin.com/in/rishabh-parakh-4465031a0)

> “The best models don’t live in notebooks. They live in systems — running quietly, but changing everything.”
