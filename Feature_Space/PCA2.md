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


