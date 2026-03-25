# Fruit Classifier — Bosch Data Science Project
**Goal:** Multi-class classification to distinguish apples, bananas, and grapes using color, size, and weight.

---

## 📁 Repository Structure

| File | Description |
|---|---|
| `BOSCH.ipynb` | Full Jupyter Notebook (preprocessing + models) |
| `fruit_classifier_documentation.pdf` | Complete project documentation |
| `fruit_data.xlsx` | Raw dataset (200 records) |

---

## ⚙️ Preprocessing Steps

- Removed missing values
- Lowercased and stripped whitespace
- Removed stray digits from text columns (`Yellow1` → `yellow`)
- Fuzzy matching for typo correction (`largee` → `large`)
- Per-fruit IQR outlier removal on weight
- Label encoding for categorical features

---

## 🤖 Models & Results

| Model | Test Size | Test Accuracy | F1 Weighted | ROC-AUC |
|---|---|---|---|---|
| Decision Tree | 0.30 | 86.21% | 0.8621 | 0.9555 |
| Random Forest | 0.15 | 82.05% | 0.8205 | 0.9378 |
| Logistic Regression | 0.15 | 64.10% | 0.6124 | 0.8193 |

> ✅ **Best model: Decision Tree** — highest accuracy and ROC-AUC with no overfitting.

---

## 🔧 Tuning Methodology

- **GridSearchCV** — exhaustive hyperparameter search
- **Stratified K-Fold** (5 splits) — preserves class ratios per fold
- **Scoring metric:** F1 Weighted

---

## 🛠️ Tech Stack

`Python` · `Jupyter Notebook` · `Scikit-learn` · `Pandas` · `Matplotlib` · `Seaborn`
