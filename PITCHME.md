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
## Principal Component Analysis (PCA)
Here, `$\hat{d}$` dimensional subspace is an orthogonal basis spanned by base vectors `$\boldsymbol{u}_1, \boldsymbol{u}_2, \cdots, \boldsymbol{u}_{\hat{d}}$`.  
Point `$\hat{\boldsymbol{x}}$` is mapped into this `$\hat{d}$` dimensional subspace.
`\begin{align} 
  \hat{\boldsymbol{x}} &= (\boldsymbol{u}_1^T \boldsymbol{x}) \boldsymbol{u}_1 + (\boldsymbol{u}_2^T \boldsymbol{x}) \boldsymbol{u}_2 + \cdots + (\boldsymbol{u}_{\hat{d}}^T \boldsymbol{x}) \boldsymbol{u}_{\hat{d}} \\ 
  &= \left( \boldsymbol{u}_1 \boldsymbol{u}_1^T + \boldsymbol{u}_2 \boldsymbol{u}_2^T + \cdots + \boldsymbol{u}_{\hat{d}} \boldsymbol{u}_{\hat{d}}^T \right) \\
  &= \boldsymbol{A} \boldsymbol{A}^T \boldsymbol{x}
 \end{align}`
where
`\begin{align}
  \boldsymbol{A} = \begin{pmatrix} \boldsymbol{u}_1 & \boldsymbol{u}_2 & \cdots & \boldsymbol{u}_{\hat{d}} \end{pmatrix}
 \end{align}`

+++
## PCA (Variance Maximization)
Consider 1-dimensional subspace mapped by a base vector `$\boldsymbol{u}$`.  
Average vector in subspace
`$$ \hat{\boldsymbol{x}} = \frac{1}{n} \sum_{p=1}^{n} \boldsymbol{u}^T \boldsymbol{x}_p = \boldsymbol{u}^T \bar{\boldsymbol{x}} $$`
Variance in subspace
`$$ \hat{\boldsymbol{\Sigma}} = \frac{1}{n} \sum_{p=1}^{n} \left( \boldsymbol{u}^T \boldsymbol{x}_p - \boldsymbol{u}^T \hat{\boldsymbol{x}} \right) \left( \boldsymbol{u}^T \boldsymbol{x}_p - \boldsymbol{u}^T \hat{\boldsymbol{x}} \right)^T = \boldsymbol{u}^T \Sigma \boldsymbol{u} $$`

Then maximize this variance. This is calculated by method of Lagrange multiplier.  
`$$ \boldsymbol{u}^T \boldsymbol{\Sigma} \boldsymbol{u} + \lambda (1 - \boldsymbol{u}^T \boldsymbol{u}) $$`
Differentiate this with respect with `$\boldsymbol{u}$`
`\begin{align} 
  \boldsymbol{\Sigma} \boldsymbol{u} &= \lambda \boldsymbol{u} \\
  \boldsymbol{u}^T \boldsymbol{\Sigma} \boldsymbol{u} &= \lambda
 \end{align}`

From above, determine that `$\boldsymbol{u}$` is the eigenvector corresponding maximum eigenvalue `$\lambda$`. Further components are found successively by the same process.

+++
## PCA (Squared Error Minimization)

+++
## Singular Value Decomposition (SVD)

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

+++
## Discriminant Function
Given a function `$ g_1 (\boldsymbol{x}), g_2 (\boldsymbol{x}), \cdots, g_1 (\boldsymbol{x}) $` for each class`$ c_1, c_2, \cdots, c_M $`<br>
`$$ \hat{c} = \mathop{\rm arg~max}\limits_{c_i \in C} g_i (\boldsymbol{x}) $$`

+++
## Linear Discriminant Function
Linear Discriminant Function (for class `$ c_i $`) <br>
`$$ g_i (\boldsymbol{x}) = \boldsymbol{w}_i^T \boldsymbol{x} $$`
where<br>
`\begin{align} \boldsymbol{x} &= \begin{pmatrix} 1 & \boldsymbol{x}^T \end{pmatrix}^T = \begin{pmatrix} 1 & x_1 & x_2 & \cdots & x_d \end{pmatrix}^T \\ \boldsymbol{w} &= \begin{pmatrix} w_0 & w_1 & w_2 & \cdots & w_d \end{pmatrix} \end{align}`

+++
## Linear Discriminant Analysis (LDA)

+++
## Least Squares Method
Least Squares Method minimizes the sum of square errors.<br>
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf X} = ({\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n)^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Least Squares Method can be formulated as follows:<br>
`$$ {\bf w} = \mathop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf Xw} - {\bf y} \|^2 $$`
`$$ {\bf w} = ({\bf X}^T {\bf X})^{-1} {\bf X}^T y $$`

+++
## Lasso Regression
Lasso Regression is Least Squares Method with L1 Regularization.<br>
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf X} = ({\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n)^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Lasso Regression can be formulated as follows:<br>
`$$ {\bf w} = \mathop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf Xw} - {\bf y} \|^2 + \lambda | {\bf w} | $$`
Lasso Regression cannot be solved analytically.

+++
## Ridge Regression
Ridge Regression is Least Squares Method with L2 Regularization.<br>
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf X} = ({\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n)^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression can be formulated as follows:<br>
`$$ {\bf w} = \mathop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf Xw} - {\bf y} \|^2 + \lambda \| {\bf w} \|^2 $$`
`$$ {\bf w} = \left( {\bf X}^T {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^T {\bf y} $$`

+++ 
## Kernel Methods
Linear Discriminant Model<br>
`$$ g({\bf \phi} ({\bf x}) ) = {\bf w}^T {\bf \phi} ({\bf x}) $$`
Kernel Function<br>
`$$ k({bf x}, {\bf x'}) = {\bf \psi} ({\bf x})^T {\bf \psi} ({\bf x'})^T $$`
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf \Psi} = ({\bf \psi} ({\bf x}_1), {\bf \psi} ({\bf x}_2), \cdots, {\bf \psi} ({\bf x}_n) )^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Regression problem can be reformulated as follows:<br>
`$$ {\bf w} = {\bf \Psi}^T {\bf a} $$`
`$$ g({\bf \psi} ({\bf x}) ) = {\bf a}^T {\bf \Psi} {\bf \psi}({\bf x}) = \sum_{i=1}^{n} a_i k({\bf x_i}, {\bf x}) $$`
Finally, all of terms containing `$ {\bf \psi} $` are given the form of `$ {\bf \Psi} {\bf \Psi}^T $` and `$ G = {\bf \Psi} {\bf \Psi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ {\bf \Psi} {\bf \Psi}^T = \begin{bmatrix} k({\bf x}_1, {\bf x}_1) & k({\bf x}_1, {\bf x}_2) & \cdots & k({\bf x}_1, {\bf x}_n) \\  k({\bf x}_2, {\bf x}_1) & k({\bf x}_2, {\bf x}_2) & \cdots & k({\bf x}_2, {\bf x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ k({\bf x}_n, {\bf x}_1) & k({\bf x}_n, {\bf x}_2) & \cdots & k({\bf x}_n, {\bf x}_n) \end{bmatrix} $$`

+++
## Kernel Ridge Regression
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf \Psi} = ({\bf \psi} ({\bf x}_1), {\bf \psi} ({\bf x}_2), \cdots, {\bf \psi} ({\bf x}_n) )^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression for `$ g({\bf \psi} ({\bf x})) $` is given as follows:<br>
`$$ {\bf w} = \methop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf \Psi w} - {\bf y} \|^2 + \frac{\lambda}{2} \| {\bf w} \|^2  $$`
`$$ {\bf \Psi}^T \left( {\bf \Psi} w - {\bf y} \right) + \lambda {\bf w} = {\bf 0} $$`
`$$ {\bf w} = - \frac{1}{\lambda} {\bf \Psi}^T \left( {\bf \Psi w} - y \right) = {\bf \Psi}^T a $$`

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
