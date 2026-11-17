# Changelog

## 17/11/2026
- Added `04_final_model.ipynb`: threshold chosen with cross-validation, engineered features (power and temperature difference) and a time-ordered split check.
- Shortened the findings in notebooks 03 and 04 and added training-only data checks.
- Updated notebooks 01 and 02: replaced outdated Milestone 3 references, removed the unkept `RobustScaler` and experiment-log promises, and added the rotational speed effect to the coefficient findings.
- Added notebook 04 and the notebook 03 run time to the README.
- Added permutation importance, the final test-set evaluation (F2 0.833), test-set error analysis, a per-type fairness check and responsible-use notes to `04_final_model.ipynb`.

## 05/11/2026
- Added `03_models_and_evaluation.ipynb`: kNN, Decision Tree and Random Forest tuned with cross-validation, precision-recall curves, a confusion matrix, error analysis by failure mode and a draft conclusion (Milestone 3).

## 13/10/2026
- Added baseline diagnostics, coefficient interpretation, an experiment log and a summary to `02_baseline.ipynb` (Week 5).

## 02/10/2026
- Added the evaluation protocol, configuration, stratified split, preprocessing pipeline and baselines in `02_baseline.ipynb` (Week 4).
- Chose F2 as the primary metric instead of F1, because missed failures cost more than false alarms.
- Added a time-order check to the leakage register in `01_data_audit.ipynb`.

## 30/09/2026
- Completed the data audit in `01_data_audit.ipynb`.

## 25/09/2026
- Submitted the project proposal and set up the repository, environment and dataset.