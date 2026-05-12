# EEG Biomarker Analysis: Alzheimer's Disease, FTD, and Healthy Controls

# ABSTRACT

Alzheimer’s Disease (AD) accounts for 60-70% of all dementia cases world-wide, whereas frontotemporal dementia (FTD) is the leading cause of dementia onset before the age of 65. Their electrophysiological profiles and relationships to cognitive severity remain incompletely characterised in open, reproducible pipelines. Resting-state EEG recordings from 88 participants (36 AD, 23 FTD, 29 HC) from OpenNeuro ds004504 were analysed using MNE-Python. Relative band power, theta/alpha ration, Individual Alpha Frequency (IAF), and alpha PLV were extracted. Correlations with MMSE scores were computed with and without age correction, and SVM and Random Forest Classifiers were evaluated using stratified 5-fold cross validation.  The results showed how theta and alpha band powers differ significantly across groups (both p = 0.001). Additionally, the theta/alpha ratio showed a strong negative correlation with MMSE (r = -0.49, p < 0.000002), with the  IAF showcasing a significant positive correlation (r = 0.37, p = 0.0004) with MMSE scores as well. The alpha PLV has a significant positive correlation (r = 0.27, p = 0.012), even after age correction, showcasing age to not be a confounding variable.Fruthermore,  SVM achieved 72.4% balanced accuracy for AD vs HC. Multiple EEG biomarkers consistently index cognitive severity in AD and FTD. This open MNE-Python pipeline offers a reproducible framework for EEG-based dementia biomarker research.


## Key Findings
1) Significant EEG slowing was observed in AD and FTD: Theta power differed significantly across groups (p = 0.001), with AD (0.112) and FTD (0.094) showing higher theta activity than healthy controls (HC = 0.060). Alpha power was significantly reduced (p = 0.001), with HC showing the highest alpha power (0.214) compared to AD (0.121) and FTD (0.126).
2) Topographic maps showed distinct spatial EEG abnormalities: HC subjects displayed low theta activity and strong posterior alpha rhythms over parietal-occipital regions, while AD showed pronounced frontal/frontocentral theta hotspots (Fz, Cz, F3, F4) and near-complete loss of posterior alpha activity. FTD showed intermediate patterns with partial preservation of posterior alpha.
3) Theta/alpha ratio strongly differentiated groups and tracked cognitive decline: The theta/alpha ratio increased progressively from HC (0.42 ± 0.38) to FTD (1.15 ± 0.95) and AD (1.97 ± 1.43), with AD showing a ratio ~4.7× higher than HC. The ratio showed a strong negative correlation with MMSE scores (r = −0.50, p < 0.000001), remaining significant after age correction (r = −0.49, p < 0.000002).
4) Individual Alpha Frequency (IAF) was significantly reduced in AD: IAF differed significantly across groups (p = 0.0001), with AD showing the lowest frequency (8.13 ± 1.52 Hz), followed by FTD (9.01 ± 1.34 Hz) and HC (9.56 ± 1.02 Hz). Lower IAF correlated with lower MMSE scores (r = 0.38, p = 0.0003), remaining significant after age correction (r = 0.37, p = 0.0004).
5)  Alpha-band functional connectivity (PLV) was reduced in dementia groups: Mean alpha PLV differed significantly (p = 0.0008), with HC showing the highest connectivity (0.698 ± 0.051), followed by AD (0.653 ± 0.056) and FTD (0.644 ± 0.060). PLV positively correlated with MMSE scores (r = 0.28, p = 0.007), remaining significant after age correction (r = 0.27, p = 0.012).
6) EEG biomarker relationships remained robust after controlling for age: Age was not significantly correlated with MMSE (r = 0.16, p = 0.14). All biomarker associations remained significant after age correction, including theta/alpha ratio (r = −0.49), IAF (r = 0.37), and alpha PLV (r = 0.27), confirming disease-related rather than age-related effects.
7) Machine learning classification achieved moderate success for AD detection: SVM classification of AD vs HC achieved a balanced accuracy of 72.4% ± 12.8%. Three-class random forest classification (AD vs FTD vs HC) achieved 47.4% ± 11.2% balanced accuracy. The confusion matrix showed correct classification rates of 64% for AD, 62% for HC, and only 17% for FTD, with most FTD cases misclassified as AD or HC.

## Dataset
OpenNeuro ds004504 — 88 subjects (36 AD, 23 FTD, 29 HC)
https://openneuro.org/datasets/ds004504

## Tools
MNE-Python, mne-connectivity, scikit-learn, pingouin, pandas, seaborn

## How to Run
1. Download the dataset from https://openneuro.org/datasets/ds004504
2. Install dependencies: 'pip install mne mne-connectivity pandas numpy matplotlib seaborn scipy scikit-learn pinguoun'
3. Open 'eeg_AD_FTD_analysis_pipeline.ipynb' in JupyterLab and run cells in order

## Files
- 'eeg_AD_FTD_analysis_pipeline.ipynb' — full analysis pipeline
- Figures — all output plots included in repository

## Author
Arnav Verma — BSc Psychology Honours, Christ (Deemed to be University), Delhi NCR
Independent Research, 2026
