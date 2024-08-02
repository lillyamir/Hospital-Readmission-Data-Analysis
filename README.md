# Hospital Readmission Data Analysis
## Predicting Patient Readmission in Hospitals

### Introduction

The goal of this project is to predict whether a patient will be readmitted to the hospital within 30 days of discharge. Understanding the factors that contribute to hospital readmission can help healthcare providers improve patient care and reduce costs. I utilized a publicly available dataset with various patient attributes and hospital records to build a predictive model for readmission.

### Data Collection and Preprocessing

I started with a dataset containing 25,000 entries and 18 columns, including patient demographics, medical specialty, diagnosis codes, and other hospital-related variables. The target variable was `readmitted`, which indicates whether a patient was readmitted within 30 days (1 for yes, 0 for no).

**Key Steps:**
- **Data Cleaning:** Handled missing values and converted categorical variables to dummy variables.
- **Feature Engineering:** Created meaningful features such as the midpoint of age ranges.
- **Standardization:** Standardized numerical features for better model performance.

### Feature Selection

To identify the most relevant features, I employed Recursive Feature Elimination (RFE) with a logistic regression model. This process helped us narrow down the predictor variables to the top 10 most significant ones.

### Model Training

I trained a logistic regression model using the selected features. The data was split into training and testing sets, with 70% used for training and 30% for testing. The logistic regression model was then fitted to the training data.

### Model Evaluation

The model's performance was evaluated using several metrics, including accuracy, precision, recall, F1 score, and ROC-AUC score. Here are the results:

#### Classification Report

```
               precision    recall  f1-score   support

           0       0.60      0.79      0.68      3974
           1       0.63      0.41      0.50      3526

    accuracy                           0.61      7500
   macro avg       0.62      0.60      0.59      7500
Iighted avg       0.61      0.61      0.59      7500
```

#### Confusion Matrix

```
[[3125  849]
 [2081 1445]]
```

#### Performance Metrics

- **Accuracy:** 0.61
- **Precision:** 0.63
- **Recall:** 0.41
- **F1 Score:** 0.50
- **ROC-AUC Score:** 0.64

### Visualizations

#### ROC Curve

The ROC curve shows the trade-off betIen the true positive rate and false positive rate. Our model achieved an ROC-AUC score of 0.64, indicating moderate performance.

#### Feature Importance

The bar plot of feature importance highlights the top predictors for readmission, which include variables like the number of medications, time in hospital, and number of procedures.

### Conclusion

The logistic regression model achieved an accuracy of 0.61 in predicting patient readmission. The most significant predictors included the number of medications, time in the hospital, and number of procedures. While the model shows moderate performance, there is room for improvement.

### Implications

Identifying the key factors associated with hospital readmission can help healthcare providers implement targeted interventions to reduce readmission rates. For instance, patients with a high number of medications or extended hospital stays might benefit from more rigorous follow-up care post-discharge.

### Future Work

To enhance the model's performance, future work could include:
- **Incorporating Additional Data:** Integrating more comprehensive datasets, including socioeconomic factors and more detailed medical histories.
- **Exploring Advanced Models:** Testing other machine learning models such as Random Forest, Gradient Boosting, or Neural Networks.
- **Feature Engineering:** Creating more sophisticated features and interactions betIen variables.

### Documentation and Reporting

The project is documented in a GitHub repository, including the code, datasets, and visualizations. The repository is structured as follows:
- `data/`: Raw and processed data files.
- `notebooks/`: Jupyter notebooks for exploration and modeling.
- `src/`: Python scripts for data processing, modeling, and evaluation.
- `reports/`: Generated plots, figures, and the final report.
- `README.md`: Project overview and setup instructions.

The GitHub repository link: [Hospital-Readmission-Data-Analysis](https://github.com/lillyamir/Hospital-Readmission-Data-Analysis)

This project demonstrates the ability to handle complex data analysis tasks, perform feature selection, train predictive models, and present the results effectively.
