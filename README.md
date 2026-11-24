# Handwritten Digit Recognizer & Neural Network Visualizer (784–16–16–10) 🧠✍️

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/masvoorii/mnist-backprop-visualizer/blob/main/MNIST_Backprop_Visualizer.ipynb)
![Python](https://img.shields.io/badge/Python-3.x-3776AB?style=flat-square&logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-From_Scratch-013243?style=flat-square&logo=numpy&logoColor=white)

An end-to-end **Artificial Neural Network (ANN)** implementation built **from scratch using NumPy** to classify binary-thresholded MNIST handwritten digits (`0–9`), paired with an **interactive step-by-step HTML/SVG forward-propagation visualizer** inside Google Colab.

---

### ✨ Key Highlights

- **Pure NumPy Backpropagation Engine:** Implemented forward pass, backward error propagation, mini-batch updates, and momentum without high-level deep learning training abstractions (`keras.datasets` is used solely to fetch raw MNIST arrays).
- **Nguyen-Widrow Weight Initialization:** Accelerates convergence across hidden layers (`784 → 16 → 16 → 10`) using Sigmoid activations.
- **Systematic Hyperparameter Tuning & Overfitting Analysis:**
  - Grid search across learning rates ($\alpha$) and momentum ($\mu$), achieving **93.46% test accuracy** (`MSE: 0.0104`) on 5,000 isolated test samples.
  - Multi-scale dataset comparison (`500`, `2,000`, `10,000`, and `50,000` patterns) illustrating generalization vs. overfitting behavior.
- **Interactive Drawing Canvas & SVG Network Visualizer:** Draw any digit (`0–9`) directly in the notebook, inspect the centered `28×28` binary preprocessing output, and watch signal activations propagate across every layer in real time.

---

### 🛠️ Tech Stack

- **Core Math & Matrix Operations:** `NumPy`
- **Data Handling & Evaluation:** `Pandas`, `Scikit-Learn` (`train_test_split`, `confusion_matrix`, `classification_report`)
- **Visualization & Image Processing:** `Matplotlib`, `Seaborn`, `Pillow (PIL)`
- **Interactive UI:** `HTML5 Canvas`, `SVG`, `JavaScript` (via Google Colab Python-JS kernel callbacks)

---

### 🚀 How to Run

1. Click the **Open in Colab** badge at the top of this page (or open `MNIST_Backprop_Visualizer.ipynb` in Google Colab).
2. Run **Cells 1–4** sequentially to preprocess the 50,000 binary MNIST samples, run the grid search, and train the `784–16–16–10` model.
3. Run **Cell 5** to launch the interactive drawing canvas, draw a digit (`0–9`), and click **Tebak Angka ▶**.
