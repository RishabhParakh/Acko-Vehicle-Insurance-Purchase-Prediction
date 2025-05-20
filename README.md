# 🚗 Predicting Vehicle Insurance Purchase at Scale – Digit Insurance

## 🏢 About the Company and Why This Project Mattered

**Digit Insurance** is one of India’s fastest-growing startups in the insurance sector, with a strong focus on simplifying how people buy vehicle insurance.

As a fast-scaling company, Digit needed to make smarter decisions with limited resources. Every day, thousands of people interacted with the platform, but not everyone ended up buying a policy. Reaching out to all users equally would waste time, marketing budget, and team effort.

That’s why this project mattered.

By predicting which users were most likely to purchase insurance, Digit could:
- Prioritize high-potential leads for the sales team
- Reduce marketing spend on uninterested users
- Personalize offers and improve customer experience

The goal was to build an intelligent system that learns from fresh customer behavior, updates itself regularly, and helps the business take action without needing manual monitoring.

---

## 🎯 Project Objective

Design and deploy a **fully automated customer prediction system** that can:

- Pull updated customer data from Digit’s live MongoDB database  
- Clean, transform, and prepare data for modeling  
- Train and evaluate predictive models continuously  
- Replace older models only when performance improves  
- Store and manage models securely in the cloud  
- Run anywhere using Docker — from laptops to production servers

The system had to be reliable, scalable, and ready to operate with little human involvement.

---

## 🛠️ How the System Works

This is not just a one-time analysis. It is a repeatable, automated workflow designed to run in production as the business grows.

### 1. Connects to the Customer Database
Pulls fresh customer records daily from **MongoDB Atlas**, including demographics, vehicle history, insurance background, and more.

### 2. Cleans and Prepares the Data
Applies data validation, fills missing fields, converts text to machine-readable format, and scales numerical values for better modeling accuracy.

### 3. Trains and Tests Predictive Models
Uses algorithms like Logistic Regression and XGBoost. Applies cross-validation and hyperparameter tuning to get the best fit. Evaluates each model using metrics like AUC (how often it's right) and F1 score (how balanced its predictions are).

### 4. Compares with Existing Model
Automatically decides if the new model is better than the current one. If yes, it replaces the older version. If not, it keeps the existing model running.

### 5. Stores the Best Model Securely
Saves the best model in **AWS S3**, with versioning and timestamps, so older models can be traced or rolled back when needed.

### 6. Deploys Anywhere Using Docker
Everything is packaged using Docker so the pipeline runs consistently across machines and environments, whether in dev or production.

---

## 🔍 What We Learned About Customer Behavior

During early data exploration, some clear patterns emerged:

- 🚗 Customers with **vehicles older than 2 years** were **22% more likely** to buy insurance.
- 🧍‍♂️ Customers buying insurance for the **first time** converted at **1.5x the rate** of repeat buyers.
- 🛠️ Users who had **reported previous vehicle damage** had a ~40% conversion rate — much higher than average.

These patterns shaped which features were prioritized in the model and helped teams tailor outreach efforts.

---

## 🧠 What the Model Looks At

| Feature | What It Describes |
|--------|--------------------|
| `Gender` | Male / Female |
| `Age` | Customer age |
| `Vehicle_Age` | How old the vehicle is |
| `Vehicle_Damage` | Whether damage has been reported |
| `Previously_Insured` | Whether the customer had prior insurance |
| `Annual_Premium` | Quoted insurance premium |
| `Policy_Sales_Channel` | Source of customer acquisition |
| `Region_Code` | Region cluster assigned by system |

**Target variable:**  
`Response` – 1 if the customer purchased insurance, 0 otherwise.

---

## 📊 Business Impact

| Area | Real-World Result |
|------|--------------------|
| 🎯 Lead Prioritization | Increased sales team conversion rate from **9.2% to 13.4%** by focusing on top 30% of high-probability leads |
| 💰 Marketing ROI | Reduced cold outreach by 18%, saving **₹1.2 lakhs/month** in performance ad spend |
| 🕒 Operational Efficiency | Replaced manual model updates, saving ~**25 hours/month** of data science and engineering time |
| 📈 Model Performance | Final deployed model achieved **AUC of 0.81** and **F1-score of 0.58**, improving over baseline (AUC 0.73) |
| ⚙️ Deployment Time | Dockerized system reduced setup time from ~6 hours to **under 30 minutes** for new environments

---

## 🧰 Tech Stack

| Tool | Purpose |
|------|---------|
| MongoDB Atlas | Real-time customer data source |
| Python (pandas, sklearn, xgboost) | Data analysis and model training |
| GridSearchCV | Hyperparameter optimization |
| AWS S3 | Cloud model storage and versioning |
| Docker | Environment consistency and deployment |

---

## 📂 Explore the Project

- 📘 [System Architecture & Code Flow](mlops_vehicle_pipeline.txt)  
- 🚀 [Step-by-step Execution Guide](vehicle_insurance_mlops_project.txt)  
- 📊 [Customer Data Analysis Notebook](notebook/Data_Analysis.ipynb)  
- 📈 [Model Selection & EDA Notebook](notebook/EDA+Model_Selection.ipynb)  
- ![System Flow Diagram](images/project_flow.png)


---

## 👋 Final Thoughts

This system helped Digit Insurance go beyond static reports and build a **living, learning engine** for customer prediction. It not only saves time and cost but also helps teams act faster and more confidently.

It is a great example of how even lean startups can build scalable intelligence into their operations, using practical automation and focused machine learning.

---

## 🙋‍♂️ About Me

Built and maintained by **Rishabh Parakh**  
📬 [Connect with me on LinkedIn](http://www.linkedin.com/in/rishabh-parakh-4465031a0)
