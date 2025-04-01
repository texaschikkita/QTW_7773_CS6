# QTW_7773_CS6
smu 7333 Dr. R Slater Case Study 6 - Jessica McPhaul


------------------------------
DOCX - has graphs and appendix.
pdf- doesnt have appendix
notebook is asis from colab
python is as is fro colab
---------------------------


# Particle Detection Using Dense Neural Networks

This project demonstrates a binary classification task using a dense neural network to predict the detection of a new particle based on a large scientific dataset.

## 🔬 Project Overview

- **Objective**: Predict the presence of a new particle (`1 = detected`, `0 = not detected`)
- **Dataset Size**: 7 million+ examples, 28 features
- **Challenge**: Efficient model training with high accuracy using cross-validation, not train/test splits

## 🧠 Model Details

- **Type**: Dense Neural Network
- **Architecture**:
  - 5 hidden layers: [500, 400, 300, 200, 100] units
  - Batch Normalization + ReLU activation
  - Final sigmoid output (`float32`)
- **Optimizer**: Adam
- **Loss Function**: Binary Crossentropy
- **Precision Policy**: Mixed precision (`float16`) on A100 GPU

## 🧪 Cross-Validation Results (5-Fold)

| Fold | Accuracy | Precision | Recall | AUC  |
|------|----------|-----------|--------|------|
| 1    | 0.8841   | 0.8737    | 0.8980 | 0.8841 |
| 2    | 0.8835   | 0.8615    | 0.9140 | 0.8835 |
| 3    | 0.8836   | 0.8762    | 0.8935 | 0.8836 |
| 4    | 0.8841   | 0.8698    | 0.9036 | 0.8841 |
| 5    | 0.8834   | 0.8630    | 0.9116 | 0.8834 |

**Averaged Results**:
- Accuracy: `0.8837`
- Precision: `0.8688`
- Recall: `0.9041`
- AUC-ROC: `0.8837`

## 📁 Files Included

- `texaschikkita-particle-detection.ipynb`: Colab notebook with full training + evaluation pipeline
- `particle_case_study.md`: Markdown case study write-up
- `particle_case_study.pdf`: Printable PDF version of the report

## 🛠️ Requirements

- Python 3.11+
- TensorFlow 2.x
- NumPy, Pandas, scikit-learn, matplotlib

## 🧾 Notes

- No train/test split was used — full compliance with cross-validation requirements
- All model decisions, metrics, and convergence points are documented
- No vague performance claims — all metrics are numerically supported

## 📫 Contact

For questions or clarifications, reach out to [texaschikkita](mailto:texaschikkita@smu.edu)

