# \# Fruit Classifier — Bosch Data Science Project

# 

# \## Problem Statement

# A multi-class classification project to distinguish between \*\*apples\*\*, \*\*bananas\*\*, and \*\*grapes\*\* using color, size, and weight as input features.

# 

# \## Dataset

# \- 200 records, 4 columns: `fruit\_type`, `color`, `size`, `weight`

# \- Target label: `fruit\_type`

# 

# \## Preprocessing

# \- Removed missing values

# \- Lowercased and stripped whitespace from text columns

# \- Removed stray digits (e.g. `Yellow1` → `yellow`)

# \- Fuzzy matching to fix typos (e.g. `largee` → `large`)

# \- Per-fruit IQR outlier removal on weight column

# \- Label encoding for categorical features

# 

# \## Models \& Results

# 

# | Model | Test Accuracy | F1 Weighted | ROC-AUC |

# |---|---|---|---|

# | Decision Tree | 86.21% | 0.8621 | 0.9555 |

# | Random Forest | 82.05% | 0.8205 | 0.9378 |

# | Logistic Regression | 64.10% | 0.6124 | 0.8193 |

# 

# \## Tuning Methodology

# \- GridSearchCV with Stratified K-Fold (5 splits)

# \- Scoring metric: F1 Weighted

# 

# \## Files

# \- `BOSCH.ipynb` — Full Jupyter Notebook with all code

# \- `fruit\_classifier\_documentation.pdf` — Project documentation

# \- `fruit\_data.xlsx` — Dataset

