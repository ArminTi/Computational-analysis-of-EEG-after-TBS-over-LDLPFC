# Computational analysis of longitudinal electroencephalograms after theta burst stimulation over left DLPFC using hierarchical dynamic causal modelling.

## Steps:

### Data Preprocessing
1. Specifying rest eeg trials (remove TEP epochs)
2. BandPass (1 - 50) and downsample to 258 (see tbs_rseeg_preprocess)
3. 2 second epoch for each trial (trial 1: Res Pre 1, trial 2: Rest pre 2, trial 3: Rest post 1, trial 4: Rest post 2, trial 5: Rest post 3)
4. Auto rejection of badepochs (see tbs_rseeg_trialrejection function)
5. Manual rejection of trials and epochs (see tbs_rseeg_cleaning)
6. ICA using runica
7. inspection of ICA (Auto labeling with manual rejection)
8. Rerefrence to average
9. Final inspection
10. change fieldtrip to spm (save spm object)

### Data Analysis

1. Loading data to SPM using fieldtrip conversion
2. Source localization: using individual MRI and real-time chanel locs
3. Model specification: spectral DCM, Conductance-based Canonical Microcircuit Model (cmm-NMDA)
4. Model estimation
5. Explained Variance
6. First Level Parametric empirical bayes
7. Peb of Peb
    
-------------------------------------------------------------------------------------------------
IDS team 23:
Supervisor: Prof. Ali Motie Nasrabadi
Mentor: Armin Toghi
Members: Ghazale ghaffaripour, Hamed moghtaderi, Babak Aliyari

