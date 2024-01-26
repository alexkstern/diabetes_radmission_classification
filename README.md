# Diabetes Readmission Classification Project

## Overview

This repository contains a comprehensive analysis of various machine learning models, feature engineering methods, and sampling techniques for predicting patient readmissions in the context of diabetes. The primary objective of this project is to explore and identify the most effective strategies for classifying patient readmissions.

### Data Availability

Due to confidentiality and privacy concerns, the complete datasets used in this project are not publicly available. The analysis and conclusions presented are based on the data provided, but full datasets cannot be shared.

### Codebase

All code associated with this project is available in the Python notebook within this repository. The notebook includes detailed steps covering:

- Data Cleaning
- Data Preprocessing
- Training of Machine Learning Models

### Key Findings

- **XGBoost Performance:** XGBoost was the most effective model overall. It showed balanced performance across accuracy, F1 score, precision, and recall metrics, particularly with the dataset where not all data was dummified.
- **Random Forest:** This model demonstrated promising results in scenarios with high dimensionality data, highlighting its suitability for complex datasets.
- **Effect of SMOTE:** The application of SMOTE slightly reduced the performance of both XGBoost and Random Forest models.
- **MLP Classifier:** The MLP classifier excelled in F1 and recall with SMOTE but showed limitations in overall accuracy, especially with the all-data dummified dataset. This indicates its proficiency in balancing false positives and negatives but questions its reliability for this specific application.
- **Feature Engineering:** Manual feature engineering marginally improved the accuracy for Random Forest and XGBoost but significantly enhanced the MLP classifier's performance.
- **BERT Model:** Despite lower overall accuracy, the BERT model showed unique strength in distinguishing between no readmission and readmission cases. It did not require differentiating based on the 30-day timeframe, which is significant in clinical settings.

### Future Research Directions

- **Fine-Tuning BERT Model:** A promising future research line involves fine-tuning the BERT model specifically for the binary classification of hospital readmission. This could include experiments without LoRA to determine if improved performance is achieved by retraining all weights directly.
- **Semantic Understanding in Healthcare:** Exploring the impact of semantic understanding captured by models like BERT compared to classical machine learning techniques in healthcare settings.

### Conclusion

The analysis provides valuable insights into the effectiveness of different machine learning approaches for the classification of diabetes patient readmissions. It highlights the strengths and limitations of various models and techniques, offering a foundation for further research and application in the healthcare industry.

---

For more details, please refer to the Python notebook included in this repository.
