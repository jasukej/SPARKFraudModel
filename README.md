## SPArk Fraud Detection Model
#### Team Unbeatabolt ⚡️

### Problem Statement
The institution wishes to find a solution to reduce fraudulent transactions while cutting down on false positives. Our team has developed the SPArk business plan, which comprises of Scheme tokenization, Predictive modelling, and AI fraud flagging. 
**This repository addresses this second component, containing notebooks for data analysis and the predictive model:**
* Descriptive Analysis (EDA): Informs the implementation of the business plan detailed in our slide deck, as well as feature and model selection.
* train_test: Notebook details model training, testing, feature selection, and hyperparameter tuning. A corresponding performance report is also attached.

### Project Structure
The repository is organized as follows:

SPARKFraudModel/
├── data/                   # Datasets (raw and clean) used for training and eval
├── eda/                    # Jupyter notebooks for exploratory data analysis
├── models/                 # Saved models
├── slide-deck/             # Visualizations and pitch deck
├── README.md               # Project README

Made as part of BOLT UBC's 2024 Case Competition. Load using Jupyter Notebook or Google Colab.

### Data Description
The dataset used for this project contains anonymized financial transaction data, including features such as transaction amount, time, and various user-specific attributes. Due to privacy concerns, sensitive information has been excluded or anonymized.

Transaction ID: Unique identifier for each transaction.
Amount: The monetary value of the transaction.
Timestamp: The time when the transaction was made.
Features: Various attributes that describe the transaction and the user.
The data is stored in the data/ directory and is processed in batches using Spark DataFrames.

### Feature Engineering
Feature engineering is a critical part of this project. Some of the key features created include:

* Transaction Frequency: Number of transactions made by a user within a specific timeframe.
* Monetary Ratio: Ratio of the current transaction amount to the user's average transaction amount.
* Time-based Features: Extracted hour, day of the week, and other temporal features to capture behavioral patterns.

### Modeling
The model pipeline consists of the following steps:

1. Data Preprocessing: Handling missing values, normalization, and splitting data into training and testing sets.
2. Feature Selection: Using techniques like PCA to select the most relevant features. Insights taken from the EDA–such as which features were most correlated–was also implemented.
3. Model Training: Several models were trained, including Random Forest, Gradient Boosting, and a custom ensemble model.
4. Hyperparameter Tuning: Grid search and cross-validation were used to optimize the models.

### Evaluation
The models were evaluated using various metrics, including:

* Accuracy: The proportion of correctly identified transactions.
* Precision: The key metric in reducing false alarms. The ratio of true positives to the sum of true and false positives.
* Recall: The ratio of true positives to the sum of true positives and false negatives.
* F1 Score: The harmonic mean of precision and recall, used to balance the two metrics.

### Results
The final model achieved an F1 score of 0.92 on the test dataset, indicating high accuracy in detecting fraudulent transactions, and a high precision expected to minimize false alarms. The model's performance is visualized in the results/ directory, where confusion matrices and other evaluation plots are found.

