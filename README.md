# Ensemble Methods & Boosting — FAANG-Level Hands-On

**Goal:** Understand why ensembles work (variance reduction, bias reduction), and learn interview-grade intuition for Random Forests, Gradient Boosting, and XGBoost-style thinking.

**Outcome:** Students can:
- explain bagging vs boosting,
- train and tune sklearn RandomForest and GradientBoosting,
- compare against a baseline model,
- reason about overfitting, leakage, and feature importance.

---

# How to Start

1. **Fork** this repository.  
2. Open `ensemble_student_lab.ipynb` in **Google Colab**.  
3. Complete all **TODO** sections.  
4. **Restart runtime → Run All** cells.  
5. Push changes and submit a **Pull Request**.  

⚠️ **Do NOT edit notebooks directly on GitHub.**

---

## Lab Rules (FAANG Style)

- ✅ Always compare to a simple baseline
- ✅ Use train/validation split or CV (no test leakage)
- ✅ Tune only a few meaningful hyperparameters
- ✅ Explain *why* performance changes (bias/variance)

---

# Out of Scope

- Implementing full boosting from scratch
- External XGBoost/LightGBM dependencies (we keep it sklearn-only here)

---

# Notebook Rules

- Do **NOT** rename the notebook  
- Do **NOT** delete TODOs  
- Do **NOT** hardcode outputs  
- Notebook must run **top-to-bottom**  

---

# Dataset

### Default (no download)
- Synthetic binary classification with nonlinearity + noise

### Optional (real dataset)
- UCI Breast Cancer Wisconsin (available via `sklearn.datasets.load_breast_cancer`)

---

## Section 1 — Bagging Intuition (Random Forest)

### Task 1.1: Train baseline vs RandomForest

**Checkpoint Questions:**

- Why does bagging reduce variance?
- Why do trees have high variance?

---

### Task 1.2: OOB score and feature importance

**FAANG Gotcha:**

- Feature importance can be misleading under correlated features.

---

## Section 2 — Boosting Intuition (Gradient Boosting)

### Task 2.1: Compare RF vs GradientBoosting

**Checkpoint Questions:**

- Why can boosting overfit if you use too many estimators?
- What does learning rate do?

---

### Task 2.2: Early stopping intuition

**Interview Angle:**

- Why are shallow trees used as weak learners?

---

## Section 3 — XGBoost-style Thinking (No dependency)

### Task 3.1: Understand regularization knobs

- subsampling
- column sampling
- shrinkage (learning rate)

---

## Submission Expectations

- Completed notebook
- Baseline vs RF vs GB comparison (metrics)
- Short answers to checkpoint questions

---

## FAANG Interview Evaluation Rubric

| Skill                         | Evaluated |
|------------------------------|-----------|
| Bias/variance reasoning       | ✅        |
| Hyperparameter intuition      | ✅        |
| Leakage awareness             | ✅        |
| Correct experimentation       | ✅        |
| Explanation clarity           | ✅        |

---

## Stretch Problems (Optional)

- Compare balanced accuracy / PR-AUC under imbalance
- Implement simple permutation importance
- Add monotonic constraints discussion (conceptual)
