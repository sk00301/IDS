# 🛡️ Intrusion Detection System (IDS)

A machine learning-based **Network Intrusion Detection System** that evaluates and compares multiple deep learning and classical ML models for detecting malicious network activity.

---

## 📌 Overview

This project explores the use of various machine learning architectures to classify network traffic as normal or malicious. It covers the full pipeline from data preprocessing and balancing to model training, evaluation, and comparison.

The following models are implemented and benchmarked:

| Model | Notebook |
|---|---|
| Feedforward Neural Network (FNN) | `balanced_fnn.ipynb` |
| Long Short-Term Memory (LSTM) | `balanced_lstm.ipynb` |
| Convolutional Neural Network (CNN) | `new_cnn_f.ipynb` |
| Random Forest with PCA | `pca_rf.ipynb` |
| Classical ML Classifiers | `classification.ipynb` |

---

## 📁 Repository Structure

```
IDS/
├── Dataset preprocessing.ipynb       # Data cleaning, encoding, and balancing
├── classification.ipynb              # Classical ML classifiers (e.g. Decision Tree, SVM)
├── balanced_fnn.ipynb                # FNN model training on balanced dataset
├── balanced_fnn_model8x.h5           # Saved FNN model weights
├── balanced_lstm.ipynb               # LSTM model training on balanced dataset
├── balanced_lstm_model_opt.h5        # Saved LSTM model weights
├── new_cnn_f.ipynb                   # CNN model training
└── pca_rf.ipynb                      # PCA dimensionality reduction + Random Forest
```

---

## 🔄 Workflow

```
Raw Dataset
    │
    ▼
Dataset Preprocessing
(cleaning, encoding, SMOTE/balancing)
    │
    ▼
Model Training
(FNN / LSTM / CNN / RF+PCA / Classical ML)
    │
    ▼
Evaluation & Comparison
(accuracy, precision, recall, F1-score)
```

---

## 🧰 Tech Stack

- **Language:** Python 3
- **Environment:** Jupyter Notebook
- **Libraries:**
  - `pandas`, `numpy` — data handling
  - `scikit-learn` — classical ML, PCA, metrics
  - `tensorflow` / `keras` — FNN, LSTM, CNN
  - `matplotlib`, `seaborn` — visualization
  - `imbalanced-learn` — dataset balancing (SMOTE)

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/sk00301/IDS.git
cd IDS
```

### 2. Install dependencies

```bash
pip install numpy pandas scikit-learn tensorflow keras imbalanced-learn matplotlib seaborn
```

### 3. Run the notebooks in order

1. `Dataset preprocessing.ipynb` — preprocess and balance the dataset
2. Any model notebook (`balanced_fnn.ipynb`, `balanced_lstm.ipynb`, `new_cnn_f.ipynb`, `pca_rf.ipynb`, `classification.ipynb`)

> ⚠️ Run the preprocessing notebook first to generate the cleaned dataset used by the model notebooks.

---

## 📊 Models & Highlights

### Feedforward Neural Network (FNN)
A fully connected neural network trained on the balanced dataset. Saved weights available as `balanced_fnn_model8x.h5`.

### LSTM
A recurrent model capturing sequential patterns in network traffic. Optimized weights saved as `balanced_lstm_model_opt.h5`.

### CNN
A convolutional architecture applied to feature vectors of network flows to detect spatial patterns.

### PCA + Random Forest
Principal Component Analysis is applied for dimensionality reduction before training a Random Forest classifier, improving efficiency and reducing noise.

### Classical ML Classifiers
Baseline models including Decision Trees, Support Vector Machines, and others for performance comparison.

---

## 📄 License

This project is open source. Feel free to use and build upon it.

---

## 🙋 Author

**[sk00301](https://github.com/sk00301)**
