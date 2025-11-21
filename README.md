# DA5401 Data Challenge

Name: Kaki Hephzi Sunanda

Roll Number: DA25M015

This repository contains the implementation, experiments, and final submission files for the DA5401 course project (Kaggle Challenge). The objective of the task was to predict a continuous *fitness score* (0–10) from text–based metric evaluations. After extensive experimentation with both regression and classification paradigms, the final solution adopts a **classification-based CatBoost model** with expectation decoding, achieving a **Kaggle Public Score of 3.624**.

## Repository Structure

```
.
├── DA25M015_Project.ipynb          # Main project notebook with full pipeline 
├── rough_test_notebooks/           # Scratch notebooks used for isolated experiments and tests
├── submissions/                    # All generated CSV submission files for Kaggle
└── README.md                       # Project documentation
```

- **DA25M015_Project.ipynb**  
  Contains the final evaluation.

- **rough_test_notebooks/**  
  Miscellaneous experiment notebooks. These were used for quick tests and exploratory trials.  
  (Not cleaned or commented)

- **submissions/**  
  All Kaggle submission CSVs, including intermediate experiments and the final model output.

## Summary of Approach

The project explored multiple modelling strategies, including:
- Linear and tree-based regressors
- XGBoost & LightGBM regression
- Classification-based CatBoost
- Model ensembling and calibration trials
- Neural network MLP classifier experiments

After systematic validation, classification emerged superior due to:
- Better stability under label imbalance
- More consistent generalization under distribution shift
- Smooth expected-score decoding using class probabilities

The final CatBoost configuration delivered the best performance.

##### Final Performance

- **Kaggle Public Score:** 3.624  
- **Model:** CatBoostClassifier
- **Chosen due to:** strong bias–variance balance, robustness to tabular data, and fast convergence.

---

