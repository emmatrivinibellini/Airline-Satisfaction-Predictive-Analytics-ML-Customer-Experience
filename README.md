# Airline Passenger Satisfaction Prediction  
### Machine Learning & Customer Experience Optimization

---

## Executive Summary

### Business Problem  
Airlines struggle to understand which service factors most strongly drive passenger satisfaction, leading to inefficient resource allocation and suboptimal customer experience strategies.
 
### Solution
This project builds an end-to-end machine learning pipeline to predict passenger satisfaction from over **100,000 records.**  
Using **Python**, I combined data cleaning, exploratory data analysis (EDA), feature selection, and multiple classification models (Random Forest, KNN, AdaBoost) to identify the most impactful drivers of customer satisfaction.

### Key Impact  
- **Best model:** Random Forest (All Features)  
- **Final test accuracy:** 89.79%  
- **Top satisfaction drivers:** online boarding, inflight entertainment, seat comfort  
- Demonstrated that overly aggressive feature selection reduces predictive performance by up to **7%**

### Next Steps  
- Deploy model insights into airline decision systems  
- Run A/B tests on key service improvements  
- Use predictive scoring to target low-satisfaction passengers in real time  

---

## Business Problem

Airlines collect large volumes of passenger feedback but often lack clarity on which operational factors actually drive satisfaction.

### Key Questions:
- What service elements most influence passenger satisfaction?
- Can we accurately predict whether a passenger will be satisfied before or after a flight?
- How can airlines use this insight to improve customer experience and operational efficiency?

The goal is to transform raw survey data into actionable business intelligence that supports better decision-making in service design and resource allocation.

---

## Methodology

This project follows a full data science lifecycle:

### 1. Data Cleaning & Preprocessing
- Handling missing values  
- Encoding categorical variables  
- Outlier detection and treatment  

### 2. Exploratory Data Analysis (EDA)
- Distribution analysis of satisfaction drivers  
- Correlation analysis between service features and target variable  

### 3. Feature Selection
- Chi-square test  
- Mutual Information  
- T-test analysis  

### 4. Model Development
- Random Forest  
- K-Nearest Neighbors (KNN)  
- AdaBoost  

### 5. Model Evaluation
- Cross-validation accuracy  
- Test set performance  
- Hyperparameter tuning (Grid Search)  

### 6. Comparative Analysis
- Full-feature model vs. reduced feature set  
- Bias-variance tradeoff evaluation  

---

## Skills & Tools

- **Python**: Data analysis and machine learning pipeline  
- **Pandas & NumPy**: Data manipulation and preprocessing  
- **Matplotlib & Seaborn**: Data visualization  
- **Scikit-learn**: ML models, feature selection, evaluation, hyperparameter tuning  
- **Jupyter Notebook**: Development environment  

---

## Results & Business Recommendations

### Model Performance

#### Approach 1 — All Features
- Random Forest: **96.8% CV → 89.79% test accuracy**
- KNN: **93.4% CV → 89.16% test accuracy**
- AdaBoost: **92.7% CV**

#### Approach 2 — Feature Selection (T-test subset)
- Random Forest: **89.65% CV → 82.61% test accuracy**
- AdaBoost: **87.76% CV → 82.28% test accuracy**
- KNN: **87.34% CV**

---

### Key Insights

- **Online boarding**, **inflight entertainment**, and **seat comfort** are the **3 strongest predictors of satisfaction** across all methods.  
- Business class passengers and frequent flyers report significantly higher satisfaction levels.  
- Gender, gate location, and customer type have minimal predictive power.  
- Reducing features too aggressively leads to measurable performance loss, indicating important hidden interactions between variables.  

---

### Business Recommendations

- Prioritize improvements in **boarding experience**, **entertainment systems**, and **seat comfort**  
- Avoid oversimplifying customer models by removing correlated service features
- Use full-feature predictive models for operational decision-making rather than heavily reduced feature sets  

---

## Next Steps

- Deploy the model to support real-time passenger satisfaction prediction  
- Run A/B tests on inflight entertainment and boarding experience improvements  
- Integrate model outputs into CRM systems to proactively identify at-risk passengers  

---

## Datasets  
Both datasets (train and test) are available here:  
[Airline Passenger Satisfaction Datasets (train.csv & test.csv)](https://drive.google.com/drive/folders/18MMXkE98uHDuWHDgXPpwD08Y7vyEnElk)  

The datasets include over **100,000 passenger records**, containing information such as:  
- Gender, Age, Customer Type, Type of Travel, Class  
- Flight Distance, Delay times  
- Ratings for onboard services, comfort, entertainment, food, etc.  
- Target variable: **Satisfaction** (Satisfied / Neutral or Dissatisfied)

---

## Files in this Repository  
| File | Description |
|------|--------------|
| `airline_satisfaction_prediction.ipynb` | Python notebook containing full workflow: EDA, feature selection, and ML models. |
| `airline_satisfaction_presentation.pdf` | Project presentation and key takeaways. |
| `README.md` | Project overview, datasets, insights, and methodology. |
