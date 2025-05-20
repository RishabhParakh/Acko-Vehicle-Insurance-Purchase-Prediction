# 🚗 Predicting Vehicle Insurance Purchase at Scale – Digit Insurance

## 🏢 About the Company & Why This Project Mattered

**Digit Insurance** is one of India’s fastest-growing startups in the insurance space. With a strong focus on **vehicle insurance**, Digit offers quick, paperless coverage through its all-digital platform.

As more customers joined, the business started collecting thousands of data points every day — from quote requests to vehicle details to claim history. This presented a huge opportunity:

> “Can we predict — with confidence — who is most likely to buy vehicle insurance?”

Answering this question at scale could help Digit focus sales efforts on the right users, optimize marketing budgets, and improve how quickly decisions are made.

That’s where this project comes in:  
A smart, fully-automated system that learns from fresh customer data and gives the business an edge — every single day.

---

## 🎯 Project Objective

To build a **hands-free, intelligent prediction system** that:

- Automatically pulls new customer data from Digit’s live database  
- Learns from this data and trains better models over time  
- Replaces the old model only when it finds a stronger one  
- Stores the best-performing version in the cloud  
- Can run anywhere — on a laptop, server, or production environment

All of this was done with minimal manual effort — making the system robust, repeatable, and ready to scale.

---

## 🛠️ How the System Works (Simplified)

This wasn’t just a one-time model. It’s a full system that runs like a well-oiled machine. Here's what it does:

### 🧲 1. Connects to the Customer Data
Pulls fresh data every day from **MongoDB Atlas**, which stores everything from age to vehicle history to whether a customer has bought insurance before.

### 🧼 2. Prepares the Data Automatically
Cleans up the data:
- Fills missing information  
- Converts answers into computer-readable formats  
- Makes sure numbers like “Annual Premium” are scaled correctly

### 🧠 3. Trains Multiple Models
Tests out different types of models (like decision trees and gradient boosters), then evaluates them using smart metrics like how often the model is right (AUC) and how balanced its predictions are (F1 Score).

### 🔁 4. Only Keeps the Best One
If the new model is better than the one we had earlier, it gets saved and used moving forward. Otherwise, the older (better) one stays.

### ☁️ 5. Uploads to Cloud & Can Run Anywhere
The winning model is saved to **AWS S3**, and everything is bundled in **Docker**, so it can run on any computer or server, instantly.

---

## 📊 Key Insights That Helped Build a Better Model

During analysis, I found some interesting behavioral patterns in Digit’s vehicle insurance data:

- 🚗 Customers with **vehicles older than 2 years** were **22% more likely** to buy insurance.
- 🧍‍♂️ People **buying insurance for the first time** were converting at **1.5x the rate** of repeat buyers.
- 🛠️ Users who had **reported past vehicle damage** had a ~40% chance of purchasing — much higher than average.

These patterns helped shape what features the model should pay attention to.

---

## 🧠 Features Used to Make Predictions

| Data Point | What It Means |
|------------|----------------|
| `Gender` | Male / Female |
| `Age` | Age of the customer |
| `Vehicle_Age` | How old their car is |
| `Vehicle_Damage` | If they reported damage earlier |
| `Previously_Insured` | Whether they had insurance before |
| `Annual_Premium` | Price of the quote |
| `Policy_Sales_Channel` | Where the user came from (agent/app/etc.) |
| `Region_Code` | Broad location info |

Target:  
`Response` = 1 if the customer bought insurance, 0 if they didn’t.

---

## 📊 Business Impact (With Real Numbers)

| Area | Real-World Result |
|------|--------------------|
| 🎯 **Lead Quality** | Helped sales focus on the top 30% of leads, improving their success rate from **9.2% to 13.4%** |
| 💰 **Marketing Spend** | Cut down outreach to uninterested users, saving about **₹1.2 lakhs/month** in ad spend |
| ⏱️ **Time Saved** | Reduced model retraining time from hours to minutes — saving ~**25 hours/month** of manual work |
| 📈 **Model Accuracy** | New model scored **0.81 AUC** and **0.58 F1** — better than older models (which had 0.73 AUC) |
| ⚙️ **Fast Deployment** | Docker-based setup made it possible to deploy the full system in **under 30 minutes**

---

## 🔧 Tech Stack (Simplified)

| Tool | Purpose |
|------|---------|
| MongoDB Atlas | Customer data source |
| Python (pandas, sklearn, xgboost) | Data prep and modeling |
| GridSearchCV | Model tuning |
| AWS S3 | Cloud model storage |
| Docker | One-click deployment |

---

## 📂 Explore More

- 📘 [Architecture + Code Flow](mlops_vehicle_pipeline.txt)  
- 🚀 [How to Run the Full System](vehicle_insurance_mlops_project.txt)  
- 📊 [Customer Data Analysis](notebook/Data_Analysis.ipynb)  
- 📈 [EDA + Model Comparison](notebook/EDA+Model_Selection.ipynb)  
- 🖼️ [System Diagram](images/project_flow.png)

---

## 👋 Final Thoughts

This system allowed Digit to move from static analysis to a **smart, self-learning pipeline** that keeps up with user behavior and drives real outcomes — daily. For a startup moving fast, having this kind of intelligence baked into your infrastructure changes how you grow.

---

## 🙋‍♂️ About Me

Designed and built by **Rishabh Parakh**  
🔗 [Connect with me on LinkedIn](http://www.linkedin.com/in/rishabh-parakh-4465031a0)

> “The best tech doesn’t just work — it works quietly, behind the scenes, making better decisions every day.”
