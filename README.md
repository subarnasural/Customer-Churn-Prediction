# Customer-Churn-Prediction
# Customer Upsell & Retention Classification using Machine Learning

## Project Overview
This project focuses on analyzing customer call behavior to predict churn probability and classify customers into meaningful business segments.  
Rather than limiting the scope to churn prediction alone, the system translates model outputs into **actionable customer categories** that can be directly used by business and marketing teams.

The final objective is to support **revenue growth and customer retention strategies** through data-driven decision making.

---

## Problem Statement
Telecommunication companies often lose customers due to dissatisfaction or better competitor offerings.  
The challenge is not only to identify customers likely to churn, but also to determine **how each customer should be approached**:

- Customers suitable for upselling
- Customers requiring monitoring
- Customers needing immediate retention actions

This project addresses that challenge using machine learning.

---

## Dataset Description
The dataset consists of customer call detail records, including:
- Account information
- Day, evening, night, and international call usage
- Customer service interaction history
- Churn indicator

Since multiple records existed per customer, the data was **aggregated at the customer level** using phone number as the unique identifier.

---

## Data Preprocessing and Feature Engineering
Key preprocessing steps include:
- Removal of duplicate records
- Aggregation of call-level data into customer-level features
- Conversion of target variable into binary format

New features engineered to improve model performance:
- Total minutes used across all call types
- Total number of calls
- Average calls per day based on account length
- High customer service interaction flag

These features help capture long-term customer behavior more effectively.

---

## Machine Learning Models Used
Multiple models were trained and evaluated for performance comparison:

- XGBoost (primary model)
- LightGBM
- AdaBoost
- Linear Support Vector Machine

Evaluation metrics:
- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

Early stopping and threshold tuning were applied to improve generalization and recall of churn-prone customers.

---

## Customer Classification Logic
Based on predicted churn probability, customers are classified into:

- **Upsellable**: Low churn probability  
- **Monitoring**: Medium churn probability  
- **Retainable**: High churn probability  

This classification converts raw predictions into **business-usable insights**.

---

## Web Application
An interactive web interface was developed using Gradio to:
- Upload customer datasets
- Visualize customer category distribution
- Identify high-value upsell opportunities
- Recommend suitable plans based on usage patterns

The interface enables non-technical users to interact with the model easily.

---

## Project Structure
customer-upsell-retention-ml/
│
├── Customer_Upsell_Final.ipynb
├── customer_upsell_final.py
├── requirements.txt
├── README.md
└── screenshots/


---

## Technologies Used
- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost
- LightGBM
- Gradio
- Plotly

---

## Results and Impact
The model successfully identifies customer churn risk and translates predictions into actionable customer segments.  
This approach helps businesses:
- Reduce churn
- Improve customer satisfaction
- Target upsell opportunities efficiently

---

## Future Improvements
- Model explainability using SHAP values
- Deployment on cloud platforms or Hugging Face Spaces
- Integration with real-time CRM systems
- Automated model retraining pipelines

---

## Author
Subarna Sural  
B.Tech in Computer Science and Engineering (AI & ML)

