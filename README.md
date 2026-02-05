# Gym Experience Classification using SVM

## About the Project
This project is a machine learning classification task where I tried to predict whether a gym member is a **Beginner** or **Experienced** based on their workout behavior and physiological data.

I built this project mainly to strengthen my understanding of:
- Support Vector Machines (SVM)
- Feature engineering
- Model comparison
- Proper evaluation using cross-validation

Instead of focusing only on accuracy, I focused on **building a clean and correct ML workflow**.

## Dataset Overview
The dataset contains information about gym members, including:
- Age and gender
- Workout duration and frequency
- Heart rate measurements
- Body fat percentage and water intake
- Experience level (1 = Beginner, 2–3 = Intermediate/Advanced)

For this project, I converted the original experience levels into a **binary target**:
- **Beginner** → Experience_Level = 1  
- **Experienced** → Experience_Level = 2 or 3  

This made the classification task clearer and easier to interpret.

## What I Did in This Project

### 1. Exploratory Data Analysis (EDA)
- Analyzed age distribution, gender breakdown, and workout types
- Studied correlations between numerical features
- Visualized how experience level varies across age groups

This helped me understand patterns in the data before modeling.

### 2. Feature Engineering
- Grouped age into ranges (18–25, 26–35, etc.)
- One-hot encoded categorical features
- Standardized numerical features
- Removed features that could cause data leakage (like calories burned)

The goal was to keep features meaningful and fair for training.

### 3. Model Building
I trained and compared multiple models:
- Logistic Regression (baseline)
- Linear Support Vector Machine
- RBF (Gaussian) Support Vector Machine

This helped me understand whether the decision boundary was mostly linear or nonlinear.

### 4. Model Tuning and Evaluation
- Used **GridSearchCV with 5-fold cross-validation** to tune SVM hyperparameters
- Compared models using accuracy, precision, recall, and confusion matrices
- Evaluated the final model on a held-out test set

The final model achieved around **89% accuracy**, with stable performance across folds.

## Key Takeaways
- The data is mostly linearly separable, but mild nonlinearity helps
- SVMs perform slightly better than Logistic Regression
- Cross-validation is important to avoid relying on lucky train-test splits
- Clean preprocessing matters as much as model choice

## Tools & Libraries Used
- Python
- pandas, numpy
- matplotlib, seaborn
- scikit-learn

## Why I Built This
I built this project as preparation for research work involving structured and signal-based data.  
It also helped me feel confident working with SVMs, pipelines, and evaluation methods that are commonly used in real-world ML projects.

## Author
**Rejim Oli**

This project was completed as a self-learning and research preparation exercise.
