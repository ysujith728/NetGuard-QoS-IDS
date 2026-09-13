# Regression Track Dataset Documentation

## Dataset
UNSW-NB15

## Track
Regression

## Purpose
Predict a continuous network Quality of Service (QoS) and traffic degradation target from flow features.

## Target Variable
- **Current Planned Target**: `sloss` (Source packet loss)

## Official Source
- **Provider**: Cyber Range Lab of the Australian Centre for Cyber Security (ACCS) / UNSW Sydney
- **URL**: [https://research.unsw.edu.au/projects/unsw-nb15-dataset](https://research.unsw.edu.au/projects/unsw-nb15-dataset)

## Expected Local File(s)
- `UNSW_NB15_training-set.csv`

## Usage Instructions
- Download `UNSW_NB15_training-set.csv` from the official UNSW-NB15 dataset repository.
- Place `UNSW_NB15_training-set.csv` directly into this directory (`data/regression/`).
- The experimental design uses the approximately 175,341-row UNSW-NB15 training CSV file to construct an 80:20 train/test split for regression training, validation, and evaluation.

## Git Notice
> [!IMPORTANT]
> The raw CSV dataset file is intentionally excluded from Git tracking via `.gitignore` due to dataset size and redistribution guidelines. Please ensure `UNSW_NB15_training-set.csv` is present in this directory before executing `notebooks/regression.ipynb`.
