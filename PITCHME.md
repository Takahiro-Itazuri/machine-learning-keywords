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
  - Singular Value Decomposition

+++?include=Feature_Space/Normalization.md
+++?include=Feature_Space/Within-Class_Variance_and_Between-Class_Variance.md
+++?include=Feature_Space/PCA1.md
+++?include=Feature_Space/PCA2.md
+++?include=Feature_Space/PCA3.md
+++?include=Feature_Space/SVD.md

---
## Discriminant Function Based Method
- Linear Discriminant Function
  - Linearly Separable
  - Linear Discriminant Analysis (LDA)
  - Least Squares Method
  - Lasso Regression
  - Ridge Regression
- Kernel Method
  - Kernel Ridge Regression

+++?include=Discriminant_Function_Based_Method/DF.md
+++?include=Discriminant_Function_Based_Method/LDF.md
+++?include=Discriminant_Function_Based_Method/LDA.md
+++?include=Discriminant_Function_Based_Method/LS.md
+++?include=Discriminant_Function_Based_Method/LR.md
+++?include=Discriminant_Function_Based_Method/RR.md
+++?include=Discriminant_Function_Based_Method/KM.md 
+++?include=Discriminant_Function_Based_Method/KRR.md

---
## Probabilistic Model Based Method
- Bayes Discriminant Method
  - Bayes' Theorem
  - Maximum A Posteriori (MAP)
  - Bayesian Error Rate
  - Naive Bayes Method
  - Improved Naive Bayes Method

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
