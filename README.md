# 📊 Telecom Marketing Campaign Analysis  
**Customer Subscription Prediction & Segmentation Using Data Analytics**

## 📌 Project Overview
In highly competitive telecom and financial markets, marketing campaigns are costly and often inefficient when customers are poorly targeted. This project applies **data analytics and machine learning techniques** to analyse a telecom marketing dataset and identify the **key drivers of customer subscription behaviour**.

The analysis combines **exploratory data analysis (EDA), predictive modelling, and customer segmentation** to help organisations optimise marketing strategies, reduce wasted outreach, and improve return on marketing investment (ROMI).

---

## 🎯 Business Problem
A telecom organisation launched multiple marketing campaigns to promote a subscription product. Despite high outreach efforts, conversion rates remained low.

### Key Challenges:
- Inefficient customer targeting  
- High operational cost from repeated contacts  
- Highly imbalanced data (few subscribers)  
- Limited understanding of what drives customer decisions  

This project addresses these challenges through data-driven insights and predictive modelling.

---

## ❓ Research Questions
1. How does **communication type** (cellular vs telephone) affect subscription rates?
2. How does the **outcome of previous campaigns** influence future subscriptions?
3. Does **contact frequency** increase or reduce subscription probability?
4. Which **customer segments** show the highest likelihood of subscribing?
5. Which model best predicts customer subscription behaviour?

---

## 🗂️ Dataset Description
- **Source:** Telecom marketing campaign dataset  
- **Target Variable:** `subscribed` (1 = Yes, 0 = No)  
- **Feature Categories:**
  - Demographics (age, job, education, marital status)
  - Campaign history (previous outcome, contact count, call duration)
  - Economic indicators (employment rate, Euribor, consumer confidence)
  - Communication details (contact type, campaign month)

A detailed explanation of variables is provided in `Data_dictionary.xlsx`.

---

## 🧹 Data Preprocessing & Feature Engineering
The dataset required extensive preparation before modelling:

- Fixed formatting and structural inconsistencies
- Renamed target variable (`y` → `subscribed`)
- Handled **“unknown” values** using logical and statistical imputation
- Treated outliers using percentile capping (winsorisation)
- Addressed **class imbalance** (~11% subscribers)
- Created new features:
  - `prev_contact` (prior engagement indicator)
  - Interaction terms (`duration_age`, `duration_campaign`)
- Applied **one-hot encoding** to categorical variables
- Selected features using **Chi-Square and ANOVA tests**

---

## 🔍 Exploratory Data Analysis (EDA)
Key findings from EDA:

- **Cellular communication** resulted in nearly **3× higher subscription rates** than telephone calls
- Customers with **successful previous campaigns** had the highest conversion probability
- Subscription rates peak with **1–3 contacts** and decline sharply with excessive follow-ups
- Strong correlations among economic variables guided feature selection

---

## 🤖 Modelling Approach

### 1️⃣ Logistic Regression
- Interpretable and statistically transparent
- Identifies marginal effects of customer and campaign features
- Useful for strategic and policy-level decisions

### 2️⃣ Bayesian Logistic Regression
- Incorporates uncertainty and prior information
- Reduces overfitting in imbalanced datasets
- Suitable when missing potential subscribers is costly

### 3️⃣ Random Forest Classifier
- Captures complex non-linear relationships
- Achieved the highest predictive performance
- Provides feature importance for actionable insights

---

## 📈 Model Performance Summary

| Model | ROC-AUC | Accuracy | Recall | F1-Score |
|------|--------|---------|--------|---------|
| Logistic Regression | ~0.94 | 0.87 | Moderate | 0.61 |
| Bayesian Logistic Regression | ~0.93 | 0.87 | High | 0.60 |
| **Random Forest** | **0.95** | **0.89** | **0.89** | **0.64** |

- **Random Forest** maximises conversion potential  
- **Logistic models** provide interpretability and business insight  

---

## 🧠 Customer Segmentation (Clustering)
K-Means clustering (`k = 4`) was used to identify customer segments:

1. **Young Professionals** – early-career, moderate engagement  
2. **Mid-Career Customers** – stable income, mixed response  
3. **Retirees** – stable behaviour, high reliability  
4. **High-Value Customers** – highly engaged, highest subscription likelihood  

PCA was applied for cluster visualisation and interpretability.

---

## 💡 Key Business Insights
- Prior campaign success is the strongest predictor of future subscriptions
- Cellular outreach significantly outperforms telephone communication
- Excessive follow-ups reduce subscription probability due to customer fatigue
- Combining predictive modelling with segmentation improves marketing ROI
- Model-driven targeting reduces operational cost and improves efficiency

---

## 🛠️ Tools & Technologies
- **Python:** pandas, numpy, matplotlib, seaborn, scikit-learn
- **Machine Learning:** Logistic Regression, Bayesian Models, Random Forest
- **Clustering:** K-Means, PCA
- **Evaluation:** ROC-AUC, Precision–Recall, Confusion Matrix
- **Environment:** Jupyter Notebook

---

## 🚀 How to Run the Project
1. Clone this repository
2. Install required Python libraries (`pandas`, `scikit-learn`, `matplotlib`)
3. Open `Marketing_Campagin.ipynb`
4. Run all cells sequentially to reproduce the analysis

---

## 📊 Results
- The convergence of **Logistic Regression** interpretability and **Random Forest** predictive strength provided a dual-lens perspective on campaign effectiveness.
- Logistic and Bayesian models offered strategic transparency by explaining how key factors such as call duration, prior campaign success, and economic stability influence subscription decisions.
- The Random Forest model delivered superior predictive performance, enabling accurate identification of high-potential subscribers and improving campaign efficiency.
- Together, these models balance **explainability and performance**, supporting both short-term optimisation and long-term strategic planning.

---

## 🤝 Contributing
Contributions to this project are welcome.  
If you have suggestions for improvements, enhancements, or alternative modelling approaches, feel free to:

1. Fork the repository  
2. Create a new branch  
3. Commit your changes  
4. Submit a pull request  

All contributions that improve clarity, performance, or usability are appreciated.

---

## 📜 License
This project is licensed under the **MIT License**.  
You are free to use, modify, and distribute this project with appropriate attribution.

---

## 📬 Contact
For any queries or discussions regarding this project, feel free to reach out:

📧 **Email:** rathore10.sonu@gmail.com
