# 📈 ISLR Chapters 5 & 6: Resampling Methods & Regularization Labs

[![GitHub Stars](https://img.shields.io/github/stars/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs?style=for-the-badge&logo=github&color=6699CC)](https://github.com/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs/network/members)
[![Issues](https://img.shields.io/github/issues/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs?style=for-the-badge&color=6699CC)](https://github.com/wajason/ISLR-Ch5-6-Resampling-Regularization-Labs/issues)
[![License](https://img.shields.io/badge/License-MIT-6699CC?style=for-the-badge)](./LICENSE)

This repository contains a comprehensive implementation and detailed annotation of the R code presented in **Chapter 5.3 (Resampling Methods)** and **Chapter 6.5 (Linear Models and Regularization Methods)** of *An Introduction to Statistical Learning* (James et al., 2021).

The aim is to provide a clear, step-by-step tutorial on model validation techniques and advanced linear modeling strategies, using the `Hitters` and `Auto` datasets to demonstrate how to improve prediction accuracy and interpretability.

---

## ✨ Key Features & Highlights

This tutorial goes beyond simply repeating the code by including:

* **Resampling Techniques (Ch 5):**
    * **Cross-Validation:** Implementation and comparison of **Leave-One-Out Cross-Validation (LOOCV)** and **k-Fold Cross-Validation** to estimate test error rates.
    * **The Bootstrap:** Using bootstrap to estimate the standard errors of coefficients, providing a robust alternative to standard formulas.

* **Variable Selection (Ch 6):**
    * **Best Subset Selection:** Visualizing RSS, $C_p$, BIC, and Adjusted $R^2$ to select the optimal model size.
    * **Stepwise Selection:** Implementing **Forward** and **Backward** stepwise selection for computationally efficient variable screening.

* **Regularization (Shrinkage Methods):**
    * **Ridge Regression:** Demonstrating how $L_2$ penalty shrinks coefficients (but doesn't nullify them) and finding the optimal $\lambda$ via CV.
    * **The Lasso:** showcasing the feature selection property of $L_1$ penalty, where coefficients are forced to zero, resulting in sparse models.
    * **Visualization:** Plots showing coefficient paths (shrinking towards zero) as the tuning parameter $\lambda$ increases .

* **Dimension Reduction:**
    * **PCR (Principal Components Regression):** Unsupervised dimension reduction.
    * **PLS (Partial Least Squares):** Supervised dimension reduction that considers the response variable $Y$.

---

## 📂 Repository Structure

| File | Description |
| :--- | :--- |
| `Resampling_and_Regularization_Tutorials.pdf` | **The fully rendered tutorial.** Contains all R code, output, plots (CV errors, Coefficient paths), and detailed personal commentary/analysis. |
| `README.md` | Project overview, links, and reproduction instructions. |

---

## 🛠️ Data Source & Reproduction

### Data Source
All data and primary code structure are derived from:
* **Book:** *An Introduction to Statistical Learning with Applications in R* (ISLR).
* **Authors:** Gareth James, Daniela Witten, Trevor Hastie, Robert Tibshirani (2021).
* **Key Datasets:**
    * `Hitters`: Predicting baseball player salaries (used for Ridge, Lasso, PCR, PLS).
    * `Auto`: Predicting MPG (used for Cross-Validation).

### Required R Packages
To recreate the analysis, you will need the following packages:
* `ISLR2` (Datasets)
* `boot` (For Cross-Validation & Bootstrap)
* `leaps` (For Subset Selection)
* `glmnet` (For Ridge & Lasso)
* `pls` (For PCR & PLS)

### How to Reproduce
1.  **Download** the PDF file to view the full annotated code.
2.  Install the required packages in R:
    ```r
    install.packages(c("ISLR2", "boot", "leaps", "glmnet", "pls"))
    ```
3.  Copy the code segments from the tutorial into your R environment to execute.
