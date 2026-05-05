# 🏦 Bank Marketing Subscription Predictor

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics.

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence[cite: 1].
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions[cite: 1].

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics[cite: 1]:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **80%** |
| **Precision** | **0.78** |
| **Recall** | **0.79** |
| **F1-Score** | **0.79** |

### Visual Insights
> **Confusion Matrix**
> <img width="566" height="460" alt="Confusion Matrix" src="https://github.com/user-attachments/assets/6df0674d-cbd1-4742-bdb6-95963e1ef0ee" />

> *The matrix shows a balanced performance, effectively capturing 79% of potential subscribers (Recall).*

---

## ⚙️ Hyperparameters & Configuration
Following the **Industry Checklist**, these parameters provided the most stable results[cite: 1]:
*   **Optimizer**: Adam (Adaptive Learning Rate)[cite: 1].
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction)[cite: 1].
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).

---

## 🚀 How to Run & Deploy

### Option 1: Google Colab (Recommended)
1.  Click the **Open in Colab** badge at the top.
2.  Upload the `bank.csv` file when prompted.
3.  Go to `Runtime` -> `Run All`.

### Option 2: Local Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/shivisrivastava0212/bank-marketing-subscription-predictor.git
    ```
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn tensorflow
    ```
3.  Run the pipeline:
    ```bash
    python scripts/model_pipeline.py
    ```

---

## 🧠This `README.md` is designed to be high-impact, professional, and systematically structured to impress recruiters. It incorporates the **industry-standard utilities** like early stopping and model checkpoints while following your specific **double asterisk** formatting rule for metrics.

---

# 🏦 Bank Marketing Subscription Predictor

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivisrivastava0212/bank-marketing-subscription-predictor/blob/main/notebooks/bank_marketing_analysis.ipynb)

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics[cite: 1].

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence[cite: 1].
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions[cite: 1].

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics[cite: 1]:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **80%** |
| **Precision** | **0.78** |
| **Recall** | **0.79** |
| **F1-Score** | **0.79** |

### Visual Insights
> **Confusion Matrix**
> ![Confusion Matrix](visuals/confusion_matrix.png)
> *The matrix shows a balanced performance, effectively capturing 79% of potential subscribers (Recall).*

---

## ⚙️ Hyperparameters & Configuration
Following the **Industry Checklist**, these parameters provided the most stable results[cite: 1]:
*   **Optimizer**: Adam (Adaptive Learning Rate)[cite: 1].
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction)[cite: 1].
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).

---

## 🚀 How to Run & Deploy

### Option 1: Google Colab (Recommended)
1.  Click the **Open in Colab** badge at the top.
2.  Upload the `bank.csv` file when prompted.
3.  Go to `Runtime` -> `Run All`.

### Option 2: Local Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/shivisrivastava0212/bank-marketing-subscription-predictor.git
    ```
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn tensorflow
    ```
3.  Run the pipeline:
    ```bash
    python scripts/model_pipeline.py
    ```

---

## 🧠 Lessons Learned
*   **Bias vs. Variance**: Managed high variance by implementing **Dropout** and **L2 Regularization**This `README.md` is designed to be high-impact, professional, and systematically structured to impress recruiters. It incorporates the **industry-standard utilities** like early stopping and model checkpoints while following your specific **double asterisk** formatting rule for metrics.

---

# 🏦 Bank Marketing Subscription Predictor

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivisrivastava0212/bank-marketing-subscription-predictor/blob/main/notebooks/bank_marketing_analysis.ipynb)

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics[cite: 1].

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence[cite: 1].
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions[cite: 1].

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics[cite: 1]:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **80%** |
| **Precision** | **0.78** |
| **Recall** | **0.79** |
| **F1-Score** | **0.79** |

### Visual Insights
> **Confusion Matrix**
> ![Confusion Matrix](visuals/confusion_matrix.png)
> *The matrix shows a balanced performance, effectively capturing 79% of potential subscribers (Recall).*

---

## ⚙️ Hyperparameters & Configuration
Following the **Industry Checklist**, these parameters provided the most stable results[cite: 1]:
*   **Optimizer**: Adam (Adaptive Learning Rate)[cite: 1].
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction)[cite: 1].
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).

---

## 🚀 How to Run & Deploy

### Option 1: Google Colab (Recommended)
1.  Click the **Open in Colab** badge at the top.
2.  Upload the `bank.csv` file when prompted.
3.  Go to `Runtime` -> `Run All`.

### Option 2: Local Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/shivisrivastava0212/bank-marketing-subscription-predictor.git
    ```
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn tensorflow
    ```
3.  Run the pipeline:
    ```bash
    python scripts/model_pipeline.py
    ```

---

## 🧠 Lessons Learned
*   **Bias vs. Variance**: Managed high variance by implementing **Dropout** and **L2 Regularization**[cite: 1].
*   **Better Data**: Refined performance by focusing on feature selection rather than just increasing model complexityThis `README.md` is designed to be high-impact, professional, and systematically structured to impress recruiters. It incorporates the **industry-standard utilities** like early stopping and model checkpoints while following your specific **double asterisk** formatting rule for metrics.

---

# 🏦 Bank Marketing Subscription Predictor

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivisrivastava0212/bank-marketing-subscription-predictor/blob/main/notebooks/bank_marketing_analysis.ipynb)

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics[cite: 1].

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence[cite: 1].
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions[cite: 1].

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics[cite: 1]:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **80%** |
| **Precision** | **0.78** |
| **Recall** | **0.79** |
| **F1-Score** | **0.79** |

### Visual Insights
> **Confusion Matrix**
> ![Confusion Matrix](visuals/confusion_matrix.png)
> *The matrix shows a balanced performance, effectively capturing 79% of potential subscribers (Recall).*

---

## ⚙️ Hyperparameters & Configuration
Following the **Industry Checklist**, these parameters provided the most stable results[cite: 1]:
*   **Optimizer**: Adam (Adaptive Learning Rate)[cite: 1].
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction)[cite: 1].
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).

---

## 🚀 How to Run & Deploy

### Option 1: Google Colab (Recommended)
1.  Click the **Open in Colab** badge at the top.
2.  Upload the `bank.csv` file when prompted.
3.  Go to `Runtime` -> `Run All`.

### Option 2: Local Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/shivisrivastava0212/bank-marketing-subscription-predictor.git
    ```
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn tensorflow
    ```
3.  Run the pipeline:
    ```bash
    python scripts/model_pipeline.py
    ```

---

## 🧠 Lessons Learned
*   **Bias vs. Variance**: Managed high variance by implementing **Dropout** and **L2 Regularization**[cite: 1].
*   **Better Data**: Refined performance by focusing on feature selection rather than just increasing model complexity.

---

###This `README.md` is designed to be high-impact, professional, and systematically structured to impress recruiters. It incorporates the **industry-standard utilities** like early stopping and model checkpoints while following your specific **double asterisk** formatting rule for metrics.

---

# 🏦 Bank Marketing Subscription Predictor

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/shivisrivastava0212/bank-marketing-subscription-predictor/blob/main/notebooks/bank_marketing_analysis.ipynb)

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics[cite: 1].

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence[cite: 1].
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions[cite: 1].

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics[cite: 1]:

| Metric | Result |
| :--- | :--- |
| **Accuracy** | **80%** |
| **Precision** | **0.78** |
| **Recall** | **0.79** |
| **F1-Score** | **0.79** |

### Visual Insights
> **Confusion Matrix**
> ![Confusion Matrix](visuals/confusion_matrix.png)
> *The matrix shows a balanced performance, effectively capturing 79% of potential subscribers (Recall).*

---

## ⚙️ Hyperparameters & Configuration
Following the **Industry Checklist**, these parameters provided the most stable results[cite: 1]:
*   **Optimizer**: Adam (Adaptive Learning Rate)[cite: 1].
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction)[cite: 1].
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).

---

## 🚀 How to Run & Deploy

### Option 1: Google Colab (Recommended)
1.  Click the **Open in Colab** badge at the top.
2.  Upload the `bank.csv` file when prompted.
3.  Go to `Runtime` -> `Run All`.

### Option 2: Local Execution
1.  Clone the repository:
    ```bash
    git clone https://github.com/shivisrivastava0212/bank-marketing-subscription-predictor.git
    ```
2.  Install dependencies:
    ```bash
    pip install pandas scikit-learn matplotlib seaborn tensorflow
    ```
3.  Run the pipeline:
    ```bash
    python scripts/model_pipeline.py
    ```

---

## 🧠 Lessons Learned
*   **Bias vs. Variance**: Managed high variance by implementing **Dropout** and **L2 Regularization**[cite: 1].
*   **Better Data**: Refined performance by focusing on feature selection rather than just increasing model complexity.

---

### **Author**
**Shivi Srivastava**  
*Student at Amity University Uttar Pradesh*  
