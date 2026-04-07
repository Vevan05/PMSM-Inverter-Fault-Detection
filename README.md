# ⚡ PMSM Inverter Fault Detection using Random Forest

## 📌 Overview
This project focuses on **fault detection and classification** in an inverter-driven Permanent Magnet Synchronous Motor (PMSM) system using machine learning.

The model uses **multi-sensor data** to identify different types of faults such as:
- Open-circuit faults
- Short-circuit faults
- Overheating conditions


## 📊 Dataset Description

The dataset consists of time-series sensor readings collected from an inverter-driven PMSM system. (https://github.com/bachaabdelkabir/PMSM-inverter-fault-diagnosis/blob/main/dataset%20CSV.csv)

### 🔢 Features (Input Variables)
| Feature | Description |
|--------|-------------|
| Ia | Phase A current |
| Ib | Phase B current |
| VDC | DC bus voltage |
| IDC | DC bus current |
| T1 | Temperature of half-bridge 1 |
| T2 | Temperature of half-bridge 2 |
| T3 | Temperature of half-bridge 3 |
| VD | Driver voltage |

### 🎯 Target Variable
| Label | Description |
|------|-------------|
| F0 | Normal operation |
| F1–F2 | Open-circuit faults |
| F3–F5 | Short-circuit faults |
| F6–F8 | Overheating conditions |

## ⚙️ Methodology

1. Data preprocessing and feature selection
2. Train-test split (80-20) with stratification
3. Model training using Random Forest Classifier
4. Performance evaluation using:
   - Accuracy
   - Confusion Matrix
   - Classification Report
   - Cross-validation
   - Balanced Accuracy
5. Overfitting validation using shuffled labels

## 🌲 Model Details

- Algorithm: **Random Forest Classifier**
- Number of Trees: 200
- Max Depth: 12
- Min Samples Split: 5
- Min Samples Leaf: 2
- Class Weight: Balanced

## 📈 Results

- **Train Accuracy:** ~99%
- **Test Accuracy:** ~99%
- **Balanced Accuracy:** ~99%
- **Cross-validation Accuracy:** ~97-98%

### 🔍 Key Observations
- The model performs well across all fault classes despite class imbalance.
- Confusion matrix shows minimal misclassification.
- Strong generalization capability.

## 🧪 Overfitting Check

To verify model robustness, labels were randomly shuffled:

- Accuracy dropped to ~11% (random chance for 9 classes)

✅ This confirms:
- No data leakage  
- Model learns meaningful patterns  
- Predictions are reliable  

## 📊 Visualizations

- Confusion Matrix
- Classification Report
- Cross-validation scores