# Ulcer-Health-Risk-Analysis

Python + Power BI Project | Patient Risk Assessment | Clinical Insights & Visualization

## 📚 Table of Contents
* Project Overview
* Tools & Technologies
* Dataset Breakdown
* Data Preparation & Feature Engineering
* Power BI Dashboard
* Key Visualizations
* Insights & Findings
* Recommendations
* Future Work
  
## 📖 Project Overview
Gastric and peptic ulcers are among the most common gastrointestinal disorders affecting millions of people worldwide. Early identification of ulcer-related risk factors can significantly improve patient outcomes and reduce complications.

This project analyzes ulcer patient data to identify patterns in ulcer severity, patient demographics, medication usage, pain characteristics, and clinical indicators. Using Python for data cleaning and preprocessing and Power BI for interactive visualization, the project transforms raw healthcare data into actionable insights for healthcare professionals and researchers.

## The dashboard enables users to:

Monitor ulcer prevalence and severity levels
Analyze patient demographics and clinical indicators
Examine medication usage patterns
Explore relationships between ulcer depth, pain severity, and patient history
Support data-driven healthcare decision-making
## 🛠️ Tools & Technologies
* Data Processing
* Python
* Pandas
* NumPy
* Jupyter Notebook
* Data Visualization
* Power BI
* Development Environment
* VS Code
* Jupyter Notebook
* Dataset
* Ulcer Patient Health Dataset
* Clinical and demographic patient records
## 📊 Dataset Breakdown
The dataset contains patient information related to ulcer diagnosis, severity, and treatment.

## Key Variables
Category	Features
Demographics	Age, BMI
Clinical Indicators	Hemoglobin Level, Ulcer Size
Medical History	Previous Ulcer History
Symptoms	Pain Severity, Pain Pattern
Diagnosis	Ulcer Depth Classification
Treatment	Medication Type
Ulcer Depth Categories

## Patients were classified into:

Erosion
Superficial Ulcer
Deep Ulcer

These categories help evaluate disease progression and treatment requirements.

## 🧹 Data Preparation & Feature Engineering

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

```

The processed dataset was then imported into Power BI for dashboard creation and visualization.

## 📈 Power BI Dashboard

The dashboard provides an interactive overview of ulcer-related health indicators and patient characteristics.

<img width="1206" height="673" alt="image" src="https://github.com/user-attachments/assets/42eea6ca-d7ad-47db-9846-14f8b10cf1c7" />


## Dashboard Highlights
## 👥 Total Patients
Displays the total number of patients included in the study.
## ⚖️ Average BMI
Provides an overview of patient body mass index distribution.
## 🩸 Average Hemoglobin Level
Monitors average hemoglobin levels, an important indicator of ulcer-related bleeding risks.

## 📉 Ulcer Depth Distribution
Visualizes the prevalence of:
*Erosion
*Superficial Ulcers
*Deep Ulcers
## 📜 Ulcer History Distribution
Analyzes previous, recurrent, and first-time ulcer cases.

## 💊 Medication Analysis
Examines treatment patterns across:
NSAIDs, Aspirin and No Medication
## 🔥 Pain Pattern Distribution
Explores pain occurrence patterns including:
Postprandial, Fasting, Nocturnal and Mixed Pain

## 👨‍⚕️ Age Group Analysis
Shows ulcer prevalence across different age groups.

## 📊 Key Visualizations
1️⃣ Patient Overview
Provides high-level statistics including:Total Patients, Average BMI and Average Hemoglobin Level

2️⃣ Ulcer Severity Analysis
Highlights the distribution of ulcer depth classifications and identifies the most prevalent ulcer type.

3️⃣ Medication Usage Patterns
Examines the relationship between medication exposure and ulcer occurrence.

4️⃣ Pain Pattern Analysis
Provides insight into symptom presentation among ulcer patients.

5️⃣ Age-Based Risk Distribution
Identifies age groups most affected by ulcer conditions.

## 🔍 Insights & Findings
1. Erosive Ulcers Were Most Common
The analysis revealed that erosive ulcers represented the largest proportion of diagnosed ulcer cases.
2. Medication Usage Influences Ulcer Risk
Patients using NSAIDs and Aspirin demonstrated notable ulcer prevalence, highlighting the known gastrointestinal risks associated with these medications.
3. Pain Patterns Vary Across Patients
Postprandial and fasting pain were among the most frequently reported symptoms, providing valuable indicators for clinical assessment.
4. Previous Ulcer History Remains a Significant Risk Factor
Patients with a history of ulcers showed increased likelihood of recurrent ulcer development.
5. Hemoglobin Levels Can Support Risk Assessment
Lower hemoglobin levels may indicate bleeding-related complications and warrant closer clinical monitoring.

## 🩺 Recommendations
Based on the analysis, the following recommendations are proposed:
## 1. Early Risk Screening to identify high-risk patients.
Healthcare providers should regularly monitor:BMI, Hemoglobin levels, Ulcer history and Medication usage
## 2. Medication Monitoring
Patients on long-term NSAIDs or Aspirin therapy should receive periodic gastrointestinal assessments to minimize ulcer complications.
## 3. Clinical Decision Support
Integrating dashboards like this into healthcare systems can help clinicians:Track patient trends, Detect risk patterns
and Support evidence-based treatment decisions
## 4. Patient Education
Educating patients about: Medication risks, Dietary habits, and Symptom recognition can improve prevention and early intervention.

## 🚀 Future Work
*Machine Learning Integration
*Develop predictive models to estimate ulcer risk and severity.
*Potential algorithms: Random Forest, XGBoost, Logistic Regression and Real-Time Monitoring
*Integrate live patient records for continuous risk assessment.
-Web-Based Healthcare Dashboard


## 🙏 Acknowledgements

Special thanks to the healthcare analytics community, Power BI developers, and open-source Python contributors whose tools and resources made this project possible.
