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


