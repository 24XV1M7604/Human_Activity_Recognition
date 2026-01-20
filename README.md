# Human Activity Recognition using Machine Learning

## Project Overview

Human Activity Recognition (HAR) is a machine learning project that aims to identify the physical activity a person is performing (such as walking, sitting, or standing) using data collected from smartphone sensors.

In this project, we build a **supervised machine learning classification system** that learns patterns from smartphone sensor data and predicts the corresponding human activity.

This project follows a **complete end-to-end machine learning workflow**, making it suitable for academic submissions, GitHub portfolios, and resume inclusion.

---

##  Problem Statement

Smartphones are equipped with sensors such as accelerometers and gyroscopes that continuously record motion data. However, raw sensor data alone does not provide meaningful insights.

The goal of this project is to:

* Analyze smartphone sensor readings
* Learn patterns associated with different human activities
* Accurately classify activities using machine learning models

---

##  Type of Machine Learning Problem

* **Category**: Supervised Learning
* **Task**: Multi-class Classification
* **Input**: Sensor-based numerical features
* **Output**: Human activity label

---

##  Dataset Description

The dataset consists of pre-processed smartphone sensor data collected from multiple subjects performing daily activities.

### Files Used

* `train.csv` – Training dataset
* `test.csv` – Testing dataset

### Dataset Characteristics

* Each row represents a fixed window of sensor readings
* Columns contain processed accelerometer and gyroscope features
* The `Activity` column is the target label

### Activities Classified

* WALKING
* WALKING_UPSTAIRS
* WALKING_DOWNSTAIRS
* SITTING
* STANDING
* LAYING

---

##  Project Workflow

```
Raw Sensor Data
      ↓
Data Loading
      ↓
Feature & Label Separation
      ↓
Label Encoding
      ↓
Feature Scaling
      ↓
Model Training
      ↓
Model Evaluation
      ↓
Model Saving
```

---

##  Technologies & Libraries Used

* Python
* Pandas
* NumPy
* Scikit-learn
* Matplotlib
* Seaborn
* Joblib

---

##  Step-by-Step Implementation

### 1️ Data Loading

The training and testing datasets are loaded using Pandas to allow easy data manipulation and analysis.

### 2️ Feature and Label Separation

* Features (X): All sensor measurements
* Labels (y): Activity column

This separation is essential for supervised learning.

### 3️ Label Encoding

Since machine learning models work with numbers, textual activity labels are converted into numerical form using `LabelEncoder`.

Example mapping:

```
0 → LAYING
1 → SITTING
2 → STANDING
3 → WALKING
4 → WALKING_DOWNSTAIRS
5 → WALKING_UPSTAIRS
```

### 4️ Feature Scaling

Sensor values may have different ranges. Standardization is applied using `StandardScaler` to ensure all features contribute equally during model training.

### 5️ Model Training

A **Logistic Regression** classifier is used as the baseline model due to its efficiency and strong performance on HAR datasets.

The model learns the relationship between sensor patterns and activity labels.

### 6️ Model Evaluation

The trained model is evaluated using:

* Accuracy score
* Classification report (Precision, Recall, F1-score)
* Confusion matrix visualization

These metrics help assess both overall and class-wise performance.

### 7️ Confusion Matrix Visualization

A heatmap-based confusion matrix is plotted to visually analyze correct and incorrect predictions across activity classes.

### 8️ Model Saving

The trained model, scaler, and label encoder are saved using Joblib, enabling reuse without retraining.

Saved files:

* `har_model.pkl`
* `scaler.pkl`
* `label_encoder.pkl`

---

##  Results

* Achieved high classification accuracy on test data
* Strong performance on both static and dynamic activities
* Minor confusion observed between similar movement activities

---

##  Key Learnings

* End-to-end machine learning workflow
* Data preprocessing and feature scaling
* Supervised classification modeling
* Model evaluation and interpretation
* Saving and reusing trained models

---

##  Applications

* Fitness and activity tracking apps
* Healthcare monitoring systems
* Smart wearable devices
* Human behavior analysis

---

##  Future Enhancements

* Add multiple ML models (SVM, Random Forest) for comparison
* Perform PCA or t-SNE for feature visualization
* Implement deep learning models (LSTM, CNN)
* Deploy model using Flask or FastAPI

---

## 🧾 Resume Description

**Human Activity Recognition using Machine Learning**
Developed a supervised machine learning system to classify human activities from smartphone sensor data. Implemented data preprocessing, feature scaling, Logistic Regression modeling, and performance evaluation using confusion matrix and classification metrics.

---

##  Conclusion

This project demonstrates a complete and practical implementation of a real-world machine learning problem. It highlights the importance of data preprocessing, proper model evaluation, and systematic workflow in building reliable ML systems.

---
