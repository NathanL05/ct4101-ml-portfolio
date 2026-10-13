## Predicting Machine Failure from Sensor Readings

CT4101 Machine Learning portfolio project

## Question
Can we predict whether a milling machine will fail (yes/no) using sensor data like temperature, speed, torque and tool wear? This is a binary classification problem. The idea is to flag machines for a maintenance check, not to replace normal inspections.

## Dataset
AI4I 2020 Predictive Maintenance Dataset from the UCI Machine Learning Repository (CC BY 4.0). 10,000 rows, about 3.4% are failures. See [data/README.md](data/README.md) for the source, licence and citation.

## Setup
Tested with Python 3.13.11 on macOS.

```bash
python3 -m venv .venv
source .venv/bin/activate        # Windows: .venv\Scripts\activate
pip install -r requirements.txt
```

## How to run
From the project folder, with the virtual environment active:

```bash
jupyter lab
```

Open the notebooks in `notebooks/` in order and run each one with **Kernel → Restart Kernel and Run All Cells**:

1. `01_data_audit.ipynb` – data audit, leakage register and candidate features
2. `02_baseline.ipynb` – evaluation protocol, train/test split, preprocessing pipeline and baselines

Notebook 02 writes the cross-validation results to `reports/experiment_log.csv`. All randomness uses seed 42.

## Project structure
```
data/            dataset and data README
notebooks/       numbered notebooks, run in order
reports/         experiment log (and later figures)
ASSISTANCE.md    declaration of AI and other help
CHANGELOG.md     project changelog
requirements.txt package versions
```

Repository: https://github.com/NathanL05/ct4101-ml-portfolio