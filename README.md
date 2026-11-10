# 🩺 Diabetes Prediction Using Machine Learning

## 📌 Project Overview

This project focuses on predicting whether a person is diabetic or non-diabetic using Machine Learning techniques. It uses the **Support Vector Machine (SVM)** algorithm with a Linear Kernel to classify individuals based on medical diagnostic information.

The model is trained on the Pima Indians Diabetes Dataset and uses various health-related attributes to predict the likelihood of diabetes.

## 🎯 Objectives

- Analyze and understand the diabetes dataset.
- Perform data preprocessing and standardization.
- Build a classification model using Support Vector Machine (SVM).
- Evaluate model performance using training and testing accuracy.
- Predict diabetes outcomes for new input data.

## 🛠️ Technologies & Libraries Used

- **Programming Language:** Python
- **Data Analysis:** Pandas, NumPy
- **Data Visualization:** Matplotlib, Seaborn
- **Machine Learning:** Scikit-learn
- **Development Environment:** Jupyter Notebook / Google Colab

## 📂 Dataset Information

**Dataset:** Pima Indians Diabetes Dataset

The dataset contains 768 records and 9 columns, including 8 independent features and 1 target variable.

### Features

| Feature | Description |
|---|---|
| Pregnancies | Number of pregnancies |
| Glucose | Plasma glucose concentration |
| BloodPressure | Diastolic blood pressure |
| SkinThickness | Triceps skinfold thickness |
| Insulin | 2-hour serum insulin |
| BMI | Body Mass Index |
| DiabetesPedigreeFunction | Diabetes pedigree function |
| Age | Age of the individual |
| Outcome | Diabetes prediction (0 or 1) |

**Target Variable:**
- `0` – Non-Diabetic
- `1` – Diabetic

## 🔍 Project Workflow

### 1. Data Collection and Analysis
- Loaded the dataset using Pandas.
- Examined the first five records using `head()`.
- Checked dataset dimensions using `shape`.
- Analyzed statistical information using `describe()`.
- Checked the distribution of diabetic and non-diabetic individuals using `value_counts()`.
- Compared average feature values using `groupby()`.

### 2. Data Preprocessing
- Separated independent features (X) and the target variable (Y).
- Applied StandardScaler to standardize the input features.
- Transformed the dataset into standardized values.

### 3. Train-Test Split

Split the dataset into training and testing sets.

- Training Data: 80%
- Testing Data: 20%
- Stratified Sampling: Maintains the target class distribution.
- Random State: 2

### 4. Model Building

Implemented the Support Vector Machine (SVM) classifier using Scikit-learn.

**Algorithm:** Support Vector Machine (SVM)

**Kernel:** Linear

```python
from sklearn import svm

classifier = svm.SVC(kernel='linear')

classifier.fit(X_train, Y_train)
```

### 5. Model Evaluation

Evaluated the model using Accuracy Score.

**Training Accuracy:** 78.66%

**Testing Accuracy:** 77.27%

The model achieved approximately 77% accuracy on the unseen test dataset.

### 6. Prediction on New Input Data

The trained model accepts new medical input values and predicts whether an individual is diabetic or non-diabetic.

Prediction process:
1. Collect medical input values.
2. Convert input into a NumPy array.
3. Reshape the input into the required format.
4. Apply the same StandardScaler transformation.
5. Pass the standardized input to the trained SVM model.
6. Display the prediction result.

## 📊 Model Performance

| Evaluation Metric | Result |
|---|---:|
| Training Accuracy | 78.66% |
| Testing Accuracy | 77.27% |

## 🚀 How to Run the Project

**Step 1: Clone the repository**

```bash
git clone https://github.com/your-username/Diabetes-Prediction.git
```

**Step 2: Navigate to the project directory**

```bash
cd Diabetes-Prediction
```

**Step 3: Install required libraries**

```bash
pip install numpy pandas scikit-learn matplotlib seaborn jupyter
```

**Step 4: Run the Jupyter Notebook**

```bash
jupyter notebook
```

**Step 5:** Open the notebook and execute the cells.

## 📁 Project Structure

```text
Diabetes-Prediction/
│
├── diabetes.csv
├── diabetes_prediction.ipynb
├── README.md
└── requirements.txt
```

## 🔮 Future Improvements

- Handle missing or zero-valued medical measurements appropriately.
- Perform feature selection and hyperparameter tuning.
- Compare SVM with Random Forest, Logistic Regression, and other classification algorithms.
- Evaluate using Precision, Recall, F1-Score, and Confusion Matrix.
- Develop an interactive web application using Streamlit.
- Deploy the trained model for real-time predictions.

## ⚠️ Disclaimer

This project is developed for educational and machine learning purposes. Predictions are not a substitute for professional medical diagnosis or advice.

## 👨‍💻 Author

**Sriram Pranay Kumar**

- GitHub: https://github.com/your-username
- LinkedIn: https://www.linkedin.com/in/your-profile/
