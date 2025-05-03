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
> - Replace older models with newer ones when performance improves  

---

## ✅ Why This Project Was Necessary

This project addresses both **current and future needs** of the company:
- In the short term, I delivered **actionable insights** from the 2022 data and built a **high-performing model** to predict customer purchase intent.
- In the long term, I developed a **fully automated machine learning pipeline** that retrains models on new data and keeps performance consistently high without manual intervention.

---

## 📁 Project Overview

The project is divided into two core phases:

---

## 📊 Phase 1: Data Analysis, EDA & Model Selection

**Objective**  
Analyze 2022 customer data to identify behavior patterns and build a prediction model to estimate which customers are likely to buy vehicle insurance.

### 🔢 Features Used in the Model
- `Gender`
- `Age`
- `Vehicle_Age`
- `Vehicle_Damage`
- `Previously_Insured`
- `Annual_Premium`
- `Policy_Sales_Channel`
- `Region_Code`

### 🎯 Target Variable
- `Response`: 1 if the customer purchased insurance, 0 otherwise.

---

## 🔍 Key Insights from 2022 Customer Data

As part of Phase 1, I performed a detailed exploratory data analysis on Acko's 2022 customer dataset. The goal was to identify patterns in customer behavior that could influence insurance purchase decisions. Here are the most impactful insights uncovered:

---

### 1. 🚹 Gender Patterns in Purchase Behavior

While both genders were active on the platform, **male customers were more likely to complete a purchase**.

<img src="images/Gender_Distribution.png" width="300"/>

➡️ **Business takeaway:** Tailor messaging and offers to align with conversion behaviors across genders — e.g., highlight security or pricing differently.

---

### 2. 🚗 Vehicle Age Strongly Influences Interest

Customers with **vehicles older than 2 years** were significantly more likely to purchase insurance.

<img src="images/Insurance_purchase_by_vehicle_age_category.png" width="400"/>

➡️ **Business takeaway:** Target older vehicle owners with maintenance-inclusive insurance or long-term coverage options.

---

### 3. ❌ First-Time Insurance Buyers Are More Interested

Customers who had **never held a previous insurance policy** were more inclined to buy.

<img src="images/Insurance_purchase_rates_based_on_previous_coverage.png" width="400"/>

➡️ **Business takeaway:** Focus on onboarding and education strategies for first-time buyers.

---

### 4. 🛠️ History of Vehicle Damage is a Major Trigger

Customers who had reported **past vehicle damage** were strongly motivated to purchase coverage.

<img src="images/Insurance_buyers_vehicle_damage_status.png" width="300"/>

➡️ **Business takeaway:** Highlight real customer stories and repair cost savings in marketing to reinforce urgency.

---

👉 [Explore Data Analysis Notebook](notebook/Data_Analysis.ipynb)  
👉 [Explore EDA & Model Selection Notebook](notebook/EDA+Model_Selection.ipynb)

---

## ⚙️ Phase 2: Production-Ready Machine Learning Pipeline

**Objective**  
Build an automated and scalable prediction system that integrates with Acko's real-time customer database.

### 🔧 Architecture Includes:
- MongoDB Atlas for real-time data
- Data validation, transformation, and training modules
- Model evaluation and versioning
- AWS S3 for model storage
- Docker for consistent deployment

### 🧱 Pipeline Highlights

- 🔄 Auto-ingests data from MongoDB  
- 🧹 Cleans, validates, and transforms the data  
- 📊 Trains and evaluates ML models  
- ☁️ Pushes best model to AWS S3  
- 📦 Dockerized for easy deployment  

![Project Flow](images/project_flow.png)

---

## 📄 Technical Documentation

📘 Complete breakdown of components, architecture, and MLOps logic:  
👉 [View Technical Documentation](mlops_vehicle_pipeline.txt)

---

## 🚀 Step-by-Step Execution Guide

🛠️ End-to-end instructions to replicate, run, and deploy the full system:  
👉 [Read Execution Guide](vehicle_insurance_mlops_project.txt)

---

## 🎯 Business Value & Impact

This project delivered measurable results that directly benefited marketing, sales, and engineering operations:

---

### 1. 🏆 Higher Conversion from Targeted Leads  
By focusing on the top quartile of likely buyers, Acko improved policy conversions significantly without increasing outreach effort.

---

### 2. 💰 Smarter Marketing Spend  
Budget was refocused on high-intent segments (e.g., older vehicles, uninsured drivers), eliminating waste on cold leads and improving ad performance.

---

### 3. 🔁 Zero Manual Retraining  
The ML pipeline now handles retraining, validation, and deployment automatically — reducing engineering effort and downtime.

---

### 4. ⚡ Instant Lead Scoring  
The system delivers real-time predictions on updated data — enabling faster decisions, better customer targeting, and stronger campaign execution.

---

This solution empowers Acko to scale smarter — closing more sales, reducing overhead, and reacting to data faster than ever before.
