# Ulcer-Health-Risk-Analysis
🩺 Ulcer Health Risk Analysis Dashboard

Python + Power BI Project | Patient Risk Assessment | Clinical Insights & Visualization

📚 Table of Contents
Project Overview
Tools & Technologies
Dataset Breakdown
Data Preparation & Feature Engineering
Power BI Dashboard
Key Visualizations
Insights & Findings
Recommendations
Future Work
📖 Project Overview

Gastric and peptic ulcers are among the most common gastrointestinal disorders affecting millions of people worldwide. Early identification of ulcer-related risk factors can significantly improve patient outcomes and reduce complications.

This project analyzes ulcer patient data to identify patterns in ulcer severity, patient demographics, medication usage, pain characteristics, and clinical indicators. Using Python for data cleaning and preprocessing and Power BI for interactive visualization, the project transforms raw healthcare data into actionable insights for healthcare professionals and researchers.

The dashboard enables users to:

Monitor ulcer prevalence and severity levels
Analyze patient demographics and clinical indicators
Examine medication usage patterns
Explore relationships between ulcer depth, pain severity, and patient history
Support data-driven healthcare decision-making
🛠️ Tools & Technologies
Data Processing
Python
Pandas
NumPy
Jupyter Notebook
Data Visualization
Power BI
Development Environment
VS Code
Jupyter Notebook
Dataset
Ulcer Patient Health Dataset
Clinical and demographic patient records
📊 Dataset Breakdown

The dataset contains patient information related to ulcer diagnosis, severity, and treatment.

Key Variables
Category	Features
Demographics	Age, BMI
Clinical Indicators	Hemoglobin Level, Ulcer Size
Medical History	Previous Ulcer History
Symptoms	Pain Severity, Pain Pattern
Diagnosis	Ulcer Depth Classification
Treatment	Medication Type
Ulcer Depth Categories

Patients were classified into:

Erosion
Superficial Ulcer
Deep Ulcer

These categories help evaluate disease progression and treatment requirements.

🧹 Data Preparation & Feature Engineering

Python was used to clean and prepare the dataset before importing it into Power BI.

Key Processing Tasks
Handling missing values
Standardizing categorical variables
Data validation
Outlier identification
Feature aggregation for dashboard metrics
## Data Preparation & Feature Engineering

Python was used to clean and prepare the ulcer patient dataset before importing it into Power BI.

```python
import pandas as pd
import numpy as np

df = pd.read_csv("ulcer_data.csv")

# Handle missing values
df.fillna(df.mean(numeric_only=True), inplace=True)

# BMI category
df['BMI_Category'] = pd.cut(
    df['BMI'],
    bins=[0,18.5,25,30,100],
    labels=['Underweight','Normal','Overweight','Obese']
)

# Average metrics
avg_bmi = df['BMI'].mean()
avg_hb = df['Hemoglobin'].mean()
```

The processed dataset was then imported into Power BI for dashboard creation and visualization.
