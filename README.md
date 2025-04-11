# 🧪 XRF Cleaner for Drilling Geochemistry

![Python](https://img.shields.io/badge/python-3.10-blue.svg)
![Status](https://img.shields.io/badge/status-field--tested-green)


> A field-tested Jupyter notebook pipeline to clean, organize, and consolidate batch exports from Olympus Vanta portable XRF devices. Built for high-frequency sampling environments like **mudlogging**, this tool automates creation of structured geochemical datasets on a per-well basis.

---

## 🛠️ Features

-  Cleans raw `.csv` exports from Olympus Vanta
-  Skips calibration and beam spectral files
-  Auto-generates **per-well master sheets**
-  Logs processed files to avoid duplication
-  Supports "dry-run" QA/QC mode
-  Can handle hundreds of files in batch mode

---

## 📂 File Structure

```bash
xrf-cleaner-repo/
├── notebooks/
│   ├── Multi_File_XRF_Cleaner.ipynb
│   └── Single_File_XRF_Cleaner.ipynb
├── sample_data/
│   └── chemistry-841515-*.csv
├── processed/
│   └── master_Sample Data.csv
├── README.md
└── .gitignore
```
----
## 🚀 Quickstart

**1. Clone this repo:**

```bash
git clone https://github.com/jdoan-ds/XRF_Cleaner.git
cd XRF_Cleaner
```

**2. (Optional) Create a virtual environment:**
```bash
python3 -m venv venv
source venv/bin/activate
```

**3. Install requirements**
```bash
pip install -r requirements.txt
```

**4. Open the notebook:**
```bash
jupyter lab
```

----

## 📊 Sample Output

Each well will have a master_<well_name>.csv generated that includes:
	•	Cleaned elemental data
	•	Metadata from instrument
	•	Processing log reference
    
----

## 💬 Questions?

Open an issue or send a pigeon.

----

