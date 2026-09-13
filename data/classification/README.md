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

## Expected Local File(s)
- `GeneratedLabelledFlows.zip` / target CSV files (e.g., `Monday-WorkingHours.pcap_ISCX.csv`, `Wednesday-workingHours.pcap_ISCX.csv`, or combined dataset files).
- The exact CSV selection and subset file(s) will be finalized after dataset verification.

## Usage Instructions
- Download the CIC-IDS2017 dataset from the official UNB website.
- Extract and place the required dataset CSV file(s) into this directory (`data/classification/`).

## Git Notice
> [!IMPORTANT]
> Raw dataset files are intentionally excluded from Git tracking via `.gitignore` due to file size considerations and licensing terms. Do not commit `.csv` or `.zip` files to the repository.
