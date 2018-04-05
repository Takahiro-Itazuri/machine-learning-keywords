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
Determine class `$c$` maximizing `$ P(c \mid \boldsymbol{x}) $`
`\begin{align} \hat{c} &= \mathop{\rm arg~max}\limits_{c \in C} p(c \mid \boldsymbol{x}) \\ &= \mathop{\rm arg~max}\limits_{c \in C} p (\boldsymbol{x} \mid c) P(c) \\ &= \mathop{\rm arg~max}\limits_{c in C} \left{ \log p (\boldsymbol{x} \mid c) + \log P(C) \right} \end{align}`