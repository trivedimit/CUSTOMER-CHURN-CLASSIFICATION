# Customer Churn Classification Project

## 📌 Project Overview
This project focuses on **predicting customer churn** using various machine learning techniques.  
The main challenge in churn prediction is dealing with **imbalanced data**, where the number of customers who churn is significantly smaller than those who don’t.  

To address this, I explored multiple **resampling techniques** and compared the performance of different models (**Logistic Regression, KNN, Decision Tree, and SVM**).  

The entire workflow—from **data exploration** to **model evaluation**—was performed in Jupyter Notebook, and the results were compiled into a structured PDF report.

---
```
## 📂 Repository Structure
├── dataset/ # Raw dataset
├── notebook/ # Jupyter Notebook with full workflow
├── pdf/ # PDF version of project report
├── requirements.txt # Required dependencies
└── README.md # Project documentation
```
---

## 🔑 Project Steps

### 1. Initial Setup & Data Overview
- Loaded the dataset and essential Python libraries.  
- Performed initial inspection of data shape, types, and distributions.  

### 2. Univariate Analysis
- Explored numerical feature distributions using **histograms**.  
- Used **boxplots** to compare feature spread across churn (1) vs non-churn (0).  

### 3. Bivariate Analysis
- Conducted **statistical tests**:  
  - **One-Way ANOVA** for numerical features.  
  - **Chi-Square test** for categorical features.  
- Performed **correlation analysis** with a correlation matrix.  

### 4. Data Preprocessing
- ✅ No missing values found.  
- **Outlier handling** using **Local Outlier Factor (LOF)**.  
- **Categorical encoding** with **One-Hot Encoding**.  
- **Feature scaling** using **StandardScaler**.  

### 5. Machine Learning Modeling
- Performed **train-test split**.  
- Started with **Logistic Regression (LR)** as a baseline model.  

#### Handling Class Imbalance
Tested several techniques to improve model performance on imbalanced data:
1. **Upsampling minority class**  
2. **Downsampling majority class**  
3. **Cluster Centroids**  
4. **SMOTE**  
5. **ADASYN**  
6. **Tomek Links**  
7. **NearMiss (1, 2, 3)**  
8. **Hybrid approaches** (SMOTE + Tomek Links + NearMiss)  

- Selected the **best-performing resampling method** → **Tomek Links**.  

#### Training Other Models
- Trained **KNN, Decision Tree, and SVM** on:  
  - Original dataset.  
  - Best resampled dataset (Tomek Links).  

- Compared performances across models and datasets.

---

## ⚙️ Tech Stack
- **Programming Language:** Python  
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, Imbalanced-learn  

---

## 📊 Results
- Logistic Regression, KNN, Decision Tree, and SVM were evaluated.  
- **Tomek Links resampling** provided the best balance between **accuracy, precision, recall, and F1-score**.  
- Demonstrated the importance of **resampling techniques** in classification tasks with imbalanced datasets.  

---
## Install dependencies:
- pip install -r requirements.txt

## Open the notebook:
- jupyter notebook notebook/churn_classification.ipynb

---
