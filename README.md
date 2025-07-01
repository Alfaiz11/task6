# Task 6
# K-Nearest Neighbors (KNN) Classification - Airline Passenger Satisfaction

This project implements a **K-Nearest Neighbors (KNN)** classifier to predict airline passenger satisfaction based on travel-related features like class, travel type, service ratings, and more. It includes data preprocessing, normalization, exploratory data analysis (EDA), model training, hyperparameter tuning, and decision boundary visualization.

---

## Dataset

- **Name**: Airline Passenger Satisfaction
- **Source**: [Kaggle Dataset](https://www.kaggle.com/datasets/teejmahal20/airline-passenger-satisfaction)
- **Size**: 129,880 rows, 24 features
- **Target**: `satisfaction` (Satisfied or Neutral/Dissatisfied)

---

## Project Workflow

### 1. Data Preprocessing
- Handled missing values using median imputation
- Encoded categorical features using `LabelEncoder`
- Scaled numerical features using `StandardScaler`

### 2. Model Building
- Used `KNeighborsClassifier` from `sklearn`
- Split data into 80% training and 20% test sets
- Trained KNN with various values of `K`

### 3. Hyperparameter Tuning
- Tested `K` values from 1 to 15 using 5-fold cross-validation
- Plotted cross-validated accuracy vs. `K`
- **Best K found: 7**, with ~92.90% accuracy

### 4. Evaluation
- Evaluated model with:
  - Accuracy
  - Confusion Matrix
  - Precision, Recall, F1-score (using `classification_report`)
- Achieved final test accuracy of **~92.90%**

### 5. Dimensionality Reduction & Visualization
- Used **PCA** to reduce data to 2D
- Visualized decision boundaries of KNN in PCA space
- Demonstrated clear class separation and model boundary

---

## Results

- **Best K**: 7
- **Cross-validated Accuracy**: ~92.90%
- **Final Test Accuracy**: ~92.90%
- **Model Insights**:
  - KNN performs well on this dataset
  - Proper scaling and encoding significantly impact performance
  - PCA is effective for decision boundary visualization in high-dimensional data
