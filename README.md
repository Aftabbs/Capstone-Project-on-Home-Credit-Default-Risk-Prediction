# Capstone Project on Home Credit Default Risk Prediction.
This project was completed as a collaborative capstone project by a team of five students from Great Lakes Institute of Management. The project focuses on predicting the creditworthiness of loan applicants and their ability to repay loans. By leveraging a dataset provided by Home Credit, which includes telco data and transactional data, the team utilized exploratory data analysis, feature engineering, and machine learning techniques to build predictive models.
                                               ![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/595cb2c8-2db5-4fe4-99f6-1d2bf4b7d744)

# Problem Statement

The problem is that a large number of loan applicants are being rejected due to insufficient or non-existent credit histories. Home Credit wants to leverage data analysis and machine learning to assess the creditworthiness of applicants and predict their ability to repay loans accurately.

# Dataset Sampling

Due to the large size of the dataset (more than 300,000 rows and 122 columns), performing exploratory data analysis (EDA) and modeling on the entire dataset can be computationally expensive. Therefore, a random sample of 100,000 rows is generated, and statistical tests (One Sample Z-Test for numerical columns and Chi-Square Goodness of Fit test for categorical columns) are performed to ensure the similarity between the sample and the population. Resampling is conducted until a representative sample is obtained.
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/5fe3fb3c-3a3b-4423-90af-474306f30249)

# Data Preprocessing

**Null Value Analysis**

![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/c020958c-1608-4bdb-9a92-9fd99a169d08)

Many columns in the dataset contain a significant number of null values. Nulls are replaced with appropriate values based on different approaches such as median imputation, mode imputation, and KNN imputation. Additionally, a new null column is created to indicate whether a value is null or not, for columns with null proportions greater than 10%. Rows with less than 10% null values are dropped.

**Outlier Analysis and Treatment**

![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/cd84d601-b691-440f-ab34-7da9c53ab951)

Outliers are identified and removed using the 3 times IQR (interquartile range) as the limit. However, given that this is a finance dataset, it is decided to retain outliers and utilize models that are not sensitive to outliers.

**Univariate,Bivariate,Multivariate Analysis**

![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/d723a1dc-2956-4c8e-ba7f-84a9e8783dd3)
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/af770975-813d-41e0-8cf0-2630e9204e26)
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/1cefb5b0-5935-4970-a23b-bef052955abd)


# Feature Selection and Model Building
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/b2cda003-6d28-4afb-93aa-fc6f9a38c2bf)

Random Forest is used as the base model due to its ability to provide feature importance. The important features are identified using the base model. Notable findings include:

**Feature Importance**
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/de215a87-babb-4cfb-b252-4b1c6341ef63)

At least 50% of defaulters are correctly identified, but precision for defaulters is low.
The top three important features are EXT_SOURCE_2, EXT_SOURCE_3, and DAYS_BIRTH.
Different classification algorithms are experimented with, and model evaluation is performed using confusion matrix and ROC AUC score. Fine-tuning techniques are applied to improve model performance.

# Model Evaluation and Selection

Based on different evaluation metrics, including recall and ROC AUC score, the following conclusions are drawn:
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/71b39455-414d-4972-876a-1743b172ff97)
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/c9fd5a5b-aab5-4ba6-9e96-d104c4eb4d00)
![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/1671a205-486d-4045-b434-7ce0248bbce5)

Fine-Tuned XG Boost achieves the highest recall score of 0.72 for defaulters.
Fine-Tuned Gradient Boost achieves the highest ROC AUC score of 0.7523 overall.


# Conclusion
This capstone project on Home Credit Default Risk Prediction was conducted by a team of students from Great Lakes Institute of Management. By applying exploratory data analysis, feature engineering, and machine learning techniques, the team successfully developed predictive models to assess the creditworthiness of loan applicants. The project aims to facilitate better decision-making in the lending industry and mitigate credit risks.

# Industrial Use Case
The insights gained from this project can be applied in the lending industry to assess loan applicants' creditworthiness and predict their repayment abilities. By leveraging machine learning techniques, financial institutions can make more informed decisions and minimize the risk of default.


![image](https://github.com/Aftabbs/Home-Credit-Default-Risk-Prediction/assets/112916888/aed24ec1-acc2-4a92-8349-98ebf6f4c660)

Feel free to add additional sections or modify the structure of the Readme.md file to fit your project and provide more details as needed.













