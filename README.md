# CS598_DL4Health
This is the project script repository for UIUC course CS598 Deap Learning for Health Data-Reproducing the Paper "Learning Latent Space Representations to Predict Patient Outcomes: Model Development and Validation. The original github repository is https://github.com/subendhu19/CLOUT

## Datasets preprocessing
After communication with the author of the paper, structured datasets from MIMIC-III (version 1.4) were preprocessed using the script Data_processing_modified_from_source_code.ipynb` modified from the author provided processing script `process_mimic.py`. 

## Modeling Scripts
Scripts developed during the report drafting phase of the project were all put in the folder "Old_codes". 
Scripts updated and developed for the final report include the follows:
    
### Baseline Models 
1. Logistic Regression + concatednated features: `Logistic Regression Modified from Source Code.ipynb` 
2. RETAIN: `Baseline_RETAIN_ICD9.ipynb` (Using only Diagnosis ICD9 codes); `Baseline_RETAIN_All_Features.ipynb` (Using concatenated ICD+Med+Lab).
3. CLOUT with Auto-Encoder (AE): `AE_modified_from_source_code.ipynb` (Generating hidden states that are used to weight the concatenated features for CLOUT), `CLOUT_and_AE_modifed_from_source_code.ipynb`. 
4. LSTM: `LSTM_ICD9.ipynb`

### CLOUT Models (with correlated latent space embeddings)
1. CAE (Correlated Auto-Encoder that generate the latent space embeddings): `CAE_modifed_from_source_code.ipynb`
2. CLOUT + concatenated features: `CLOUT_Concat_modifed_from_surce_code.ipynb` 
3. CLOUT + latent space only: 
4. CLOUT + latent space with concatenated features" `CLOUT_Concat_Latent_modified_from_source_code.ipynb`
    
