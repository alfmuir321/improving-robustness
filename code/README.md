# README


## Information

We provide almost everything needed to run the notebooks here, including the datasets. We do not include the model weights, these are hosted on Google Drive and can be downloaded here: https://drive.google.com/drive/folders/1XCBhyj8Ce83Es8TC-Eu64LorFu740DeF?usp=sharing

Each weights folder contains the weights for a training stage. The folder of weights must be downloaded, and the file path to the folder provided in the code. These are approximately 1.7GB each.

Each notebook contains code for a distinct task in this project. They can largely be run 'as is', so long as the weights have been downloaded, the relevant packages installed, and the relevant file paths provided. 

A GPU is required to run all notebooks except preprocessing.ipynb. A powerful GPU is recommended due to the size of the model (we used an Nvidia A100). 


## Code Description

**preprocessing.ipynb**: code used to generate the training and evaluation sets. File path to the raw data (train.jsonl, valid.jsonl) must be provided

**train_ts1.ipynb**: code used to train the model in TS1

**train_ts2.ipynb**: code used to train the models in TS2. A file path to the TS1 model weights needs to be provided. The first 3 cells (IMPORTS, LOAD DATA, LOAD MODEL) need to be run, then any one of the TS2.X cells can be run. If one TS2.X cell has run, a different one can be run by re-running the LOAD MODEL cell, as this resets the model

**eval_performance.ipynb**: code used to evaluate the accuracies of the models on the evaluation sets V. File path to the desired model, and the evaluation sets, must be provided.

**eval_consistency.ipynb**: code used to evaluate the answer and representational consistency of the models. File paths to model and V_standard must be provided. 

**generate_pca_plots.ipynb**: code used to generate the PCA plots. File paths to model, V_standard, V_paraphrase, and T_standard or T_paraphrase must be provided.

**generate_dt_plots.ipynb**: code used to generate the decoder trajectory plots. File paths to ALL of the models (TS0, TS1, TS2.1, TS2.2, TS2.3, TS2.4), and V_standard must be provided. TS2.4.1 and TS2.4.2 can be evaluated in place of TS2.4, only needing to change the file path to the model weights.
