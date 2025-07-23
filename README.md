# Customer-Satisfaction-Prediction
Title: Customer Satisfaction Prediction using Random Forest Classifier
Submitted by: Sara
1. Introduction
In customer-centric industries, predicting customer satisfaction plays a vital role in improving service quality and retention. This project uses machine learning techniques to analyze customer support ticket data and predict satisfaction ratings.
2. Objective

Analyze the dataset and understand customer satisfaction trends.

Build a predictive model using customer ticket features.

Identify key drivers of satisfaction to guide business strategies.
3. Tools & Technologies Used

Language: Python

Libraries: pandas, seaborn, matplotlib, scikit-learn

Model: Random Forest Classifier

IDE: Google Colab
4. Dataset Description
The dataset consists of customer support tickets with attributes such as:

Customer Age, Gender

Product Purchased

Ticket Type, Priority, Channel

Customer Satisfaction Rating (Target: Rating 1 to 5)
Over 200,000 rows were processed using chunked loading to manage large data efficiently.
5. Exploratory Data Analysis (EDA)
5.1. Rating Distribution

 A bar plot of satisfaction ratings showed balanced but widely spread classes.
5.2. Correlation

 Heatmap revealed a weak correlation between age and satisfaction, indicating categorical variables may play a more critical role.
6. Model Development
6.1. Preprocessing

 Numerical Feature: Passed through unchanged (Customer Age).

 Categorical Features: One-hot encoded using ColumnTransformer.
6.2. Model Pipeline

 Random Forest Classifier was implemented inside a Pipeline with preprocessing steps.
6.3. Train-Test Split

 70% training and 30% testing split. Model trained and evaluated accordingly.
7. Results & Evaluation
✅ Accuracy:
20.0%
Confusion Matrix & Classification Report:

 Very low prediction accuracy across all 5 satisfaction classes.

 Precision, recall, and F1-score hovered around 0.20 for all classes.
Interpretation:
The model struggled to make accurate predictions, likely due to:

 High class overlap

 Non-linear or hidden patterns not captured by features

 Potential label noise in satisfaction ratings
8. Feature Importance
A bar chart of the Top 10 Most Important Features revealed:

 Ticket Priority and Type were more influential than demographic info.

 Product Purchased also contributed significantly to satisfaction prediction.
9. Conclusion
The Random Forest model did not perform well on this dataset, highlighting challenges in predicting customer satisfaction from limited or noisy features. However, feature importance analysis provided insights into what aspects affect satisfaction most.
10. Future Work

 Try boosting models (e.g., XGBoost, LightGBM)

 Balance the dataset using techniques like SMOTE

 Add NLP features from ticket texts or customer comments

 Fine-tune hyperparameters and improve feature engineering
