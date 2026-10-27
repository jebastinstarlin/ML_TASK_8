# Phishing Website Detection Using SVM

## 1. Project Overview

This project implements a Machine Learning-based **Phishing Website Detection System** using a Support Vector Machine (SVM) classifier. The model is trained on the PhiUSIIL Phishing URL Dataset to predict whether a website is phishing or legitimate based on various URL and website-related features.

## 2. Objectives

The primary objectives of this project are:

- To detect phishing websites using Machine Learning.
- To train an SVM classification model using website feature data.
- To evaluate model performance using standard classification metrics.
- To visualize classification results using a Confusion Matrix and ROC Curve.

## 3. Technologies Used

The following technologies and libraries are used in this project:

- **Python** – Programming language.
- **Pandas** – Data manipulation and analysis.
- **NumPy** – Numerical computations.
- **Matplotlib** – Data visualization.
- **Seaborn** – Statistical data visualization.
- **Scikit-learn** – Machine Learning model development and evaluation.

## 4. Dataset

**Dataset Name:** PhiUSIIL Phishing URL Dataset

The dataset contains website-related features and labels indicating whether a website is phishing or legitimate. These features are used to train and evaluate the SVM classification model.

## 5. Data Preprocessing

The following preprocessing steps are performed:

1. Load the dataset from a CSV file.
2. Remove records with missing target labels.
3. Drop non-numeric and irrelevant columns, including `URL`, `Domain`, `TLD`, and `Title`.
4. Separate the target column, `Label`, from the input features.
5. Convert the target labels into binary values.
6. Replace infinite values with `NaN`.
7. Fill missing numerical values using median values.
8. Select numerical features for model training.
9. Split the dataset into training and testing sets.

## 6. Machine Learning Model

The classifier used in this project is **Linear Support Vector Classification (LinearSVC)**.

### Pipeline Components

- **StandardScaler:** Standardizes numerical features to improve model training.
- **LinearSVC:** Classifies websites as phishing or legitimate using a linear decision boundary.

### Model Parameters

```python
LinearSVC(
    C=1.0,
    class_weight="balanced",
    random_state=42,
    max_iter=5000
)
```

The model is implemented using a Scikit-learn pipeline that combines feature scaling and classification.

## 7. Dataset Splitting

The dataset is divided into two subsets:

- **Training Set:** 80% of the dataset, used to train the model.
- **Testing Set:** 20% of the dataset, used to evaluate model performance.

## 8. Evaluation Metrics

The model's performance is evaluated using the following metrics:

- **Confusion Matrix:** Shows the number of correct and incorrect predictions for each class.
- **Precision:** Measures the proportion of predicted phishing websites that are actually phishing.
- **Recall:** Measures the proportion of actual phishing websites correctly identified by the model.
- **F1-Score:** Calculates the harmonic mean of precision and recall.
- **ROC-AUC Score:** Measures the model's ability to distinguish between phishing and legitimate websites.
- **Classification Report:** Provides precision, recall, F1-score, and support for each class.

## 9. Visualizations

### 9.1 Confusion Matrix

The Confusion Matrix visualizes the model's classification results by showing the number of correctly and incorrectly classified phishing and legitimate websites.

### 9.2 ROC Curve

The Receiver Operating Characteristic (ROC) Curve illustrates the classifier's ability to distinguish between phishing and legitimate websites at different decision thresholds. The ROC-AUC score summarizes the model's overall discriminative ability.

## 10. Project Structure

```text
Phishing-Website-Detection/
│
├── ML task 9.py
├── PhiUSIIL_Phishing_URL_Dataset.csv
└── README.md
```

## 11. How to Run the Project

### Step 1: Install Dependencies

Open a terminal and execute the following command:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

### Step 2: Place the Dataset

Ensure that `PhiUSIIL_Phishing_URL_Dataset.csv` is located in the project directory.

Update the dataset path in the Python script if necessary:

```python
df = pd.read_csv("PhiUSIIL_Phishing_URL_Dataset.csv")
```

### Step 3: Run the Python Script

Execute the following command in the terminal:

```bash
python "ML task 9.py"
```

### Step 4: View the Results

After execution, the program displays the dataset summary, class distribution, evaluation metrics, and classification report. It also generates the Confusion Matrix and ROC Curve visualizations.

## 12. Expected Output

The program produces the following results:

- Dataset summary and information.
- Class distribution of phishing and legitimate websites.
- Trained SVM classification model.
- Confusion Matrix visualization.
- Precision, Recall, and F1-Score.
- ROC-AUC score.
- Classification Report.
- ROC Curve visualization.

**Note:** Actual evaluation scores depend on the dataset, preprocessing steps, target-label mapping, and model performance.

## 13. Learning Outcomes

Through this project, you will learn:

- Data preprocessing and handling missing values.
- Numerical feature selection.
- Feature scaling using StandardScaler.
- Machine Learning classification using SVM.
- Model evaluation using classification metrics.
- Visualization of classification results using Matplotlib and Seaborn.
- Application of Machine Learning to cybersecurity and phishing website detection.

## 14. Conclusion

The Phishing Website Detection System demonstrates how Machine Learning can be applied to cybersecurity to identify potentially fraudulent websites. By using a Linear Support Vector Classifier and evaluating its performance through multiple metrics and visualizations, the project provides a practical approach to distinguishing phishing websites from legitimate ones.
