# 🏦 Bank Marketing Subscription Predictor

## 📋 Project Overview
This project implements a high-performance classification pipeline to predict customer response to bank term deposit campaigns. By analyzing demographic and behavioral data, the model identifies high-potential leads, allowing for optimized marketing resource allocation.

The project follows a **Golden Training Pipeline** to ensure stability, prevent overfitting, and achieve industry-grade evaluation metrics.

---

## 🏗️ Systematic Workflow

### 1. Data Processing & Brute Force Cleaning
*   **Standardization**: Used `StandardScaler` to normalize feature scales for optimal convergence.
*   **Brute Force Cleaning**: Implemented a custom utility to automatically handle varying CSV column names and handle missing values through automated imputation.
*   **Stratified Split**: Utilized an **80-20 train-test split** to maintain class proportions].
*   **Imbalance Handling**: Addressed potential class imbalance by using **Stratified Sampling** to ensure training and validation sets were accurately representative of the minority "subscriber" class.
*   **Evaluation Environment**: Utilized **Google Colab** with hardware acceleration (GPU/TPU) to manage data scaling and accelerate model iterations efficiently.

### 2. Industry-Grade Training Utilities
To ensure the model reaches the **best weights**, the following callbacks were implemented:
*   **Early Stopping**: Monitored `val_loss` with a patience of 5 to prevent overfitting.
*   **Model Checkpoint**: Automatically saved the `best_model.h5` based on validation performance.
*   **LR Scheduler**: Used `ReduceLROnPlateau` to decrease the learning rate when learning stagnated.

---

## 📊 Performance Metrics

The model was evaluated using a comprehensive suite of industry-standard metrics:

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
Following the **Industry Checklist**, these parameters provided the most stable results:
*   **Optimizer**: Adam (Adaptive Learning Rate).
*   **Epochs**: **50** (with Early Stopping active).
*   **Batch Size**: **32** (Balanced for speed and noise reduction).
*   **Best Model Weights**: Found at **Epoch 14** (Restored via `restore_best_weights=True`).
*   **Loss Function**: Utilized **Binary Cross-Entropy** as the objective function, the industry standard for optimizing binary classification tasks.
*   **Activation Functions**: Implemented **ReLU** for hidden layers to prevent vanishing gradients and a **Sigmoid** activation for the output layer to generate a precise probability score.
---

## 📉 Training Stability & Overfitting Control
To maintain a balance between **Bias and Variance**, I implemented the following techniques:
*   **Dropout (0.5)**: Applied to hidden layers to prevent co-dependency between neurons and force the network to learn robust features.
*   **Weight Decay (L2 Regularization)**: Added a penalty to large weights to simplify the model and improve generalization on unseen bank data.
*   **Early Stopping**: Monitored `val_loss` and restored **best model weights** from the optimal epoch to ensure the model did not train into the "overfitting zone".


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

*   **Bias vs. Variance Tradeoff**: By monitoring the gap between training loss and validation loss, I identified and mitigated overfitting using **Dropout (0.5)** and **L2 Regularization**.
*   **The Power of Data Scaling**: I observed that without `StandardScaler`, the model took significantly longer to converge and was less stable during training.
*   **Industry-Standard Callbacks**: Implementing **Early Stopping** and **Model Checkpoint** ensured that the final model utilized the **best weights** from **Epoch 14**, rather than just the final epoch.
*   **Metric Selection**: I learned that for a marketing campaign, **Accuracy** can be misleading; focusing on **Recall** is crucial to ensure that potential high-value customers are not missed by the model.
*   **Start Simple, Then Scale**: Following the **Golden Rule**, I started with a simple baseline experiment before increasing model complexity, which helped in identifying the most impactful features early on.

---
## 👨‍💻 Author
**Shivi Srivastava**  
*Aspiring AI Engineer | Amity University Uttar Pradesh*  
[LinkedIn Profile](https://www.linkedin.com/in/shivi-srivastava-8a5086310/) | [GitHub Portfolio](https://github.com/shivisrivastava0212)  
