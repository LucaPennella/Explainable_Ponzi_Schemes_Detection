## Notebooks Overview

The root of this repository contains a set of Jupyter notebooks used for feature engineering, model training, and explainability analysis. Below is a summary of their purpose:

- `1009_best_features_SHAP.ipynb`  
  Generates SHAP explanations for the selected feature subset using the final model.

- `2210_Model_Selection.ipynb`  
  Compares different classifiers using cross-validation and selects the best model based on performance metrics.

- `2510_best_features_model.ipynb`  
  Trains the final model using the best-performing feature set identified from previous experiments.

- `2710_best_features_SHAP.ipynb`  
  Performs a refined SHAP analysis using the selected model and top-ranked features.

- `Bytecode_list_Script.ipynb`  
  Parses and extracts raw bytecode for each contract address and stores it for later use.

- `Script_Account_Features.ipynb`  
  Computes account-level features such as transaction statistics, balance variations, and participation patterns.

- `Script_Code_Features.ipynb`  
  Extracts opcode-level features (absolute and weighted frequencies) from EVM bytecode.

---

> Each notebook is designed to be modular and independently executable.  
> Outputs are saved in the `dataset/` folder and used for training in downstream steps.
