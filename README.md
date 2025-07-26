# AI-ETHICS
week 7 AI ASSIGNMENT

# Fairness Assessment using COMPAS Dataset

This project explores the fairness of machine learning models using the COMPAS (Correctional Offender Management Profiling for Alternative Sanctions) dataset. We use the AIF360 toolkit to detect and mitigate bias based on race.

---

##  Project Structure

```bash
Fairness-Assessment/
│
├── compas_fairness.ipynb     # Main notebook with bias detection and mitigation
├── compas.csv                # COMPAS dataset
├── README.md                 # Project documentation
└── requirements.txt          # Python dependencies
```

---

## Part 1: Theoretical Foundations (40%)

### 1.1 What is AI Fairness?

AI Fairness involves ensuring that automated decisions do not result in unjust or prejudiced outcomes for individuals, particularly those from marginalized groups.

### 1.2 Protected Attribute

In this project, we focus on **race** as the protected attribute, comparing outcomes for **African-American** and **Caucasian** groups.

---

## Part 2: Dataset & Preprocessing (20%)

- **Dataset**: [ProPublica’s COMPAS dataset](https://github.com/propublica/compas-analysis)
- **Attributes Used**:
  - `Ethnic_Code_Text` (Protected attribute: Race)
  - `DecileScore` (Prediction score)
  - `label` (Ground truth: whether the individual reoffended)

We cleaned the dataset and selected relevant columns before fairness analysis.

---

## Part 3: Fairness Analysis with AIF360 (40%)

### 3.1 Bias Detection

We evaluated **False Positive Rates** between racial groups.

### 3.2 Bias Mitigation

We applied **Reweighing** to balance group weights using AIF360, followed by fairness evaluation using:

- Statistical Parity Difference
- Disparate Impact
- Equal Opportunity Difference

---

## Key Metrics

| Metric                       | Before Reweighing | After Reweighing |
|-----------------------------|-------------------|------------------|
| Statistical Parity Diff     |        TBD        |       TBD        |
| Disparate Impact            |        TBD        |       TBD        |
| Equal Opportunity Difference|        TBD        |       TBD        |

---

##  Conclusion

- The COMPAS model showed racial bias, especially in FPR.
- Reweighing helped mitigate bias and improve fairness across key metrics.

---

##  Requirements

```
Python >= 3.7
aif360
pandas
matplotlib
scikit-learn
```

Install with:

```bash
pip install -r requirements.txt
```

---

## Author

**Hellen Diana Njeri Macharia**  
Data Scientist | AI Fairness Advocate  
Email: hellendiana091@gmail.com

---
