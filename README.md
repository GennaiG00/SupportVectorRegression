# Support Vector Regression (SVR) Exploration

This repository contains a Jupyter Notebook (`sample.ipynb`) that explores Support Vector Regression (SVR), a powerful machine learning algorithm used for continuous variable estimation. The notebook bridges the conceptual gap between Support Vector Classification (SVC) and Regression, ultimately applying SVR to a real-world, high-dimensional dataset.

## 📋 Table of Contents
- [Overview](#overview)
- [Notebook Structure](#notebook-structure)
- [Case Study: Concrete Compressive Strength](#case-study)
- [Results & Evaluation](#results--evaluation)
- [Requirements](#requirements)
- [Usage](#usage)

## 📖 Overview
Support Vector Regression (SVR) adapts the principles of Support Vector Machines (SVM) for regression tasks. Instead of finding a hyperplane that separates classes, SVR attempts to find a function that best approximates the continuous target variable while minimizing error. It introduces an $\epsilon$-insensitive tube, where errors falling within a threshold ($\epsilon$) are ignored, allowing for a sparse and robust solution.

## 🗂️ Notebook Structure
The notebook is structured to guide the user from foundational intuition to practical, high-dimensional application:

1. **Introduction to SVM (Classification):** - A 2D example demonstrating linearly separable data.
   - Visualization of the decision boundary, margins, and support vectors using `sklearn.svm.SVC`.
2. **Introduction to SVR (Regression):**
   - A simple regression problem illustrating SVR behavior on data with random noise.
   - Implementation of `sklearn.svm.SVR` with a Linear Kernel.
   - Visualization of the central prediction line and the $\epsilon$-margin tube.
3. **High-Dimensional Real Case Study:**
   - Application of SVR on a real-world dataset (predicting **Concrete Compressive Strength** based on its ingredients).
   - Working in an $n$-dimensional space ($n > 2$) where direct plotting is not feasible, relying on mathematical evaluation instead.
4. **Kernel Comparison:**
   - Evaluating the model's performance using different kernels: **Linear**, **Sigmoid**, **RBF** (Radial Basis Function), and **Polynomial**.

## 🏗️ Case Study: Concrete Compressive Strength
The final section of the notebook evaluates the relationship between various concrete ingredients and the resulting compressive strength. Because the data involves multiple features, it operates in a high-dimensional space, requiring robust performance metrics to interpret the results.

## 📊 Results & Evaluation
Models are evaluated using standard regression metrics:
- **MSE (Mean Squared Error)** and **MAE (Mean Absolute Error):** Error metrics where lower values indicate better performance.
- **$R^2$ (R-squared):** Goodness-of-fit metric where higher values represent better model accuracy.

**Key Findings:**
- The relationship between concrete ingredients and compressive strength is inherently **non-linear**.
- **Linear and Sigmoid kernels** resulted in suboptimal performance.
- **RBF and Polynomial kernels** achieved significantly higher accuracy, yielding the best $R^2$ scores and the lowest error rates.

## 💻 Requirements
To run the notebook, you need a Python environment with the following libraries installed:
- `numpy`
- `matplotlib`
- `scikit-learn`
- `jupyter` 

## 🚀 Usage
1. Clone the repository and navigate into the directory.
2. Install the required dependencies:
   ```bash
   pip install numpy matplotlib scikit-learn jupyter
