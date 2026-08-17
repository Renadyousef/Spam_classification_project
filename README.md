# 📧 Spam Email Classification Using Machine Learning

##  Project Overview

This project focuses on building and evaluating machine learning models to classify emails as **Spam** or **Not Spam (Ham)**.

The project follows an end-to-end machine learning workflow, starting with data exploration and preprocessing, followed by feature engineering, baseline modeling, supervised classification, hyperparameter tuning, and model evaluation.

The goal is to identify a reliable classification model that can distinguish spam emails from legitimate emails while maintaining good generalization performance.

---

##  Objectives

The main objectives of this project are to:

* Explore and understand the email dataset.
* Perform data cleaning and preprocessing.
* Identify useful patterns and characteristics of spam emails.
* Engineer relevant features from email text.
* Establish baseline classification performance.
* Compare multiple supervised machine learning models.
* Investigate model overfitting and generalization.
* Tune the main models using hyperparameter optimization.
* Select the most suitable model for spam email classification.

---

##  Project Structure

The repository contains separate notebooks for each stage of the analysis and modeling process:

```text
Spam_classification_project/
│
├── artifacts/
│
├── Baseline.ipynb
├── Final_EDA.ipynb
├── Clustering_emails.ipynb
│
├── LazyClassifier.ipynb
├── logisticregression.ipynb
├── DecisionTree.ipynb
├── randomForest.ipynb
├── SVM.ipynb
│
├── requirements.txt
└── README.md
```

### Notebook Description

| Notebook                   | Purpose                                                   |
| -------------------------- | --------------------------------------------------------- |
| `Final_EDA.ipynb`          | Exploratory Data Analysis and feature engineering         |
| `Baseline.ipynb`           | Baseline model and initial performance evaluation         |
| `LazyClassifier.ipynb`     | Comparison of multiple classification algorithms          |
| `logisticregression.ipynb` | Logistic Regression implementation and evaluation         |
| `DecisionTree.ipynb`       | Decision Tree modeling, evaluation, and tuning            |
| `randomForest.ipynb`       | Random Forest classification                              |
| `SVM.ipynb`                | Support Vector Machine modeling and hyperparameter tuning |
| `Clustering_emails.ipynb`  | Unsupervised clustering analysis of emails                |

---

#  Exploratory Data Analysis

The EDA stage investigates the structure and characteristics of the email dataset before model training.

The analysis includes:

* Dataset inspection
* Data cleaning
* Missing-value checks
* Duplicate checks
* Distribution analysis
* Spam vs. non-spam exploration
* Text-based feature analysis
* Feature engineering
* Identification of patterns that distinguish spam from legitimate emails

### Feature Engineering

Several features were created from the email content to provide additional information to the classification models.

Examples include:

* Combined email text
* Capital-letter count
* Spam-related character patterns
* Other text-derived features

The engineered features are then used alongside the email text representation during the modeling stage.

---

#  Machine Learning Approach

The project uses a combination of supervised and unsupervised machine learning techniques.

## Baseline

A baseline model was established first to provide a reference point for evaluating the performance of more advanced models.

This makes it possible to determine whether subsequent preprocessing, feature engineering, and model tuning actually improve classification performance.

---

## LazyClassifier

`LazyClassifier` was used to quickly compare multiple supervised classification algorithms using the prepared training and validation data.

This provided an initial overview of which algorithms were promising candidates for the spam classification problem.

The results from this comparison were then used to identify the main models for deeper evaluation and tuning.

---

#  Decision Tree

A Decision Tree classifier was developed and evaluated.

The analysis included:

* Training and validation performance
* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix
* Classification report
* Overfitting analysis
* Tree-depth investigation
* Hyperparameter tuning

Special attention was given to the difference between training and validation performance to determine whether the tree was overfitting.

---

#  Random Forest

Random Forest was evaluated as another supervised classification approach.

The model combines multiple decision trees to produce a more robust classification result.

Its performance was evaluated using classification metrics and compared against the other supervised models.

---

# Logistic Regression

Logistic Regression was implemented as a linear classification approach.

It provides an important benchmark because spam classification is fundamentally a binary classification problem.

The model was evaluated using standard classification metrics and compared with the tree-based and kernel-based approaches.

---

#  Support Vector Machine

A Support Vector Machine (SVM) classifier was implemented and tuned.

Hyperparameter optimization was performed using **GridSearchCV**.

The search included parameters such as:

* `C`
* `kernel`
* `gamma`

The purpose of tuning was to find a model configuration that provides strong validation performance while maintaining good generalization.

---

#  Model Evaluation

The models were evaluated using multiple classification metrics rather than relying on accuracy alone.

### Accuracy

Measures the overall percentage of correctly classified emails.

### Precision

Measures how many emails predicted as spam were actually spam.

### Recall

Measures how many of the actual spam emails were successfully detected.

### F1-Score

Provides a balance between precision and recall.

### Confusion Matrix

Provides a detailed breakdown of:

* True Positives
* True Negatives
* False Positives
* False Negatives

For a spam-filtering system, false positives are particularly important because incorrectly classifying a legitimate email as spam can cause important messages to be missed.

---

#  Overfitting & Generalization

Training and validation performance were compared for the main models.

The purpose was to determine whether each model was:

* **Underfitting**
* **Overfitting**
* **Generalizing well**

For example, a large difference between training and validation performance can indicate that a model has learned the training data too closely.

This analysis was particularly important when selecting the appropriate complexity for the Decision Tree and evaluating the tuned SVM.

---

#  Hyperparameter Tuning

Hyperparameter optimization was applied to the main models to improve their performance.

Grid Search was used to systematically evaluate different parameter combinations and identify configurations that performed well on the validation data.

The goal was not simply to maximize training performance, but to obtain a model that generalizes well to unseen emails.

---

#  Unsupervised Learning

In addition to supervised classification, the project includes an exploratory clustering analysis.

The clustering notebook investigates whether emails can naturally form meaningful groups based on their characteristics without using the spam labels during clustering.

This provides an additional perspective on the structure of the email dataset.

---

#  Model Selection

The final model should be selected based on its performance on unseen validation data rather than training performance alone.

The main considerations are:

* Validation performance
* F1-score
* Precision
* Recall
* Generalization
* Overfitting behavior
* Suitability for the spam-filtering problem

For spam detection, a balanced evaluation is important because both **missing spam emails** and **incorrectly filtering legitimate emails** can negatively affect users.

The detailed model results and comparisons are available in the individual notebooks.

---

# 🛠️ Technologies Used

* **Python**
* **Pandas**
* **NumPy**
* **Scikit-learn**
* **Jupyter Notebook**
* **Matplotlib**
* **Seaborn**
* **LazyClassifier**
* **GridSearchCV**
* Machine Learning
* Natural Language Processing
* Exploratory Data Analysis

---

#  Getting Started

## 1. Clone the repository

```bash
git clone https://github.com/Renadyousef/Spam_classification_project.git
cd Spam_classification_project
```

## 2. Install the required dependencies

```bash
pip install -r requirements.txt
```

## 3. Open the notebooks

Launch Jupyter Notebook or Jupyter Lab:

```bash
jupyter notebook
```

Then start with:

```text
Final_EDA.ipynb
```

and continue through the modeling notebooks.



