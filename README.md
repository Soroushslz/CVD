# CVD

# Comparative Evaluation of Deep Learning Models for Cardiovascular Disease Diagnosis and Classification

**Author**: [Soroush Soltanizadeh](https://www.linkedin.com/in/soroush-soltanizadeh-1136892b6/)
**Google Scholar**: [Profile](https://scholar.google.com/citations?user=ARKNJYwAAAAJ&hl=en)

---

## 🩺 Overview

Cardiovascular diseases (CVDs) remain the leading cause of mortality worldwide. Early and precise diagnosis is critical in preventing fatal outcomes. This project presents a comparative analysis of several deep learning architectures, specifically designed for **automated diagnosis and classification of CVDs** using ECG data.

We evaluate models based on accuracy, F1-score, and computational complexity using the **PTB Diagnostic ECG (PTB-ECG)** dataset. The objective is to identify models that strike the best balance between performance and efficiency for real-time, AI-driven CVD diagnosis.

---

## 🧠 Models Evaluated

* **Convolutional Neural Network (CNN)**
* **Multilayer Perceptron (MLP)**
* **Long Short-Term Memory (LSTM)**
* **CNN-MLP (Hybrid)**
* **ConvLSTM (Convolutional LSTM)**

> 🏆 **Key Finding**: The **LSTM model** achieved **99.98% accuracy**, **98% F1-score**, and **100% precision**, outperforming other architectures in both diagnostic performance and model robustness.

---

## 📊 Dataset

* **Name**: PTB Diagnostic ECG Dataset
* **Source**: Publicly available ECG recordings
* **Features**: ECG signal samples
* **Target**: CVD classification labels

---

## ⚙️ Methodology

1. **Data Preprocessing**

   * Standardization using `StandardScaler`
   * Reshaping ECG signals for model compatibility
   * Label encoding for categorical targets

2. **Model Architecture**

   * CNN with Conv1D layers and dropout for regularization
   * Training with `Adam` optimizer and sparse categorical cross-entropy loss

3. **Training and Evaluation**

   * 80/20 train-test split
   * Metrics: Accuracy, F1-score, Precision
   * Complexity measured by convolutional layer operations

---

## 📈 Results

| Model    | Accuracy   | F1-Score | Precision | Remarks                                   |
| -------- | ---------- | -------- | --------- | ----------------------------------------- |
| **LSTM** | **99.98%** | **98%**  | **100%**  | Best overall performance                  |
| CNN      | \~93–95%   | \~93%    | \~94%     | Efficient but less accurate               |
| CNN-MLP  | \~96%      | \~96%    | \~97%     | Good trade-off between accuracy and speed |
| ConvLSTM | \~97.5%    | \~97%    | \~97%     | Strong hybrid performance                 |

> 🧮 **CNN Complexity**: Computed based on convolution kernel size, filters, strides, and input dimensions.

---

## 💡 Significance

* Demonstrates the feasibility of **low-complexity DL models** for **real-time CVD diagnosis**
* Enhances diagnostic **efficiency** and **accuracy**, reducing human error in ECG interpretation
* Contributes to the development of **clinically viable AI tools** for cardiovascular healthcare

---

## 🛠 Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/cvd-deep-learning-evaluation.git
cd cvd-deep-learning-evaluation
```

2. Install required libraries:

```bash
pip install -r requirements.txt
```

> Libraries include `TensorFlow`, `NumPy`, `Pandas`, `Scikit-learn`

3. Run the training:

```bash
python main.py
```

---

## 📌 Future Work

* Extend to multi-lead ECG classification
* Incorporate explainable AI techniques (e.g., SHAP, LIME)
* Validate on larger and more diverse datasets

---

## 📄 License

This project is licensed under the MIT License.
