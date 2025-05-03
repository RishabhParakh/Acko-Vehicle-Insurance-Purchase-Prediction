# 🚗 Acko General Insurance – Vehicle Insurance Purchase Prediction

## 🏢 About the Company & Problem Context

**Acko General Insurance** is one of India’s leading digital-first insurers, known for offering fast, paperless, and personalized vehicle insurance services across the country.

In 2022, Acko collected a significant amount of customer data from its platform. With this dataset, the company wanted to:
- Analyze customer behavior
- Identify which types of customers were most likely to buy vehicle insurance
- Build a predictive model to estimate the likelihood of purchase for each customer

However, Acko’s customer base is dynamic — new users join daily, and existing user behavior continues to evolve. Their data infrastructure is built on **MongoDB**, which updates in real-time as customers interact with the system.

This led to a **critical business need**:  
> Acko required a **scalable, automated machine learning solution** that could:
> - Continuously ingest updated customer data from MongoDB  
> - Automatically validate, process, and train predictive models  
> - Serve real-time predictions to internal teams via an API  
> - Replace older models with newer ones when performance improves  

---

## ✅ Why This Project Was Necessary

This project addresses both **current and future needs** of the company:
- In the short term, I delivered **actionable insights** from the 2022 data and built a **high-performing model** to predict customer purchase intent.
- In the long term, I developed a **fully automated machine learning pipeline** that retrains models on new data and serves predictions in real time — without any manual intervention.

The pipeline integrates seamlessly with MongoDB and AWS, making it **cloud-ready, self-improving, and scalable** to support Acko's growth.

What started as a data analysis exercise evolved into a complete ML engineering and deployment solution — tailored to Acko’s real-world operational needs.

---

## 📁 Project Overview

The project is divided into two core phases:

---

## 📊 Phase 1: Data Analysis, EDA & Model Selection

**Objective**  
Analyze 2022 customer data to identify behavior patterns and build a prediction model to estimate which customers are likely to buy vehicle insurance.

**Approach**  
I performed a detailed exploration of the customer dataset, focusing on features such as gender, vehicle age, insurance history, and past vehicle damage. I cleaned the data, visualized key trends, handled class imbalance, and trained multiple models to evaluate performance using accuracy and AUC.

**Key Insights**
- **Gender:** Male customers were more likely to purchase insurance.
- **Vehicle Age:** Older vehicles (2+ years) had higher insurance purchase rates.
- **Previous Insurance:** First-time buyers showed greater purchase interest.
- **Vehicle Damage History:** Damaged vehicle owners were more inclined to purchase.

### 📸 Visual Highlights

- <img src="images/Gender_Distribution.png" width="300"/>
- <img src="images/Insurance_buyers_vehicle_damage_status.png" width="300"/>
- <img src="images/Insurance_purchase_by_vehicle_age_category.png" width="400"/>
- <img src="images/Insurance_purchase_rates_based_on_previous_coverage.png" width="400"/>

👉 [Click here for full EDA notebook](notebook/Data_Analysis.ipynb)  
👉 [Click here for model selection notebook](notebook/EDA+Model_Selection.ipynb)

---

## ⚙️ Phase 2: Production-Ready Machine Learning Pipeline

**Objective**  
To automate the prediction workflow, ensuring the model can ingest real-time data, retrain when necessary, and serve predictions reliably at scale.

**Architecture Overview**  
The system includes the following components:
- MongoDB Atlas for live customer data
- Data validation, transformation, and preprocessing modules
- Model training and evaluation logic with automatic version comparison
- AWS S3 for storing production models
- Flask API to serve real-time predictions
- Docker for consistent deployment across environments

### 🧱 Pipeline Highlights

- 🔄 Auto-ingests data from MongoDB  
- 🧹 Cleans and prepares it for modeling  
- 📊 Evaluates and compares model performance  
- ☁️ Pushes best model to AWS S3  
- 🌐 Serves predictions via Flask API  
- 📦 Dockerized for scalable deployment  

![Project Flow](images/project_flow.png)

---

## 📄 Technical Documentation

👉 [Click here to view the technical explanation](mlops_vehicle_pipeline.txt)

---

## 🚀 Step-by-Step Execution Guide

👉 [Click here for step-by-step instructions](vehicle_insurance_mlops_project.txt)

---

## 🎯 Business Value & Impact

- 📈 **Smarter Targeting:** Prioritizes top 20–25% high-intent leads, increasing conversion rate and reducing cost per acquisition.  
- 💰 **Better ROI:** Campaigns tailored to first-time buyers and owners of older/damaged vehicles expected to improve ROI by 30–40%.  
- 🔁 **Self-Updating Models:** Retrains and replaces models automatically, keeping performance sharp.  
- 📊 **Instant Decisioning:** Real-time predictions improve customer interaction and upsell timing.  
- ☁️ **Cloud-Ready & Scalable:** Integrated with AWS and MongoDB for reliable and efficient operations.

This project enables Acko to make data-backed marketing and product decisions in real time.
