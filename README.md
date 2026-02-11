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

## Results


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
<img width="509" height="91" alt="Screenshot 2026-02-11 at 10 26 32 PM" src="https://github.com/user-attachments/assets/69c6e118-a8d5-4f01-94ba-e77c4afa73bc" />
<img width="435" height="39" alt="Screenshot 2026-02-11 at 10 27 15 PM" src="https://github.com/user-attachments/assets/a4f7494a-1983-4d29-b982-5109c5811b66" />
<img width="457" height="72" alt="Screenshot 2026-02-11 at 10 27 49 PM" src="https://github.com/user-attachments/assets/84b4f9ca-3658-4c9c-a7e1-ce31a45cbaa8" />
<img width="465" height="84" alt="Screenshot 2026-02-11 at 10 28 23 PM" src="https://github.com/user-attachments/assets/c06fac53-8395-46bb-81e5-b3ca8ca0e8fc" />

<img width="726" height="576" alt="Screenshot 2026-02-11 at 10 28 58 PM" src="https://github.com/user-attachments/assets/a866129c-6386-4d5e-977a-e8ab31e4d42d" />


<img width="658" height="85" alt="Screenshot 2026-02-11 at 10 29 40 PM" src="https://github.com/user-attachments/assets/c96ec3ee-8390-49e4-a2c8-0f77e568892e" />


---

#  Conclusion

This project demonstrates two approaches to probability density estimation:

- A flexible data-driven GAN approach  
- A structured parametric modeling approach  

Both methods provide insight into learning and approximating probability distributions from real-world environmental data.
