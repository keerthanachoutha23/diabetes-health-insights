# **Diabetes Health Insights**

## **Project Overview**
This project explores diabetes prevalence using the **BRFSS 2015 dataset**, analyzing key health indicators and their influence on diabetes risk. The goal is to uncover trends in health behaviors, socioeconomic factors, and medical history that contribute to diabetes outcomes. Additionally, machine learning models were developed to improve diabetes prediction.

## **Files Included**
- **`diabetes_analysis.ipynb`** – Jupyter Notebook containing data cleaning, exploratory analysis, and machine learning models.
- **`final_analysis_report.md`** – Summary report of key findings, insights, and recommendations.
- **`diabetes_012_health_indicators_BRFSS2015.csv`** – The cleaned dataset used in this study.

## **Key Insights**
- **Diabetes prevalence increases with age**, with individuals over 60 having the highest risk.
- **Higher BMI and high blood pressure (Hypertension)** are strongly correlated with diabetes.
- **Lower-income groups are at a higher risk of developing diabetes**, likely due to disparities in healthcare access and lifestyle factors.
- **Regular physical activity and a balanced diet** show positive associations with lower diabetes prevalence.

## **Machine Learning Analysis**
To enhance diabetes risk prediction, two models were implemented:

### **Random Forest Classifier**
- **Accuracy**: **79%**
- **Strengths**: High precision for identifying non-diabetic individuals.
- **Weaknesses**: Poor recall for prediabetes cases, meaning it struggles to detect individuals at early risk.

### **XGBoost Classifier**
- **Accuracy**: **83%** (outperformed Random Forest)
- **Strengths**: Improved recall for diabetes cases and higher overall prediction performance.
- **Weaknesses**: Prediabetes cases still remain underrepresented in predictions.

### **Future Improvements**
- Additional feature engineering to improve predictive power.
- Hyperparameter tuning for better recall on prediabetes cases.
- Exploring deep learning approaches for enhanced classification accuracy.

## **Conclusion**
This analysis provides valuable insights into the factors influencing diabetes risk and demonstrates the potential of machine learning in early detection. The findings highlight the importance of **preventive healthcare, lifestyle interventions, and targeted public health policies** to reduce diabetes prevalence.

📊 **Next Steps**: Implement further model refinements and expand the dataset to include more recent trends in diabetes risk factors.

