# Dataset Description and File Structure

This repository contains the dataset and resources associated with the paper **"X-SPIDE: An eXplainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum"**.  
The project aims to detect Ponzi schemes deployed as smart contracts on the Ethereum blockchain, combining strong model performance with explainability through XAI techniques.

---

## Dataset Overview

The `dataset/` folder includes multiple cleaned and annotated datasets used for training, validation, and benchmarking of various machine learning classifiers:

| Filename                           | Description                                                              |
|------------------------------------|--------------------------------------------------------------------------|
| `Contract Adresses.csv`            | List of smart contract addresses analyzed.                               |
| `DS_deployed_bytecode.csv`         | Dataset including deployed bytecode and associated features.             |
| `DS_full_bytecode.csv`             | Dataset including both creation and deployed bytecode.                   |
| `address_without_byt.csv`          | Addresses for which bytecode could not be retrieved.                     |
| `bytecode_list.zip`                | Raw bytecode of smart contracts (compressed).                            |
| `depl_bytecode_list.zip`           | Deployed bytecode only (compressed).                                     |
| `bytecode_opcode_8k.csv`           | Dataset with disassembled opcode features (absolute/weighted frequency). |
| `duplicate_bytecode.csv`           | Duplicate bytecode entries identified in the dataset.                    |
| `duplicate_bytecode_join_addr.csv` | Duplicate bytecode linked to corresponding addresses.                    |

---

## Feature Types

- **Opcode-based features**: absolute and weighted frequencies of EVM instructions.
- **Account/transaction-based features**: e.g., balance, number of input/output transactions, investment ratios.
- **Label**: binary class (`1` for Ponzi, `0` for Non-Ponzi).

---

## Data Cleaning and Deduplication

- Contracts with missing, destroyed or unretrievable bytecode were excluded.
- Duplicated bytecodes (deployed under different addresses) were removed to avoid bias.
- Separate datasets were built for:
  - **Creation bytecode**
  - **Deployed bytecode**
  - **Full opcode + transaction features**

---

## Citation

If you use this dataset in your research, please cite:

```bibtex
@article{pennella2025xspide,
  title     = {X-SPIDE: An Explainable Machine Learning Pipeline for Detecting Smart Ponzi Contracts in Ethereum},
  author    = {Luca Pennella and Fabio Pinelli and Letterio Galletta},
  journal   = {IEEE Access},
  year      = {2025},
  note      = {To appear}
}
