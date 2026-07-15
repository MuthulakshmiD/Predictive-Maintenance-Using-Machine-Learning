# Predictive-Maintenance-Using-Machine-Learning
# ⚙️ Predictive Maintenance of Industrial Machines Using Machine Learning

## Project Overview

Predictive maintenance is a data-driven approach used to predict machine failures before they occur. This project uses industrial machine sensor data and machine learning techniques to identify failure risks and support preventive maintenance decisions.

The project analyzes mechanical system parameters such as temperature, rotational speed, torque, and tool wear to predict whether a machine will fail.

---

# Problem Statement

Unexpected machine failures can cause:

- Production downtime
- Increased maintenance cost
- Reduced equipment efficiency
- Safety risks

The objective of this project is to build a machine learning model that predicts machine failure using sensor data collected from industrial equipment.

---

# Objectives

- Clean and preprocess mechanical system data
- Analyze machine parameters and identify patterns
- Perform exploratory data analysis (EDA)
- Build a machine learning classification model
- Evaluate model performance
- Predict future machine failures

---

# Dataset

## AI4I 2020 Predictive Maintenance Dataset

The dataset contains simulated industrial machine sensor data.

### Dataset Features

| Feature | Description |
|---|---|
| Type | Machine category |
| Air temperature [K] | Environmental temperature |
| Process temperature [K] | Machine process temperature |
| Rotational speed [rpm] | Machine operating speed |
| Torque [Nm] | Mechanical torque |
| Tool wear [min] | Tool usage time |

### Target Variable

```
Machine failure
```

Values:

```
0 → Machine operating normally

1 → Machine failure detected
```

---

# Technologies Used

## Programming Language

- Python

## Libraries

- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib

---

# Machine Learning Algorithm

## Random Forest Classifier

Random Forest was selected because:

- Handles nonlinear relationships
- Works well with sensor data
- Provides feature importance
- Reduces overfitting compared to single decision trees

---

# Project Workflow

## 1. Data Collection

Loaded industrial machine sensor dataset.

---

## 2. Data Cleaning

Performed:

- Missing value checking
- Duplicate removal
- Data type verification
- Feature preprocessing

---

## 3. Data Preprocessing

Steps:

- Converted categorical machine type into numerical values
- Removed unnecessary identifier columns
- Removed failure-mode columns to prevent data leakage

Removed columns:

```
UDI
Product ID
TWF
HDF
PWF
OSF
RNF
```

---

# 4. Exploratory Data Analysis

Performed analysis using visualization techniques.

### Visualizations Created:

## Correlation Heatmap

Used to understand relationships between machine parameters.

## Feature Distribution Analysis

Analyzed:

- Temperature variations
- Torque distribution
- Rotational speed
- Tool wear patterns

---

# 5. Model Development

## Data Split

Dataset divided into:

```
80% Training Data

20% Testing Data
```

---

## Model Training

Algorithm:

```
Random Forest Classifier
```

Parameters:

```
Number of Trees = 100
Random State = 42
```

---

# 6. Model Evaluation

Evaluation metrics used:

## Accuracy

Measures overall prediction correctness.

## Precision

Measures how many predicted failures were actually failures.

## Recall

Measures how many actual failures were detected.

## F1 Score

Balance between precision and recall.

## Confusion Matrix

Shows:

- Correct predictions
- Incorrect predictions

---

# Results

The Random Forest model achieved approximately:

```
95% - 98% Accuracy
```

Performance may vary depending on train-test split and preprocessing.

---

# Feature Importance

The model identifies important machine parameters affecting failures.

Important factors include:

- Tool wear
- Torque
- Rotational speed
- Process temperature
- Air temperature

---

# Project Structure

```
Predictive-Maintenance-ML/

│
├── Predictive_Maintenance_Project.py
│
├── ai4i2020.csv
│
├── predictive_maintenance_model.pkl
│
└── README.md
```

---

# Installation

Clone the repository:

```bash
git clone https://github.com/yourusername/Predictive-Maintenance-ML.git
```

Move into project folder:

```bash
cd Predictive-Maintenance-ML
```

Install required libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib
```

---

# How to Run

Run the Python file:

```bash
python Predictive_Maintenance_Project.py
```

The program will:

- Load data
- Clean data
- Perform analysis
- Train model
- Evaluate model
- Save trained model
- Predict machine failure

---

# Sample Prediction

Example input:

```
Machine Type: 1

Air Temperature: 300 K

Process Temperature: 310 K

Rotational Speed: 1500 rpm

Torque: 40 Nm

Tool Wear: 100 min
```

Output:

```
Machine Operating Normally

Failure Probability: 8.5%
```

---

# Skills Demonstrated

## Data Science

- Data cleaning
- Exploratory Data Analysis
- Statistical analysis
- Data visualization

## Machine Learning

- Classification
- Model training
- Model evaluation
- Feature importance analysis

## Python

- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn

---

# Future Improvements

Possible enhancements:

- Real-time IoT sensor integration
- Cloud deployment
- Power BI dashboard
- Deep learning based failure prediction
- Live machine monitoring system

---

# Applications

This project can be applied in:

- Manufacturing industries
- Automotive production
- Industrial automation
- Equipment monitoring systems
- Smart factories

---


# Conclusion

This project demonstrates how machine learning can be applied to mechanical system data to predict equipment failures and improve maintenance planning through data-driven decision making.
