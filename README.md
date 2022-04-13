# CS598_DL4Health
This is the project script repository for UIUC course CS598 Deap Learning for Health Data-Reproducing the Paper "Learning Latent Space Representations to Predict Patient Outcomes: Model Development and Validation. The original github repository is https://github.com/subendhu19/CLOUT

## Datasets
The original paper did not mention which version of MIMIC III datasets and which particular sets were used to build up the input dataset "p-MIMIC". Based on the Appendix 1, the following datasets from MIMIC III 1.4 were used to reproduce this paper:
1. ADMISSION.csv 
    This dataset was used to extract "SUBJECT_ID" of patients that had at least two encounters/admissions, and to verify the demographic statistics performed in the paper (Appendix 1).
    
2. DIAGNOSES.csv and D_ICD_DIAGNOSES.csv
    These datasets were used to buld the ICD code feature.
    
3. PRISCRIPTIONS.csv
    This dataset was used to build the medication feature.
    
4. LABEVENTS.csv and D_LABITEMS.csv
    This dataset was used to build the laboratory feature.
