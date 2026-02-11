# Predictive_Analysis_Assignment_2-Suresh-Sir-
#  Probability Density Function using Data

This project focuses on estimating the **Probability Density Function (PDF)** of NO₂ concentration data using two different approaches:

1. GAN-based distribution learning (Non-Parametric Approach)
2. Parametric Non-Linear Probability Model

The objective is to transform environmental data and learn its probability distribution using both deep learning and mathematical modeling techniques.

---

#  Project 1: PDF Estimation using GAN

##  Methodology

Data Collection  
→ Column Selection (no2)  
→ Data Transformation  
→ PDF Estimation using GAN  
→ PDF Approximation from Generated Samples  
→ PDF Visualization  

---

##  Dataset Information

- Dataset File: `data.csv`
- Target Column: `no2`

Missing values are removed before processing.

---

##  Data Transformation

The selected NO₂ values are transformed using:

z = T(x) = x + a sin(bx)

Where:
- x = standardized NO₂ values  
- a, b = transformation parameters  

This non-linear transformation increases distribution complexity.

---

##  PDF Estimation using GAN

A Generative Adversarial Network (GAN) is trained on the transformed data.

- The Generator produces synthetic samples.
- The Discriminator differentiates real and fake samples.
- Through adversarial learning, the generator captures the underlying distribution.

After training, generated samples are used to approximate the PDF.

---

##  PDF Approximation

The learned distribution is approximated using:

- Histogram-based density estimation
- Kernel Density Estimation (KDE)

These methods allow smooth visualization of the probability density curve.

---

##  Objectives

- Apply non-linear transformation to real-world data  
- Learn probability density directly from samples  
- Implement GAN for distribution modeling  
- Approximate and visualize the learned PDF  

---

## 📈 Results

- The GAN successfully models the transformed NO₂ distribution.
- KDE aligns closely with histogram density.
- The learned PDF reflects the non-linear structure of the data.

---

# Project 2: PDF using Parametric Non-Linear Model

##  Methodology

Data Collection  
→ Column Selection (no2)  
→ Data Transformation  
→ Parameter Estimation  
→ Probability Function Construction  
→ Parameter Output  

---

##  Dataset Information

- Dataset File: `data.csv`
- Target Column: `no2`

---

##  Data Transformation

The same transformation is applied:

z = T(x) = x + a sin(bx)

This ensures consistency across both modeling approaches.

---

## Probability Model

The probability density function is defined as:

p(z) = c * exp(-λ (z - μ)^2)

Where:
- μ = mean parameter  
- λ = precision-related parameter  
- c = normalization constant  

The parameters (μ, λ, c) are estimated from the transformed dataset.

---

##  Objectives

- Perform non-linear transformation of environmental data  
- Estimate parameters of a predefined density model  
- Construct a valid probability function  
- Display optimal parameter values (μ, λ, c)  

---

##  Results

- The estimated parameters define a smooth density curve.
- The parametric model captures the central tendency effectively.
- Demonstrates contrast between adversarial learning and analytical modeling.

---

# 🔍 Comparison

| Aspect | GAN-Based Model | Parametric Model |
|--------|-----------------|-----------------|
| Assumption | No prior PDF assumption | Assumes exponential quadratic form |
| Flexibility | High | Moderate |
| Learning Method | Adversarial Training | Parameter Estimation |
| Complexity | Higher | Lower |

---

#  Conclusion

This project demonstrates two approaches to probability density estimation:

- A flexible data-driven GAN approach  
- A structured parametric modeling approach  

Both methods provide insight into learning and approximating probability distributions from real-world environmental data.
