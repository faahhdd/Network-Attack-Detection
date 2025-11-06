# Network Attack Detection using Machine Learning  

This project focuses on detecting **network attacks** using the **UNSW-NB15 dataset**.  
It applies a full data science pipeline — from **EDA and preprocessing** to **feature engineering**, **scaling**, and **model training** — to classify traffic as **Normal (0)** or **Attack (1)**.

---

## 📊 Dataset Overview
The **UNSW-NB15** dataset contains various network flow features including:
- Basic connection attributes (e.g., `proto`, `service`, `state`)
- Packet and byte counts (`spkts`, `dpkts`, `sbytes`, `dbytes`)
- Time-based and statistical metrics (`dur`, `rate`, `sload`, `dload`)

> 📁 Files used:
> - `UNSW_NB15_training-set.csv`
> - `UNSW_NB15_testing-set.csv`

---

## ⚙️ Project Steps

### **1. Data Loading & Exploration**
- Loaded both training and testing datasets.
- Checked structure, missing values, and label distribution.
- Visualized key relationships using histograms, boxplots, and heatmaps.

### **2. Data Cleaning & Transformation**
- Applied **log transform** on skewed numerical features to handle outliers.
- Encoded categorical columns (`proto`, `service`, `state`) using `CategoricalDtype`.

### **3. Feature Engineering**
Created meaningful network-related features such as:
- `pkt_total`, `byte_total`  
- `pkt_ratio_sd`, `byte_ratio_sd`  
- `pkts_per_sec`, `bytes_per_sec`  
- `ttl_diff`

### **4. Scaling**
Standardized numerical features using `StandardScaler`.

### **5. Model Training**
Trained and compared two ML models:
- **Logistic Regression**
- **Random Forest Classifier**

---

## 🧪 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|:------|:----------|:-----------|:--------|:----------|:----------|
| Logistic Regression | 0.877 | 0.967 | 0.849 | 0.904 | 0.970 |
| Random Forest | 0.902 | 0.988 | 0.867 | 0.924 | 0.982 |

> 🏆 **Random Forest** achieved the best balance between accuracy and recall.

---

## 🖼️ Visuals
The notebook includes:
- **EDA Visualizations** (distributions, correlations)
- **Before/After Log Transform comparisons**
- **Model comparison metrics**




---

## 📂 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/<your-username>/Network-Attack-Detection.git
   cd Network-Attack-Detection
