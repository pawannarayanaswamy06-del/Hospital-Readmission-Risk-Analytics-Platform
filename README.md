# Hospital Readmission Risk Analytics Platform

**Author:** Pawan Narayanaswamy  
**Focus Areas:** Healthcare Analytics, Machine Learning, Explainable AI, Fairness Analysis, Streamlit, MLOps

---

## Overview

Hospital Readmission Risk Analytics Platform is an end-to-end machine learning application designed to predict the probability of 30-day hospital readmission using patient demographics, medical history, hospitalization details, and clinical measurements.

The platform combines predictive modeling, explainable AI, fairness analysis, database-backed patient record management, and an interactive Streamlit interface to support data-driven healthcare decision-making and operational planning.

---

## Business Problem

Hospital readmissions represent a significant clinical and financial challenge for healthcare organizations. Preventable readmissions increase treatment costs, reduce hospital capacity, and may indicate gaps in discharge planning, medication adherence, chronic disease management, or post-discharge follow-up.

This project demonstrates how machine learning can help healthcare providers proactively identify high-risk patients and prioritize targeted interventions to improve patient outcomes and reduce avoidable readmissions.

---

## Objectives

- Predict the likelihood of patient readmission within 30 days of discharge
- Provide interpretable explanations using SHAP (SHapley Additive Explanations)
- Evaluate fairness across demographic groups
- Store patient records and predictions in a relational database
- Deliver insights through an interactive Streamlit application
- Support testing, linting, and CI/CD workflows

---

## Key Features

- 🔍 **Readmission Risk Prediction** using machine learning classification models
- 📊 **Explainable AI** with SHAP feature importance visualizations
- ⚖️ **Fairness Analysis** across demographic segments
- 💾 **Database Integration** using SQLAlchemy
- 🎨 **Interactive Streamlit Dashboard**
- 🧪 **Automated Testing** with pytest
- 🧹 **Code Quality Checks** with flake8 and black
- 🚀 **CI/CD Pipeline** with GitHub Actions

---

## Tech Stack

### Programming & Analytics
- Python
- Pandas
- NumPy
- Scikit-learn

### Explainability & Visualization
- SHAP
- Matplotlib

### Application Development
- Streamlit

### Database
- SQLAlchemy

### Testing & Quality
- Pytest
- Flake8
- Black

### DevOps & CI/CD
- Git
- GitHub Actions

---

## Project Architecture

```text
Patient Data Input
        ↓
Data Validation & Preprocessing
        ↓
Feature Engineering
        ↓
Machine Learning Model
        ↓
Risk Probability Prediction
        ↓
SHAP Explainability
        ↓
Fairness Analysis
        ↓
Database Storage
        ↓
Streamlit Dashboard 
```

## Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/pawannarayanaswamy06-del/hospital-readmission-risk-analytics-platform.git
cd hospital-readmission-risk-analytics-platform
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Initialize the database:
```bash
python -c "from db.database import db; db.init_db()"
```

5. Run the application:
```bash
streamlit run src/app.py
```

## Development

### Running Tests
```bash
pytest tests/
```

### Code Formatting
```bash
black .
flake8 .
```

## Project Structure

```
hospital-readmission-prediction/
├── .github/
│   └── workflows/
│       └── test.yml
├── data/
│   └── synthetic_readmission_data.csv
├── models/
│   └── readmission_model.pkl
├── src/
│   ├── app.py
│   ├── explainability.py
│   ├── fairness_analysis.py
│   └── services/
│       └── patient_service.py
├── tests/
│   └── test_app.py
├── db/
│   ├── database.py
│   └── models.py
├── requirements.txt
└── README.md
```

## Usage

1. **Prediction Tab**
   - Enter patient information
   - Fill in medical history and clinical measurements
   - Click "Predict Readmission Risk" to get the prediction
   - View the risk percentage and SHAP explanation

2. **Model Explainability Tab**
   - View SHAP summary plot
   - Explore feature importance table

3. **Fairness Analysis Tab**
   - Analyze model performance across different demographic groups
   - View fairness metrics and visualizations

## Business Impact

This solution can help healthcare organizations:

- Identify high-risk patients prior to discharge
- Improve care coordination and follow-up planning
- Reduce preventable readmissions
- Lower operational and treatment costs
- Support value-based care initiatives
- Increase transparency in AI-assisted decision-making

## Model Details

The system uses a machine learning model trained on historical patient data to predict readmission risk. The model considers various factors including:

- Patient demographics
- Medical history
- Clinical measurements
- Hospital stay information
- Previous admissions

## Future Enhancements
- MLflow experiment tracking
- FastAPI prediction endpoint
- Docker containerization
- Streamlit Cloud deployment
- Model drift monitoring
- Advanced patient cohort analysis
- Power BI executive dashboard

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Dataset: Synthetic hospital readmission data
- SHAP library for model explainability
- Streamlit for the web interface
