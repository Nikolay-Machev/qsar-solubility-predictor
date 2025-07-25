# qsar-solubility-predictor
Predicts molecular solubility from SMILES using RDKit descriptors and an XGBoost model.
# 🧪 QSAR Solubility Predictor using RDKit & XGBoost

This project predicts the aqueous solubility of molecules from SMILES strings using a machine learning model trained on 200+ molecular descriptors generated with RDKit.

## 📊 Model Performance

- **Model**: XGBoost Regressor
- **Features**: 208 molecular descriptors
- **Dataset**: ESOL (1128 molecules)
- **Test R² Score**: 0.899
- **Cross-Validated R² (5-fold)**: 0.912
- **RMSE**: 0.691

## 📁 Files Included

- `qsar_model.ipynb` — Jupyter notebook with full training + evaluation pipeline
- `qsar_model.pkl` — Saved XGBoost model
- `descriptor_names.pkl` — List of RDKit descriptor names
- `requirements.txt` — Python dependencies
- `.gitignore` — Excludes Jupyter checkpoints and cache files
- `README.md` — Project overview

## 🧬 Dataset

- **Name**: ESOL (Delaney) — solubility in water
- [Download from DeepChem](https://deepchemdata.s3-us-west-1.amazonaws.com/datasets/delaney-processed.csv)

## 🚀 How to Run Locally

```bash
git clone https://github.com/Nikolay-Machev/qsar-solubility-predictor.git
cd qsar-solubility-predictor
pip install -r requirements.txt
jupyter notebook qsar_model.ipynb
