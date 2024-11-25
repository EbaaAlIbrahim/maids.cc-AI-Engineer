# maids.cc-AI-Engineer
refarding the AI engineer position
Detailed Project Breakdown
Data Inspection
To start, we explored the training dataset by:

Displaying the first few rows using head() to understand its structure and contents.
Checking for any missing values with isnull().sum(). In this case, there were no missing values, so we proceeded confidently.
Data Standardization
Since numerical features often have different scales (e.g., battery power vs. clock speed), we used StandardScaler to standardize these features. This step ensures that all features contribute equally to the model's performance.

Exploratory Data Analysis (EDA)
To better understand the dataset:

Distribution of Price Range: A bar chart visualized the number of devices in each price range, giving us insights into how the data is distributed.
Correlation Heatmap: A heatmap showed the relationships between features, highlighting any strong correlations that could be leveraged for predictions.
Data Splitting
The dataset was divided into:

Features (X): The independent variables (device specifications).
Target (y): The dependent variable (price_range).
We further split the data into training and validation subsets. This split allows us to train the models on one portion of the data and validate their performance on unseen data.

Random Forest Classifier
We trained a Random Forest Classifier to classify devices into one of the four price ranges. The process involved:

Teaching the model to recognize patterns in the training data.
Testing the model on validation data to evaluate its performance.
Using the following metrics to assess the results:
Confusion Matrix: Highlights the model's correct and incorrect predictions for each class.
Classification Report: Provides detailed metrics such as precision, recall, F1-score, and support for each price range.
Accuracy Score: Shows the overall percentage of correct predictions.
XGBoost Classifier
We also trained an XGBoost Classifier, which is often more efficient and powerful. To optimize its performance, we fine-tuned it with hyperparameters such as eval_metric='mlogloss' (a multi-class log-loss function). Similar to the Random Forest model, predictions were made on the validation set and evaluated with the same metrics.

