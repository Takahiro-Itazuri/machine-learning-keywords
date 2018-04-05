# Machine Learning Keywards
## Takahiro Itazuri (Waseda University)

---
## Pattern Recognition and Machine Learning
- Supervise Learning
  - Classification
  - Regression
- Unsupervised Learning
  - Clustering
- Reinforcement Learning

---
## Feature Space
- Normalization
- Wihtin-Class Variance and Between-Class Variance
- Curse of Dimensionality
- Dimension Reduction
  - Principal Component Analysis

+++
## Within-Class Variance and Between-Class Variance
Average Vector  
`$$ \bar{\boldsymbol{x}}_i = \frac{1}{n_i} \sum_{\boldsymbol{x}_p \in C_i} \boldsymbol{x}_p $$`
Variance
`$$ V_i = \frac{1}{n_i} \sum_{\boldsymbol{x}_p \in C_i} \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)^T \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)$$`
Within-Class Variance
`$$ V_w = \frac{1}{n} \sum_{i=1}^{M} \sum_{\boldsymbol{x}_p \in C_i} \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)^T \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right) $$`
Between-Class Variance
`$$ V_b = \frac{1}{n} \sum_{i=1}^{M} n_i \left( \bar{\boldsymbol{x]}_i - \bar{\boldsymbol{x}}} \right)^T \left( \bar{\boldsymbol{x]}_i - \bar{\boldsymbol{x}}} \right) $$`

+++
## Principal Component Analysis
Here, `$\hat{d}$` dimensional subspace is an orthogonal basis spanned by base vectors `$\boldsymbol{u}_1, \boldsymbol{u}_2, \cdots, \boldsymbol{u}_{\hat{d}}$`.  
Point `$\hat{\boldsymbol{x}}$` is mapped into this `$\hat{d}$` dimensional subspace.
`\begin{align} \hat{\boldsymbol{x}} &= (\boldsymbol{u}_1^T \boldsymbol{x}) \boldsymbol{u}_1 + (\boldsymbol{u}_2^T \boldsymbol{x}) \boldsymbol{u}_2 + \cdots + (\boldsymbol{u}_{\hat{d}}^T \boldsymbol{x}) \boldsymbol{u}_{\hat{d}} \\ &= \left( \boldsymbol{u}_1 \boldsymbol{u}_1^T + \boldsymbol{u}_2 \boldsymbol{u}_2^T + \cdots + \boldsymbol{u}_{\hat{d}} \boldsymbol{u}_{\hat{d}}^T \right) \\ &= \boldsymbol{A} \boldsymbol{A}^T \boldsymbol{x} \end{align}`
where
`\begin{align} \boldsymbol{A} = \begin{pmatrix} \boldsymbol{u}_1 & \boldsymbol{u}_2 & \cdots & \boldsymbol{u}_{\hat{d}} \end{pmatrix} \end{align}`

+++
## Principal Component Analysis (Variance Maximization)
Consider 1-dimensional subspace mapped by a base vector `$\boldsymbol{u}$`.  
Average vector in subspace
`$$ \hat{\boldsymbol{x}} = \frac{1}{n} \sum_{p=1}^{n} \boldsymbol{u}^T \boldsymbol{x}_p = \boldsymbol{u}^T \bar{\boldsymbol{x}} $$`
Variance in subspace
`$$ \hat{\boldsymbol{\Sigma}} = \frac{1}{n} \sum_{p=1}^{n} \left( \boldsymbol{u}^T \boldsymbol{x}_p - \boldsymbol{u}^T \hat{\boldsymbol{x}} \right) \left( \boldsymbol{u}^T \boldsymbol{x}_p - \boldsymbol{u}^T \hat{\boldsymbol{x}} \right)^T = \boldsymbol{u}^T \Sigma \boldsymbol{u} $$`

---
## Discriminant Function
- Linear Discriminant Function
  - Linearly Separable
  - Linear Discriminant Analysis (LDA)
  - Least Squares Method
- Bayes Discriminant Method
  - Bayes' Theorem
  - Maximum A Posteriori (MAP)
  - Bayesian Error Rate
  - Naive Bayes Method
  - Improved Naive Bayes Method

+++
## Discriminant Function
Given a function `$ g_1 (\boldsymbol{x}), g_2 (\boldsymbol{x}), \cdots, g_1 (\boldsymbol{x}) $` for each class`$ c_1, c_2, \cdots, c_M $`
`$$ \hat{c} = \mathop{\rm arg~max}\limits_{c_i \in C} g_i (\boldsymbol{x}) $$`

+++
## Linear Discriminant Function
Linear Discriminant Function (for class `$ c_i $`)  
`$$ g_i (\boldsymbol{x}) = \boldsymbol{w}_i^T \boldsymbol{x} $$`
where
`\begin{align} \boldsymbol{x} &= \begin{pmatrix} 1 & \boldsymbol{x}^T \end{pmatrix}^T = \begin{pmatrix} 1 & x_1 & x_2 & \cdots & x_d \end{pmatrix}^T \\ \boldsymbol{w} &= \begin{pmatrix} w_0 & w_1 & w_2 & \cdots & w_d \end{pmatrix} \end{align}`

+++
## Bayes Discriminant Method
Given a loss function `$ l(c,c') $`, expectation of loss functino for input pattern `$\boldsymbol{x}$`
`$$ L(c \mid \boldsymbol{x}) = \sum_{c' \in C} l(c, c') P(c' \mid \boldsymbol{x}) $$`
Determine that `$\boldsymbol{x}$` is in class `$c$` minimizing `$L$`.

+++
## Bayes' Theorem
`$$ P ( c \mid \boldsymbol{x} ) = \frac{p( \boldsymbol{x} \mid c ) P(c)}{ p(x) } $$`

+++ 
## Maximum A Posteriori (MAP)
Estimate class `$\hat{c}$` maximizing `$ P(c \mid \boldsymbol{x}) $`  
`\begin{align} \hat{c} &= \mathop{\rm arg~max}\limits_{c \in C} p(c \mid \boldsymbol{x}) \\ &= \mathop{\rm arg~max}\limits_{c \in C} p (\boldsymbol{x} \mid c) P(c) \\ &= \mathop{\rm arg~max}\limits_{c in C} \left\{ \log p (\boldsymbol{x} \mid c) + \log P(C) \right\} \end{align}`

+++
## Bayesian Error Rate
`$$ e_B (\boldsymbol{x}) = 1 - P(\hat{c} \mid \boldsymbol{x}) = \mathop{\rm min}\limits_{c \in C} \left\{ 1 - P(c \mid \boldsymbol{x}) \right\} $$`
`$$ e_B = \int \mathop{\rm min}\limits_{c \in C} \left\{ 1 - P(c \mid \boldsymbol{x}) \right\} p(\boldsymbol{x}) d\boldsymbol{x} $$`

+++
## Naive Bayes Method
Naive Bayes Method assumes that each element of `$\boldsymbol{x}$` is independet.
Here, probabilistic model is described as follows.
`$$ p(\boldsymbol{x} \mid c) = \prod_{i=1}^{d} p(x_i \mid c) $$`

+++
## Improved Naive Bayes Method
Improved Naive Bayes Method takes into account that elements of `$\boldsymbol{x}$` are not independent.  
Then this method compensate for positive correlation as follows.
`$$ \hat{c} = \mathop{\rm arg~max}\limits_{c} \prod_{i=1}^{d} {\hat{p} (x_i \mid c)}^{\alpha} \hat{P} (c) $$`
where `$\alpha$` is a hyper parameter.