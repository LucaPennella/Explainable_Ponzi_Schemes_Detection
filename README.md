# X-SPIDE: An eXplainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum

This repository contains the resources associated with the paper  
**"X-SPIDE:An eXplainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum"**, which proposes a transparent and reproducible approach for identifying Ponzi schemes deployed as smart contracts on the Ethereum blockchain.

The X-SPIDE pipeline combines high-performance classification with explainability tools such as SHAP values and Partial Dependence Plots (PDPs), enabling not only effective detection but also insight into decision-making.

---

## Repository Structure

- `dataset/`  
  Contains cleaned datasets, extracted bytecodes, contract addresses, and feature files.

- `data/`  
  Scripts and Jupyter notebooks for model training, evaluation, and XAI analysis.

- `miscellaneous/`  
  Includes lists of misclassified contracts, manual inspection notes, and queries used for validation.

- `old_scripts/`  
  Legacy scripts from early development stages (kept for reference and transparency).
---

## Dataset Highlights

- `DS_deployed_bytecode.csv`: Features extracted from deployed bytecode and transactions  
- `DS_full_bytecode.csv`: Combined dataset using creation + deployed code  
- `bytecode_opcode_8k.csv`: Opcode frequencies (absolute/weighted)  
- `Contract Adresses.csv`: All contracts included in the analysis  
- `duplicate_bytecode.csv`: Duplicated bytecode instances removed from training  
- `address_without_byt.csv`: Contracts whose bytecode was not retrievable  

> Datasets are cleaned, deduplicated, and formatted for supervised ML with binary classification (Ponzi vs Non-Ponzi).

---

## Features

- **Code-based features**: Frequency of opcodes from EVM bytecode (absolute and normalized)  
- **Account-based features**: ETH flow statistics, transaction timing, and initiator profit  
- **Label**: Ponzi (`1`) vs Non-Ponzi (`0`) classification  

---

## How to Cite

If you use X-SPIDE, its datasets, or the code in your research, please cite:

> Pennella et al.: *X-SPIDE: An eXplainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum*, IEEE Access.

BibTeX:
```bibtex
@article{pennella2025xspide,
  title     = {X-SPIDE: An eXplainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum},
  author    = {Luca Pennella and Fabio Pinelli and Letterio Galletta},
  journal   = {IEEE Access},
  year      = {2025},
  note      = {To appear}
}






