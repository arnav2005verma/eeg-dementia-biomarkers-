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

## How to Run
1. Download the dataset from https://openneuro.org/datasets/ds004504
2. Install dependencies: `pip install mne mne-connectivity pandas numpy matplotlib seaborn scipy scikit-learn pingouin`
3. Open `eeg_alzheimers_analysis.ipynb` in JupyterLab and run cells in order

## Files
- `eeg_alzheimers_analysis.ipynb` — full analysis pipeline
- `Verma_EEG_Dementia_complete.docx` — manuscript
- Figures — all output plots included in repository

## Author
Arnav Verma — BSc Psychology Honours, Christ (Deemed to be University), Delhi NCR
Independent Research, 2025
