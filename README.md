# Clinical Data Automation — Rave to SDTM Pipeline

Automated mapping of raw Medidata Rave data exports to **CDISC SDTM-compliant datasets** using Python.

Built from 7+ years of hands-on Medidata Rave study build experience — this tool solves a real problem: manual SDTM mapping from Rave exports is time-consuming, error-prone, and inconsistent across studies. This pipeline automates the most repetitive parts.

---

## What This Does

- Ingests raw `.csv` exports from Medidata Rave
- Applies wide-to-long transformation logic for vital signs, labs, and demographics
- Normalises dates to ISO 8601 format (as required by CDISC submission standards)
- Outputs SDTM-structured datasets for key domains: `DM`, `VS`, `LB`, `AE`
- Flags records that fail basic SDTM conformance checks

---

## SDTM Domains Covered

| Domain | Description |
|--------|-------------|
| DM | Demographics |
| VS | Vital Signs |
| LB | Laboratory Test Results |
| AE | Adverse Events |

---

## Tech Stack

- Python 3.9+
- Pandas, NumPy
- Jupyter Notebook

---

## Project Structure

```
clinical-data-automation-python/
│
├── data/
│   ├── raw/                  # Sample Rave export CSVs (anonymised/synthetic)
│   └── sdtm_output/          # Generated SDTM datasets
│
├── notebooks/
│   ├── 01_rave_to_dm.ipynb   # Demographics domain mapping
│   ├── 02_rave_to_vs.ipynb   # Vital Signs domain mapping
│   ├── 03_rave_to_lb.ipynb   # Lab Results domain mapping
│   └── 04_rave_to_ae.ipynb   # Adverse Events domain mapping
│
├── src/
│   ├── mapper.py             # Core mapping functions
│   ├── date_utils.py         # ISO 8601 date normalisation
│   └── validator.py          # Basic SDTM conformance checks
│
├── requirements.txt
└── README.md
```

---

## Quick Start

```bash
git clone https://github.com/Puneetha-M/clinical-data-automation-python
cd clinical-data-automation-python
pip install -r requirements.txt
jupyter notebook notebooks/01_rave_to_dm.ipynb
```

---

## Clinical Context

In clinical trials, SDTM (Study Data Tabulation Model) is required by FDA and EMA for regulatory submissions. Raw EDC data from Medidata Rave must be transformed, mapped, and validated before it can be submitted. This pipeline demonstrates that transformation end-to-end on synthetic data.

---

## Author

**Puneetha** — Medidata Rave Certified Study Builder | MSc Data Analytics @ BSBI Berlin  
[LinkedIn](https://www.linkedin.com/in/puneetham/) | [GitHub](https://github.com/Puneetha-M)
