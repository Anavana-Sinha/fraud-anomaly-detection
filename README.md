# fraud-anomaly-detection Using Machine Learning

Introduction:
This project develops and compares two machine learning approaches for detecting suspicious transactions:
Random Forest — supervised classification
Isolation Forest — unsupervised anomaly detection
The objective is to evaluate how well these two approaches identify fraudulent transactions using precision, recall, F1-score, and PR-AUC.

Dataset:
The project uses the Credit Card Fraud Detection dataset.This dataset contains Time,v1 to v28 transaction features,Amount which is transaction amount and Class which is used as target variable. The dataset contains a highly imbalanced class distribution, with fraudulent transactions representing a very small percentage of the total transactions.

Problem Statement: How effectively can supervised and unsupervised machine learning methods detect fraudulent credit card transactions under extreme class imbalance?

Models Used:
1.Random Forest: Random Forest is a supervised ensemble learning algorithm that combines multiple decision trees.In this project, Random Forest was trained using the known transaction labels.

2.Isolation Forest: Isolation Forest is an unsupervised anomaly detection algorithm.Instead of learning directly from fraud labels, it attempts to identify transactions that are unusual compared with the rest of the dataset.
The model was used to investigate whether an anomaly-detection approach could identify fraudulent transactions without relying on supervised classification.

Data Preprocessing:
The Class column was separated as the target variable And the remaining columns were used as input features.
The dataset was divided into:
      a. 80% training data
      b. 20% testing data
Stratified splitting was used so that the class distribution was maintained between the training and testing sets.

Evaluation Metrics:
1.Precision: Precision measures how many transactions predicted as fraudulent were actually fraudulent.
2.Recall: Recall measures how many of the actual fraudulent transactions were detected.
3.F1 Score: F1-score provides a balance between precision and recall.
4.PR-AUC: Precision-Recall Area Under the Curve is particularly useful for highly imbalanced classification problems because it focuses on the performance of the minority class.

Result Analysis:
Random Forest achieved substantially better overall performance. 
As It achieved:
    a. 96.05% precision
    b. 74.49% recall
    c. 83.91% F1-score
    d. 0.8542 PR-AUC
Isolation Forest achieved higher recall at 84.69%, meaning it detected a larger proportion of fraudulent transactions.
However, its precision was only 4.22%, indicating that a large number of transactions identified as anomalies were actually legitimate.
The PR-AUC of Random Forest (0.8542) was also considerably higher than the PR-AUC of Isolation Forest (0.2180).

Therefore, among the two approaches evaluated in this project, Random Forest provided the better overall fraud detection performance.

Conclusion:
This project compared supervised and unsupervised machine learning approaches for credit card fraud detection under severe class imbalance.The results show that Random Forest performed significantly better overall than Isolation Forest. Although Isolation Forest achieved higher recall, its very low precision resulted in many false-positive predictions.
Random Forest provided a better balance between detecting fraudulent transactions and avoiding unnecessary fraud alerts.

Therefore, for this dataset, Random Forest was the more effective approach for fraud detection.
