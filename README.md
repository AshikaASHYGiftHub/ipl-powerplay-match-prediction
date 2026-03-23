# The Powerplay Effect: Predicting IPL Match Outcomes from Early-Over Performance
### MSc Computing (Data Analytics) — Dublin City University | 2025

## Overview
This project examines how Powerplay performance in the first six overs 
affects IPL match results using machine learning. Using public match-level 
and ball-by-ball data, it explores whether early-over performance can 
reliably predict the final match outcome.

---

## Research Question
Can Powerplay performance (first 6 overs) predict the outcome 
of an IPL match?

---

## Dataset
Two public IPL datasets from Kaggle:

| Dataset | Records |
|---|---|
| Match-level data | 1,095 completed matches |
| Ball-by-ball data | ~260,000 delivery records |

Source: [IPL Complete Dataset 2008–2020](https://www.kaggle.com/datasets/patrickb1912/ipl-complete-dataset-20082020)

Data includes only professional match details (teams, venues, scores, 
wickets) — no personal or sensitive information.

---

## Methods

### Feature Engineering
- Powerplay runs, wickets, run rate, wicket rate
- Net Powerplay Rating (PP-NRR)
- Batting-first status, toss alignment, toss decision
- Historical win rates for batting team, opponent, and venue
- One-hot encoding of categorical variables

### Models Evaluated
| Model | Accuracy |
|---|---|
| Majority Baseline | 0.54 |
| Logistic Regression | 0.58 |
| Decision Tree | 0.52 |
| Random Forest | 0.63 |
| XGBoost | 0.57 |

### Validation
- 80/20 train-test split with stratified sampling
- 5-fold cross-validation
- GridSearchCV for hyperparameter tuning (Random Forest & XGBoost)

---

## Key Findings
- Random Forest achieved the best accuracy at 63%
- Powerplay run rate, PP-NRR, and team strength are the 
  strongest predictors
- Teams scoring more runs early and keeping wickets tend to win more
- Losing wickets early significantly reduces winning probability
- Prediction errors occur mostly in matches where later overs 
  differ greatly from the Powerplay

---

## Tools & Technologies
- Python
- Scikit-learn
- XGBoost
- Pandas
- Matplotlib
- Seaborn
- Jupyter Notebook

---

## Repository Structure

```
ipl-powerplay-match-prediction/
├── Report/
│   └── Report_Machine_Learning.pdf
├── IPL_Project.ipynb
└── README.md
```
---

## Future Enhancements
- Add player-level performance features
- Include pitch and weather conditions
- Build live ball-by-ball prediction model
- Extend to other T20 leagues (BBL, CPL, PSL)

---

## Ethical Considerations
This project uses only publicly available match data with no personal 
or sensitive information. The model is built strictly for academic 
and educational purposes.

---

## Authors
**Ashika Rajkumar**
MSc Computing (Data Analytics), Dublin City University
ashika.rajkumar2@mail.dcu.ie

**Avinash Rajasekar**
MSc Computing (Data Analytics), Dublin City University

**Haritha Ramadass**
MSc Computing (Data Analytics), Dublin City University

**Kundan Raghavendra Rao**
MSc Computing (Data Analytics), Dublin City University

## Contributions
| Task | Ashika | Avinash | Haritha | Kundan |
|---|---|---|---|---|
| Data cleaning & preprocessing | Yes | | | |
| Feature engineering | Yes | | | |
| Dataset merging | Yes | | | |
| Result interpretation | Yes | | | |
| Report writing & documentation | Yes | | | Yes |
| ML model development | | Yes | | |
| Model training & evaluation | | Yes | | |
| Performance evaluation | | Yes | | |
| Exploratory data analysis | | | Yes | |
| Data visualisation | | | Yes | |
| Powerplay prediction | | | Yes | |
| Model comparison | | | Yes | |
| Dataset identification | | | | Yes |
| Literature review | | | | Yes |
| Report formatting | | | | Yes |

