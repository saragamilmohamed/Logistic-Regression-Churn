Project Overview
Customer churn prediction is a common problem faced by businesses. This project focuses on using a logistic regression model to predict whether a customer will churn based on various features like age, gender, balance, and more.

Dataset
The dataset used in this project is the "Churn_Modelling" dataset. It contains the following key features:

RowNumber: Unique row identifier.
CustomerId: Unique customer identifier.
Surname: Customer's last name.
CreditScore: Credit score of the customer.
Geography: Country of the customer.
Gender: Gender of the customer.
Age: Age of the customer.
Tenure: Number of years the customer has been with the bank.
Balance: Bank balance of the customer.
NumOfProducts: Number of bank products the customer uses.
HasCrCard: Whether the customer has a credit card.
IsActiveMember: Whether the customer is an active member.
EstimatedSalary: Estimated salary of the customer.
Exited: Whether the customer has churned (1 if yes, 0 if no).
Data Preprocessing
Data preprocessing steps include:

Dropping Unnecessary Columns: Columns like RowNumber, CustomerId, and Surname are dropped as they do not contribute to the prediction.
Label Encoding: The Gender column is label-encoded to convert it into numerical format.
One-Hot Encoding: The Geography column is one-hot encoded to create separate columns for each country.
Handling Missing Values: The balance is adjusted for customers with a balance of 0 by replacing it with the mean balance.
Exploratory Data Analysis (EDA)
EDA is performed to understand the distribution of features and relationships between them. Visualizations include:

Age Distribution: A histogram showing the distribution of customer ages.
Balance Distribution by Gender: A boxplot to compare balance distributions across genders.
Gender Distribution by Exited Status: A count plot to show the distribution of churn across genders.
Correlation Heatmap: A heatmap to show the correlation between different features.
Feature Engineering
Feature Selection: The SelectKBest method is used to select the top 3 features that are most significant for predicting churn.
Selected Features: Based on the selection process, the features Age, IsActiveMember, and GeographyGermany are chosen.
Modeling
A logistic regression model is trained using the selected features. The dataset is split into training and testing sets to evaluate model performance. Key steps include:

Splitting the Dataset: The dataset is split into training and testing sets using an 80-20 split.
Feature Scaling: Features are scaled using StandardScaler to standardize the range of independent variables.
Model Training: The logistic regression model is trained on the training data.
K-Fold Cross-Validation: Cross-validation is performed to assess the generalizability of the model. The mean accuracy across folds was 78.98%.
Model Evaluation
The model is evaluated using the following metrics:

Accuracy: The model achieved an accuracy of 82.15% on the test set.
Confusion Matrix: A confusion matrix is plotted to visualize the performance of the model.
Precision: The precision score is 0.63, indicating the percentage of correct positive predictions out of all positive predictions.
Recall: The recall score is 0.18, indicating the percentage of actual positives that were correctly identified by the model.
Cross-Validation Results
The model was also evaluated using 12-fold cross-validation, yielding the following accuracy scores across folds:

Cross-Validation Accuracy Scores: [0.80, 0.80, 0.79, 0.81, 0.77, 0.77, 0.78, 0.82, 0.79, 0.74, 0.79, 0.81]
Mean Accuracy: 78.98%
Conclusion
The logistic regression model provides a good starting point for predicting customer churn with an accuracy of 82.15%. However, the relatively low recall score suggests that the model could be improved, possibly by using more complex algorithms or by further refining the features used in the model.
