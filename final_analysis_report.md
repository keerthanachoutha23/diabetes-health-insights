**Diabetes Health Indicators Analysis Report**

### **1. Introduction**
The purpose of this analysis is to explore the relationships between various health indicators and diabetes status using data from the **Behavioral Risk Factor Surveillance System (BRFSS) 2015**. The dataset contains **229,781** cleaned records with **22 features**, including **demographic information, health conditions, and lifestyle factors**.

### **2. Data Cleaning & Preprocessing**
- **Duplicate Removal**: 23,899 duplicate records were removed, reducing the dataset to 229,781 unique records.
- **Missing Values**: No missing values were detected in any of the columns.
- **Data Types**: All columns were numerical, requiring no conversions.
- **Target Variable**: `Diabetes_012` (0 = No Diabetes, 1 = Prediabetes, 2 = Diabetes)

### **3. Exploratory Data Analysis (EDA)**

#### **3.1 Distribution of BMI**
- BMI values ranged from **12 to 98**, with an average of **28.69**.
- The **majority of respondents** had a BMI in the **overweight or obese category**, reinforcing the need to explore its relationship with diabetes.

#### **3.2 Correlation Analysis**
- **Strong Positive Correlation**: `HighBP`, `HighChol`, and `DiffWalk` showed a strong relationship with diabetes.
- **Moderate Correlation**: `BMI` and `GenHlth` (self-reported general health) also showed significant associations with diabetes.
- **Weak or No Correlation**: Factors such as `Income` and `Education` showed little direct correlation with diabetes status.

#### **3.3 Diabetes Prevalence by Age**
- Diabetes prevalence **increases significantly with age**.
- Individuals **above 60 years old** have the highest proportion of diabetes cases.
- Younger age groups have a higher prevalence of **prediabetes**, indicating early warning signs.

#### **3.4 Diabetes and Income Levels**
- Lower-income groups showed a **higher prevalence of diabetes**, possibly due to disparities in healthcare access, diet, and lifestyle choices.
- Higher-income groups had a lower incidence, likely reflecting better access to healthcare and healthier lifestyle options.

#### **3.5 Impact of Lifestyle Factors**
- **Physical Activity**: Individuals with regular physical activity had a lower prevalence of diabetes.
- **Smoking & Alcohol**: Heavy alcohol consumption was **not strongly correlated** with diabetes, while smoking showed **a weak correlation**.
- **Fruit & Vegetable Intake**: Regular consumption was linked to a lower diabetes risk, though the correlation was not very strong.

### **4. Machine Learning Analysis**

To improve diabetes prediction, two machine learning models were applied: **Random Forest** and **XGBoost**.

#### **4.1 Random Forest Model**
- **Accuracy**: **79%**
- **Key Findings**:
  - Strong performance for **No Diabetes (0.0)** with **0.89 precision and 0.87 recall**.
  - **Poor performance for Prediabetes (1.0)** (recall = 0.00, meaning it fails to identify prediabetes cases).
  - **Moderate performance for Diabetes (2.0)** with **0.40 precision and 0.49 recall**.

#### **4.2 XGBoost Model**
- **Accuracy**: **83%** (better than Random Forest)
- **Key Findings**:
  - **Better recall for Diabetes (2.0) (0.28 vs. 0.49 in RF)**.
  - **Still struggles with Prediabetes (1.0), recall = 0.00**.
  - **Higher weighted precision (0.81) and recall (0.83)**, making it the preferred model.

#### **4.3 Key Takeaways from Machine Learning**
- **Random Forest performed well overall but struggled with minority classes**.
- **XGBoost had better recall for diabetes but still struggled with prediabetes**.
- **Further improvements** could include **hyperparameter tuning, feature selection, or using deep learning techniques**.

### **5. Key Findings & Recommendations**
1. **Age and BMI** are key risk factors for diabetes; preventive healthcare should focus on **early screening and interventions for overweight individuals.**
2. **Physical inactivity and poor general health** are associated with higher diabetes prevalence, emphasizing the need for **public health campaigns on physical activity and nutrition**.
3. **Lower-income individuals are more likely to develop diabetes**, highlighting the importance of **accessible healthcare and dietary education** for these groups.
4. **Hypertension (HighBP) and HighCholesterol are major comorbidities**, reinforcing the need for **multi-faceted health interventions** targeting both diabetes and cardiovascular risk factors.
5. **Machine Learning can be used for early detection of diabetes risk**, with XGBoost showing better predictive power than Random Forest.

### **6. Conclusion**
This analysis provides insights into the prevalence and risk factors of diabetes in the BRFSS dataset. Future research could involve **predictive modeling** using machine learning to identify high-risk individuals more accurately. Additionally, policy recommendations should aim at addressing **health disparities and promoting early preventive care**.

