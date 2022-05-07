# CS598_DL4Health
This is the project script repository for UIUC course CS598 Deap Learning for Health Data-Reproducing the Paper "Learning Latent Space Representations to Predict Patient Outcomes: Model Development and Validation. The original github repository is https://github.com/subendhu19/CLOUT

## Datasets preprocessing
After communication with the author of the paper, structured datasets from MIMIC-III (version 1.4) were preprocessed using the script Data_processing_modified_from_source_code.ipynb` modified from the author provided processing script `process_mimic.py`. 

## Modeling Scripts
Scripts developed during the report drafting phase of the project were all put in the folder "Old_codes". 
Scripts updated and developed for the final report include the follows. All scripts for models include sections of data loading, model construction, model training and prediction. Some models also incude the risk factor interpretation section.
    
### Baseline Models 
1. Logistic Regression + concatednated features: `Logistic Regression Modified from Source Code.ipynb` 
2. RETAIN: `Baseline_RETAIN_ICD9.ipynb` (Using only Diagnosis ICD9 codes); `Baseline_RETAIN_All_Features.ipynb` (Using concatenated ICD+Med+Lab).
3. CLOUT with Auto-Encoder (AE): `AE_modified_from_source_code.ipynb` (Generating hidden states that are used to weight the concatenated features for CLOUT), `CLOUT_and_AE_modifed_from_source_code.ipynb`. 
4. LSTM: `LSTM_ICD9.ipynb`

### CLOUT Models (with different encounter vector structures)
Auto-Encoder (AE) and Correlational Auto-Encoder (CAE) were constructed by first and second scripts listed below. The embedding weights learned from AE or CAE were used to build the representations of clinical features that fed the LSTM model as encounter vector alone or concatenated with embeddings of clinical features.  
1. AE (Auto-Encoder that generates the AE embeddings): `AE_modified_from_source_code.ipynb`
2. CAE (Correlated Auto-Encoder that generates the latent space embeddings): `CAE_modifed_from_source_code.ipynb`
3. CLOUT + AE only: `CLOUT_and_AE_modifed_from_source_code.ipynb`
3. CLOUT + AE with concatenated features: `CLOUT_and_AE_concatenation_modified_from_source_code.ipynb`
4. CLOUT + concatenated features: `CLOUT_Concat_modifed_from_surce_code.ipynb` 
5. CLOUT + latent space only: `CLOUT_and_Latent_Space_only_modified_from_source_code.ipynb`
6. CLOUT + latent space with concatenated features" `CLOUT_Concat_Latent_modified_from_source_code.ipynb`. This is the final model. 
    
