# XRF Cleaner for Drilling Geochemistry

This repository contains two field-tested Jupyter notebooks used to clean and organize batch and single-file exports from Olympus Vanta portable XRF devices during drilling operations.

Built by a working mudlogger transitioning into data science, these tools are tailored for high-frequency sampling environments like mudlogging, with a focus on QA/QC, logging, and structured dataset creation.

---

## 🚀 Contents

### `notebooks/Single_File_XRF_Cleaner.ipynb`
- Processes a single Vanta `.csv` export
- Cleans column headers
- Converts `wt%` values to `ppm`
- Handles zero division errors
- Clips outliers between the 1st and 99th percentiles

### `notebooks/Multi_File_XRF_Cleaner.ipynb`
- Batch processes multiple `chemistry-*.csv` files
- Tracks processed files in a log to avoid duplication
- Extracts well names from serial numbers via dictionary mapping
- Saves cleaned individual files and updates per-well master sheets
- Includes dry-run mode and a QA/QC summary dashboard

---

## 🧪 Features

- Unit conversion: wt% to ppm
- QA/QC filtering (outlier clipping, 0 replacement)
- File-level logging to prevent reprocessing
- Per-well master dataset creation
- Configurable dry run for safe testing
- Summary dashboard reporting for every run

---

## 🗂️ Structure

xrf-cleaner-repo/
├── notebooks/
│   ├── Single_File_XRF_Cleaner.ipynb
│   └── Multi_File_XRF_Cleaner.ipynb
├── sample_data/             # (optional demo CSVs)
├── processed/               # <- ignored via .gitignore
├── README.md
└── .gitignore
---

## 📦 Requirements

- Python 3.x
- pandas

Install with:

```bash
pip install pandas

💼 Author

Built by a field-based mudlogger transitioning into data science. This project reflects real-world needs in scientific drilling workflows and demonstrates applied ETL, data cleaning, and QA/QC logic.
