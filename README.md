# EEG Biomarker Analysis: Alzheimer's Disease, FTD, and Healthy Controls

Independent research project analysing resting-state EEG from 88 subjects 
(OpenNeuro ds004504) using MNE-Python.

## Key Findings
- Theta/alpha ratio correlates strongly with MMSE cognitive scores (r = -0.49, p < 0.000001)
- Individual alpha frequency significantly lower in AD (8.13 Hz) vs HC (9.56 Hz)
- Alpha-band PLV connectivity disrupted in posterior regions in AD
- SVM achieves 72.4% accuracy distinguishing AD from healthy controls

## Pipeline
Preprocessing → PSD Band Power → Theta/Alpha Ratio → IAF → 
Alpha PLV Connectivity → ML Classification → Age-corrected Statistics

## Dataset
OpenNeuro ds004504 — 88 subjects (36 AD, 23 FTD, 29 HC)
https://openneuro.org/datasets/ds004504

## Tools
MNE-Python, mne-connectivity, scikit-learn, pingouin, pandas, seaborn

## Author
Arnav Verma — BSc Psychology Honours, Christ (Deemed to be University), Delhi NCR
Independent Research, 2025
