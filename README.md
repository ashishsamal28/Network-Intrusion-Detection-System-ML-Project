# Network-Intrusion-Detection-System-ML-Project

A complete machine learning pipeline for detecting network intrusions using the **NSL-KDD dataset**. The project classifies network traffic into 5 categories — Normal, DoS, Probe, R2L, and U2R — by comparing 6 different ML classifiers.

---

## Dataset

**NSL-KDD** (Network Security Laboratory – Knowledge Discovery in Databases)

| Property | Details |
|---|---|
| Source | [NSL-KDD Dataset](https://www.unb.ca/cic/datasets/nsl.html) |
| Features | 41 network traffic features |
| Target Classes | Normal, DoS, Probe, R2L, U2R |
| Attack Types Mapped | 39 attack types → 5 categories |

---

## Models Compared

| Model | Description |
|---|---|
| Gradient Boosting | Ensemble boosting classifier |
| Random Forest | Ensemble bagging classifier |
| Decision Tree | Single tree classifier |
| K-Nearest Neighbors | Distance-based classifier |
| Logistic Regression | Linear probabilistic classifier |
| Naive Bayes | Probabilistic classifier |

---

## Pipeline

```
Raw NSL-KDD Data
      ↓
Data Loading & Cleaning
      ↓
Exploratory Data Analysis (EDA)
      ↓
Preprocessing (Label Encoding + Standard Scaling)
      ↓
Train/Test Split (70/30, stratified)
      ↓
Model Training & Evaluation
      ↓
Confusion Matrix + Feature Importance
      ↓
5-Fold Cross-Validation
      ↓
Results Saved to outputs/model_summary.csv
```

---

## Evaluation Metrics

- Accuracy
- F1-Score (weighted)
- Precision (weighted)
- Recall (weighted)
- Confusion Matrix
- 5-Fold Stratified Cross-Validation

---

## Project Structure

```
Network-Intrusion-Detection-System/
│
├── NSL_KDD_Intrusion_Detection.ipynb   # Main notebook
├── outputs/
│   └── model_summary.csv               # Model performance results
└── README.md
```

---

## Requirements

```bash
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/ashishsamal28/Network-Intrusion-Detection-System.git
   cd Network-Intrusion-Detection-System
   ```

2. **Download the NSL-KDD dataset**
   - Get `KDDTrain+.txt` from Kaggle
   - Place it in the project root or update the path in Cell 3

3. **Open the notebook**
   ```bash
   jupyter notebook/Collab  NSL_KDD_Intrusion_Detection.ipynb
   ```

4. **Run all cells** — Results will be saved to `outputs/model_summary.csv`

---

## Tech Stack

- **Language:** Python 3
- **Libraries:** NumPy, Pandas, Matplotlib, Seaborn, Scikit-learn
- **Environment:** Jupyter Notebook / Google Colab

---

## Attack Categories

| Category | Description | Example Attacks |
|---|---|---|
| **Normal** | Legitimate traffic | — |
| **DoS** | Denial of Service | neptune, smurf, teardrop |
| **Probe** | Port scanning / surveillance | nmap, portsweep, satan |
| **R2L** | Remote to Local | ftp_write, guess_passwd, imap |
| **U2R** | User to Root | buffer_overflow, rootkit, perl |

---

## Author

**Ashish Samal**  
[GitHub](https://github.com/ashishsamal28)
