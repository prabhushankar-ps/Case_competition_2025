
# HIV Antiretroviral Regimen Effectiveness Prediction

## Project Overview
This project analyzes antiretroviral therapy (ART) regimens prescribed to HIV patients and builds predictive models to determine which treatment combinations are most effective for achieving clinical success.

Clinical success is defined using three outcomes:
- Viral load ≤ 250 copies/mL (preferably ≤ 50 copies/mL)
- CD4 count ≥ 500 cells/mm³
- Sustained improvement across observed treatment timelines

The project was developed as part of a healthcare analytics case competition and evaluates ART effectiveness across different ethnic groups using machine learning models.

## Problem Statement
With over 30 FDA-approved antiretroviral drugs available, selecting the most effective regimen for a patient is complex. Incorrect or suboptimal choices can lead to higher costs, delayed viral suppression, and additional strain on healthcare systems.

This project aims to:
- Standardize decision-making for ART selection
- Improve patient outcomes
- Reduce unnecessary treatment costs

## Dataset
- Number of patients: 187,236
- Domain: HIV treatment outcomes
- Key variables include:
  - Viral load
  - CD4 count
  - Treatment regimen
  - Ethnicity
  - Time-based clinical measurements

A derived target variable, **All Criteria Met**, was created to indicate whether a patient met all clinical success benchmarks.

## Methodology
1. Data cleaning and exploratory data analysis
2. Feature engineering and outcome labeling
3. Train-test split (80% training, 20% testing, random seed = 43)
4. Class imbalance handling
5. Model development:
   - Random Forest models by ethnicity (Asian, Black, White, Other)
   - Logistic Regression model on full dataset
6. Model evaluation using accuracy on unseen test data

## Models and Results
Random Forest models consistently outperformed the global logistic regression model, highlighting the importance of demographic stratification.

Approximate accuracies:
- Asian ethnicity: ~91%
- Black ethnicity: ~76%
- White ethnicity: ~70%
- Other ethnicities: ~82%
- Logistic regression (overall): ~70%

## Business and Healthcare Impact
- Potential reduction in ART-related monthly costs (currently averaging ~$2,500 per patient)
- Fewer regimen changes and reduced provider burden
- Improved personalization of HIV treatment strategies

## Future Work
- Incorporate additional demographic and clinical features
- Explore fairness-aware and explainable ML approaches
- Extend models to longitudinal outcome prediction
- Provider-facing decision support dashboards

## Repository Structure
```
.
├── Case_competition.ipynb
├── TeamB2_Executive Summary.pdf
├── README.md
```

## Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Jupyter Notebook

## Authors
- Raheela Charania
- Anmol Anchala
- Prabhu Shankar

## Disclaimer
This project is for academic and research purposes only and is not intended for direct clinical use.
