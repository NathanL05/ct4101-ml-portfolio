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

## Project structure
```
data/            dataset and data README
notebooks/       numbered notebooks, run in order
ASSISTANCE.md    declaration of AI and other help
requirements.txt package versions
```