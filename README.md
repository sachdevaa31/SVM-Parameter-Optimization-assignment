# 🔍 SVM Parameter Optimization using UCI Dataset

## 📘 Assignment Objective

This project focuses on optimizing the parameters of an SVM classifier using a multi-class dataset from the UCI Machine Learning Repository. The goal is to:

- Divide the dataset into 70% training and 30% testing sets.
- Create 10 different random samples.
- Perform parameter optimization for each sample across 100 iterations.
- Identify the best parameters and report accuracy.
- Plot the convergence graph for the best-performing sample.
- Present all results with brief analytics on GitHub.

---

## 📊 Dataset Used

- **Name**: Dry Bean Dataset  
- **Source**: [UCI Repository](https://archive.ics.uci.edu/ml/datasets/Dry+Bean+Dataset)  
- **Classes**: 7 types of dry beans  
- **Rows**: ~13,611  
- **Features**: 16 numeric shape-related attributes  
- **Target**: `Class` (Categorical, label encoded)

---

## 🧪 Methodology

1. **Preprocessing**:
   - Converted `.xlsx` dataset to `.csv`
   - Performed label encoding on target column
   - Standardized features using `StandardScaler`

2. **SVM Classifier**:
   - Used `NuSVC` from `sklearn.svm`
   - Tuned Parameters:
     - `kernel`: `'linear'`, `'rbf'`, `'poly'`, `'sigmoid'`
     - `nu`: random values from 0.01 to 0.3
   - Fixed `gamma='scale'` and `shrinking=False`

3. **Optimization**:
   - 10 random train-test splits (samples)
   - 100 iterations per sample
   - Stored accuracy and corresponding SVM params

4. **Evaluation**:
   - Recorded best accuracy & parameters for each sample
   - Plotted convergence of best-performing sample

---

## 📈 Results

### 📌 Comparative Performance Table

| Sample # | Best Accuracy (%) | Best SVM Parameters (Kernel, Nu) |
|----------|-------------------|----------------------------------|
| S1       | 91.23             | rbf, nu=0.09                     |
| S2       | 89.75             | linear, nu=0.12                  |
| S3       | 92.18             | poly, nu=0.06                    |
| S4       | 90.55             | rbf, nu=0.10                     |
| S5       | 88.90             | sigmoid, nu=0.11                 |
| S6       | 90.84             | rbf, nu=0.05                     |
| S7       | 93.11             | poly, nu=0.07                    |
| S8       | 89.23             | linear, nu=0.13                  |
| S9       | 91.67             | rbf, nu=0.08                     |
| S10      | 90.01             | sigmoid, nu=0.14                 |

🏆 **Best Sample**: **S7**  
🎯 **Highest Accuracy**: **93.11%**  
🔧 **Best Parameters**: `poly` kernel, `nu = 0.07`

---

## 📉 Convergence Graph

The following graph shows the improvement in accuracy over 100 iterations for the **best sample (S7)**:

![Convergence Graph](<img width="795" alt="graph" src="https://github.com/user-attachments/assets/4236e2f8-6e45-4465-83c2-d6712d03c52f" />
)


---


