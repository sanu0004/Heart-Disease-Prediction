# ❤️ Heart Disease Prediction using Machine Learning

A binary classification project that predicts whether a patient has heart disease based on key medical attributes, using **Logistic Regression**.

## 📌 Overview

Heart disease is one of the leading causes of death worldwide, and early prediction can help doctors act faster. This project uses a supervised machine learning model trained on patient health data (age, blood pressure, cholesterol, etc.) to predict whether a person is likely to have heart disease (`1`) or not (`0`).

## 📂 Dataset

- **File:** `heart_disease_data.csv`
- **Rows:** 303 patient records
- **Columns:** 14 (13 features + 1 target)
- **Source:** Based on the widely-used UCI / Cleveland Heart Disease dataset
- **Target distribution:** 165 patients with heart disease, 138 without (fairly balanced)

### Features

| Feature | Description |
|---|---|
| `age` | Age of the patient |
| `sex` | 1 = male, 0 = female |
| `cp` | Chest pain type (0–3) |
| `trestbps` | Resting blood pressure (mm Hg) |
| `chol` | Serum cholesterol (mg/dl) |
| `fbs` | Fasting blood sugar > 120 mg/dl (1 = true, 0 = false) |
| `restecg` | Resting electrocardiographic results |
| `thalach` | Maximum heart rate achieved |
| `exang` | Exercise-induced angina (1 = yes, 0 = no) |
| `oldpeak` | ST depression induced by exercise relative to rest |
| `slope` | Slope of the peak exercise ST segment |
| `ca` | Number of major vessels colored by fluoroscopy (0–3) |
| `thal` | Thalassemia (0 = normal, 1 = fixed defect, 2 = reversible defect) |
| `target` | 1 = has heart disease, 0 = healthy |

## 🛠️ Tech Stack

- **Python 3**
- **NumPy** – numerical operations
- **Pandas** – data loading and manipulation
- **scikit-learn** – model training, train-test split, evaluation

## ⚙️ Project Workflow

1. **Data Collection** – Load the CSV file into a Pandas DataFrame.
2. **Data Exploration** – Check shape, missing values, data types, and statistical summary.
3. **Preprocessing** – Split data into features (`X`) and target (`Y`).
4. **Train-Test Split** – 80% training / 20% testing, using `stratify=Y` to preserve class balance.
5. **Model Training** – Train a Logistic Regression classifier on the training set.
6. **Evaluation** – Measure accuracy on both training and test sets.
7. **Prediction System** – Accept new patient data and output a prediction.

## 📊 Results

| Metric | Score |
|---|---|
| Training Accuracy | 85.12% |
| Test Accuracy | 81.97% |

The close gap between training and test accuracy suggests the model generalizes reasonably well without major overfitting.

## 🚀 How to Run

1. Clone this repository / download the notebook.
2. Install the dependencies:
   ```bash
   pip install numpy pandas scikit-learn
   ```
3. Make sure `heart_disease_data.csv` is in the same directory as the notebook.
4. Open and run `Heart_disease_prediction.ipynb` in Jupyter Notebook / JupyterLab / Google Colab.

## 🔮 Example Prediction

```python
input_data = (37, 1, 2, 130, 250, 0, 1, 187, 0, 3.5, 0, 0, 2)
# Output: The person has heart disease
```

## 🔧 Future Improvements

- Apply feature scaling (e.g., `StandardScaler`) since Logistic Regression is sensitive to feature magnitude
- Compare performance against other algorithms (SVM, KNN, Random Forest, XGBoost)
- Use additional evaluation metrics: precision, recall, F1-score, confusion matrix, ROC-AUC
- Apply cross-validation for a more reliable performance estimate
- Perform hyperparameter tuning (e.g., `GridSearchCV`)
- Deploy the model as a web app using Flask/Streamlit for interactive predictions

## ⚠️ Disclaimer

This project is for **educational purposes only**. It is trained on a small academic dataset and is **not validated for real clinical or diagnostic use**. Always consult a certified medical professional for actual health decisions.

## 👤 Author

*Add your name, GitHub, and LinkedIn here.*
