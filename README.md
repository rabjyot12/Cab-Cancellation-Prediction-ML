# 🚖 Cab Cancellation Prediction using Machine Learning

## 📌 Project Overview

Cab ride cancellations can lead to customer dissatisfaction, driver inefficiency, and revenue loss for ride-hailing companies. This project aims to predict whether a cab booking will be cancelled before the ride begins using Machine Learning.

A Random Forest Classifier was trained on historical booking data after performing data preprocessing, feature engineering, exploratory data analysis (EDA), and class imbalance handling using SMOTE. The trained model was then used to predict cancellations on unseen scoring data.

---

## 🎯 Problem Statement

Build a machine learning model that predicts whether a cab booking will be cancelled based on booking details, customer information, and ride characteristics.

Target Variable:

- **Car_Cancellation**
  - 0 → Ride Not Cancelled
  - 1 → Ride Cancelled

---


## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Imbalanced-learn (SMOTE)
- Joblib
- Jupyter Notebook

---

## 📊 Project Workflow

### 1. Data Preprocessing

- Removed unnecessary columns
- Handled missing values
- Converted datetime columns
- Removed invalid records
- Removed data leakage (`Cost_of_error`)

---

### 2. Feature Engineering

Created several new features including:

- Customer Booking Count
- Ride Hour
- Ride Day of Week
- Booking Hour
- Booking Day of Week
- Booking Advance Hours
- Booking Nature
- Same Day Booking Indicator
- Vehicle Model Indicator

---

### 3. Exploratory Data Analysis (EDA)

Performed analysis to understand:

- Class imbalance
- Booking behaviour
- Cancellation trends
- Customer booking patterns
- Ride timing
- Booking nature vs cancellation

---

### 4. Handling Class Imbalance

The dataset contained approximately:

- 93% Non-Cancelled Rides
- 7% Cancelled Rides

SMOTE (Synthetic Minority Oversampling Technique) was applied to balance the training dataset before model training.

---

### 5. Model Building

Algorithm Used:

- Random Forest Classifier

Evaluation Metrics:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC Score

---

## 📈 Model Performance

### Final Model (Random Forest + SMOTE)

| Metric | Score |
|---------|------:|
| Accuracy | 89% |
| ROC-AUC | 0.818 |
| Precision (Cancelled) | 0.33 |
| Recall (Cancelled) | 0.45 |
| F1-Score | 0.38 |

The model successfully improved cancellation detection after applying SMOTE while maintaining good overall performance.

---

## 💡 Key Business Insights

- Same-day bookings showed higher cancellation rates.
- Frequent customers were less likely to cancel rides.
- Booking time significantly influenced cancellation probability.
- Class imbalance handling improved the model's ability to detect cancelled rides.

---

## 🚀 Prediction on New Data

After training, the same preprocessing pipeline was applied to the scoring dataset.

The trained model generated:

- Predicted Cancellation (0 or 1)
- Cancellation Probability

Results were exported as:

```
cab_cancellation_predictions.csv
```

## 📁 Dataset

This project uses two datasets:

- **YourCabs_training.csv** – Used for data preprocessing, feature engineering, model training, and evaluation.
- **YourCabs_score.csv** – Used for generating predictions on unseen booking records.

---

## ▶️ How to Run

### Clone the repository

```bash
git clone https://github.com/rabjyot12/Cab-Cancellation-Prediction-ML.git
```

### Install dependencies

```bash
pip install -r requirements.txt
```

### Run the notebooks

1. Open **01_Model_Training.ipynb**
2. Train the model
3. Open **02_Scoring_Prediction.ipynb**
4. Generate predictions for the scoring dataset

---

## 📌 Future Improvements

- Hyperparameter tuning using GridSearchCV
- Compare additional machine learning models
- Deploy the model using Flask or FastAPI
- Build an interactive web interface
- Integrate with real-time booking systems

---

## 👨‍💻 Author

**Rabjyotsingh Taranjeetsingh Majethiya**

B.Tech Computer Science Engineering (AI & ML)

GitHub: https://github.com/rabjyot12
LinkedIn: https://linkedin.com/in/rabjyotsingh/

---

## 📄 License

This project is licensed under the MIT License.
