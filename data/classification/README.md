# Classification Track Dataset Documentation

## Dataset
CIC-IDS2017

## Track
Classification

## Purpose
Network attack and intrusion traffic classification into multi-class threat categories and benign activity.

## Official Source
- **Provider**: Canadian Institute for Cybersecurity (CIC), University of New Brunswick (UNB)
- **URL**: [https://www.unb.ca/cic/datasets/ids-2017.html](https://www.unb.ca/cic/datasets/ids-2017.html)

## File
`network_traffic_classification.csv`

## Dataset Details
- **Filename**: `network_traffic_classification.csv`
- **File Size**: ~214.74 MB (225,177,324 bytes)
- **Rows**: 692,703 (610,492 after cleaning duplicates, NaN, and Inf values)
- **Columns**: 79 (69 after removing zero-variance features)
- **Target Variable**: `Label` (Multiclass: BENIGN, DoS Hulk, DoS GoldenEye, DoS slowloris, DoS Slowhttptest, Heartbleed)

## Usage Instructions
- The raw dataset `network_traffic_classification.csv` is located in this directory (`data/classification/`).
- The dataset is tracked via **Git LFS** (Large File Storage).

## Git Notice
> [!NOTE]
> The raw classification dataset (`network_traffic_classification.csv`) is tracked in this repository using **Git LFS**. Ensure `git lfs pull` is executed after cloning.
