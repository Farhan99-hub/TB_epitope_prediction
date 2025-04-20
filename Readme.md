# 🧬 Epitope Prediction using Machine Learning

This repository contains a machine learning pipeline to predict **B-cell** and **T-cell epitopes** from peptide sequences, focused on _Mycobacterium tuberculosis_. The project leverages features derived from biochemical properties, amino acid composition, and embeddings from ESM2 (Evolutionary Scale Modeling).

---

## 📂 Data Collection

- **Source**: [IEDB - Immune Epitope Database](https://www.iedb.org/)
- **B-cell Epitope Dataset**: Downloaded from linear B-cell assay section.
- **T-cell Epitope Dataset**: Collected from MHC ligand assay results for _Mycobacterium tuberculosis_.
- **Filtering & Preprocessing**:
  - Removed non-human and non-experimental records.
  - Cleaned and deduplicated based on epitope sequences.
  - Labelled data as `1` (positive epitope) and `0` (negative/non-epitope).

---

## 🛠️ Features Used

- Peptide biochemical properties (e.g., length, molecular weight, charge, pI, etc.)
- Amino acid frequency and sequence-level descriptors.

---

## 🤖 Models

- **Random Forest Classifier**
  - Used for both B-cell and T-cell predictions.
  - Trained with class balancing via SMOTE.
- Performance (on test set):
  - **T-cell Accuracy**: ~74%
  - **B-cell Accuracy**: ~76%

---

## 📊 Evaluation Metrics

Each model was evaluated using:

- **Accuracy**
- **Precision**
- **Recall**
- **F1-score**
- **Confusion Matrix**
- **ROC-AUC curve**

---

## 🔍 Results Summary

| Model      | Precision | Recall | F1-score | Accuracy |
|------------|-----------|--------|----------|----------|
| T-cell     | 0.74      | 0.74   | 0.74     | 0.74     |
| B-cell     | 0.76      | 0.74   | 0.75     | 0.76     |

---

## 🚀 Getting Started
https://github.com/Farhan99-hub/TB_epitope_prediction.git
To set up this project locally:

```bash
# Clone the repository
git clone https://github.com/yourusername/epitope-prediction.git
pip install -r requirements.txt
