# Probability Density Function Learning using Roll-Parameterized Non-Linear Model

## 📌 Overview

This project implements learning of a Probability Density Function (PDF) using a roll-number-parameterized non-linear transformation. The NO₂ feature from an air quality dataset is used as the input variable.

The goal is to transform the original feature using a non-linear function and estimate the parameters of a Gaussian-like probability density function.

---

## 📊 Dataset

https://www.kaggle.com/datasets/shrutibhargava94/india-air-quality-data

* Dataset: India Air Quality Data
* Feature Used: **NO₂ (Nitrogen Dioxide)**
* Source: Kaggle Air Quality Dataset

---

## ⚙️ Methodology

### Step 1: Non-linear Transformation

Each NO₂ value (x) is transformed into (z) using:

[z = x + a_r \sin(b_r x)]

Where:

* (a_r = 0.05 \times (r \mod 7))
* (b_r = 0.3 \times ((r \mod 5) + 1))
* (r) represents the university roll number.

---

### Step 2: Probability Density Function Estimation

The transformed variable (z) is modeled using:

[\hat{p}(z) = c , e^{-\lambda (z-\mu)^2}]

Parameters estimated:

* ( \mu ) — Mean of transformed data
* ( \lambda ) — Shape parameter derived from variance
* ( c ) — Normalization constant

Estimation Method:

* Maximum Likelihood Estimation (MLE) assuming Gaussian distribution.

---

## 🧮 Estimated Parameters

* **μ (mu):** 22.671161025366196
* **λ (lambda):** 0.002127276758301982
* **c:** 0.026021783620968932

---

## 💻 Technologies Used

* Python
* NumPy
* Pandas
* Google Colab

---

## 📜 License

MIT License
