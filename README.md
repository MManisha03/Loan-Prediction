# 🛡️ Online Fraud Detection using Machine Learning
# 📌 Overview

This project focuses on detecting fraudulent online transactions using Machine Learning algorithms. With the increasing reliance on digital payments, fraud detection has become crucial to safeguard users and businesses. Our work leverages decision tree models trained on large-scale transactional datasets to classify transactions as fraudulent (1) or non-fraudulent (0) with very high accuracy.

Algorithm Used: Decision Tree Classifier

Dataset: Synthetic dataset (PaySim) generated from real mobile money transactions

Accuracy Achieved: ~99.97%

Tools: Python, Google Colab, Kaggle datasets

# 📂 Dataset

We used the PaySim dataset (synthetic dataset generated from mobile financial services logs).

Dataset Features:

step: Time unit (1 step = 1 hour)

type: Type of transaction (CASH_OUT, PAYMENT, CASH_IN, TRANSFER, DEBIT)

amount: Transaction amount

oldbalanceOrg: Balance before transaction (origin account)

newbalanceOrg: Balance after transaction (origin account)

oldbalanceDest: Balance before transaction (destination account)

newbalanceDest: Balance after transaction (destination account)

isFraud: Fraud label (0 = Non-Fraud, 1 = Fraud)

Dataset Source: Kaggle

# ⚙️ Methodology

Data Preprocessing

Converted categorical features (transaction type) into numerical values

Removed irrelevant/unnecessary columns

Balanced data to handle class imbalance

Exploratory Data Analysis (EDA)

Donut pie chart to analyze transaction distribution

Identification of high-risk transaction types

Model Development

Used Decision Tree Classifier

Trained on features: type, amount, oldbalanceOrg, newbalanceOrg

Tested using a split of 90% training / 10% testing

Performance

Achieved ~99.97% accuracy

Model successfully predicts fraud in unseen transactions

# 📊 Results
Model	Accuracy
Decision Tree Classifier	99.97%

Example Prediction:

# Features = [type, amount, oldbalanceOrg, newbalanceOrg]
features = np.array([[4, 9000.60, 9000.60, 0.0]])

print(model.predict(features))

# Output: ['Fraud']

🚀 How to Run
🔹 Clone Repository
git clone https://github.com/your-username/online-fraud-detection.git
cd online-fraud-detection

🔹 Install Dependencies
pip install -r requirements.txt

🔹 Run Jupyter Notebook / Colab

You can explore the project in Google Colab:
👉 Colab Notebook Link

🔹 Run Training Script
python train_model.py

📖 References

Jainil Shah – Fraud Detection using Decision Tree (Kaggle Notebook)

Ravelin Insights on Fraud Detection:

Online Payment Fraud

Machine Learning for Fraud Detection

✅ Conclusion

Machine Learning models, especially Decision Trees, are highly effective in detecting fraud transactions.

With synthetic datasets (PaySim), we can simulate real-world fraud scenarios while protecting privacy.

This system complements human fraud analysts by automating real-time detection and reducing false positives.
