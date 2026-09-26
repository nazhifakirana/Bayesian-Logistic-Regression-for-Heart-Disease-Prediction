# Bayesian Logistic Regression for Heart Disease Prediction

A Bayesian Logistic Regression project that analyzes factors associated with heart disease and estimates the probability of disease occurrence while accounting for uncertainty in model parameters.

## Project Overview

This project applies Bayesian Logistic Regression to investigate the relationship between selected health-related factors and heart disease outcomes.

The analysis uses Markov Chain Monte Carlo (MCMC) methods to estimate posterior distributions, assess model convergence, interpret parameter uncertainty, and evaluate predictive performance.

This project was completed as a group project, with my primary contribution focused on coding, statistical modeling, and data analysis.

## My Contribution

- 80% Coding & Statistical Modeling
- Bayesian model specification
- MCMC-based inference
- Model convergence diagnostics
- Posterior analysis
- Model evaluation and interpretation
- Technical & data analysis

## Methodology

### 1. Bayesian Logistic Regression

A Bayesian Logistic Regression model was developed using a Bernoulli likelihood:

```text
yᵢ ~ Bernoulli(πᵢ)

logit(πᵢ) = β₀ + β₁x₁ᵢ + β₂x₂ᵢ + β₃x₃ᵢ
```

Weakly informative priors were assigned to the model parameters:

```text
β₀, β₁, β₂, β₃ ~ N(0, 1)
```

### 2. MCMC Inference

Posterior inference was performed using **JAGS** with two parallel MCMC chains.

The following diagnostics were used to evaluate convergence:

- R-hat
- Geweke diagnostic
- Effective Sample Size (ESS)

The model produced R-hat values around **1.00–1.01**, with effective sample sizes above **1,900**.

### 3. Posterior Analysis

Posterior means and 95% credible intervals were analyzed to understand the relationship between predictors and heart disease outcomes.

The analysis found:

- **Max Heart Rate** had the strongest effect.
- **Cholesterol** showed a meaningful association with the outcome.
- **Age** showed inconclusive evidence.

### 4. Model Evaluation

Model fit and predictive adequacy were evaluated using:

- DIC
- WAIC
- Posterior Predictive Check
- Confusion Matrix
- Accuracy
- Sensitivity
- Specificity
- Balanced Accuracy

## Results

The model achieved approximately **68.68% accuracy**.

| Metric | Result |
|---|---:|
| Accuracy | 68.68% |
| Sensitivity | 65.13% |
| Balanced Accuracy | 68.59% |
| Specificity | 72.05% |

### Confusion Matrix

|  | Actual 0 | Actual 1 |
|---|---:|---:|
| **Predicted 0** | 325 | 147 |
| **Predicted 1** | 174 | 379 |

## Key Findings

The posterior analysis identified **Max Heart Rate** as the strongest predictor in the model, while **Cholesterol** also showed a meaningful association with heart disease outcomes.

The effect of **Age** remained inconclusive based on its 95% credible interval.

The model demonstrates how Bayesian Logistic Regression can provide both predictions and interpretable estimates of parameter uncertainty.

## Tech Stack

- R
- JAGS
- MCMC
- Bayesian Statistics
- Logistic Regression
- Statistical Modeling

## Project Structure

```text
├── data/
├── R/
├── HTML/
├── Paper/
└── README.md
```

## Project Resources

- [HTML Report](#)
- [Research Paper](#)
- [R Source Code](#)
- [Dataset](#)

## Team

**By Data Science Students — BINUS University**

- **2802545655 — Nazhifa Kirana Mulia Nugraha**
- **2802504876 — Michael Yeremia**
- **2802545466 — Samuel Christopher**
- **2802524120 — Valentino Kurniawan**
- 
Data Science | Machine Learning | Statistical Modeling
