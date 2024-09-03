# Credit Card Fraud Detection
This project aims to detect fraudulent credit card transactions using machine learning models, specifically Random Forest and XGBoost classifiers. The project includes data preprocessing, feature engineering, model training, and evaluation using performance metrics like accuracy, precision, recall, and F1-score.

## Dataset
The dataset used in this project is sourced from Kaggle, specifically the "Fraud Detection" dataset available at this link. It contains transactions made by credit cards in September 2013 by European cardholders.


## Data Preprocessing
### 1. Gender Encoding
The gender feature is encoded into numeric values, where M is mapped to 1 and F to 0.

### 2. Age Calculation
The Age feature is derived from the difference between the transaction date and the date of birth (dob).

### 3. Location Matching
A new feature location_matches is created based on the proximity of the transaction location (lat, long) and the merchant's location (merch_lat, merch_long).

### 4. Datetime Features
The trans_date_trans_time feature is split into individual components like year, month, day, hour, minute, and second.

### 5. One-Hot Encoding
Categorical variables such as category are transformed into binary features using one-hot encoding.

### 6. Feature Dropping
Irrelevant features such as cc_num, city, street, etc., are dropped from the dataset to focus on the most significant features.

## Feature Engineering
Additional features were engineered to enhance model performance, including:

location_matches: A boolean feature indicating if the transaction location closely matches the merchant's location.
Datetime components: Extracted from the transaction timestamp for more granular analysis.

## Modeling

### 1. Handling Class Imbalance
The dataset was highly imbalanced, with far more non-fraudulent transactions than fraudulent ones. To address this, Synthetic Minority Over-sampling Technique (SMOTE) was used to balance the classes.

### 2. Random Forest Classifier
A Random Forest model was trained on the processed data. The model's hyperparameters were tuned to optimize performance.

### 3. XGBoost Classifier
An XGBoost model was also trained on the same data for comparison. The model's performance was evaluated and compared to the Random Forest model.

## Evaluation
Both models were evaluated using the following metrics:

- #### Accuracy: The overall correctness of the model.
- #### Confusion Matrix: The breakdown of true positives, false positives, true negatives, and false negatives.
- #### Precision: The accuracy of positive predictions.
- #### Recall: The ability of the model to capture all positive instances.
- #### F1-score: The harmonic mean of precision and recall, providing a balance between the two.

## Contributions
This project was done in during the my time as Data Science Intern at JP Morgan Chase & Co., in collaboration with my other teammates - Daria, Eric, and Vanessa. We worked together on the visuals, however, the models were built individually by me. 

