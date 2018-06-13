## Kernel Ridge Regression

Linear Discriminant Model can be reformulated by using Kernel Function `$\kappa$`  as follows:<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{a}^T \boldsymbol{\Phi} \boldsymbol{\phi}(\boldsymbol{x}) = \sum_{i=1}^{n} a_i \kappa (\boldsymbol{x_i}, \boldsymbol{x}) $$`
We define `$ G = \boldsymbol{\Phi} \boldsymbol{\Phi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ \boldsymbol{\Phi} \boldsymbol{\Phi}^T = \begin{bmatrix} \kappa (\boldsymbol{x}_1, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_n) \\  \kappa (\boldsymbol{x}_2, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ \kappa (\boldsymbol{x}_n, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_n) \end{bmatrix} $$`
By using this Gram matrix, `$\boldsymbol{a}$` can be calculated as follows:<br>
`\begin{align} \boldsymbol{a} = \left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{y} \end{align}`
Therefore, `$ g(\boldsymbol{\phi} (\boldsymbol{x})) $` can be calculated without `$ \boldsymbol{\phi} $`<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x})) = \boldsymbol{y}^T \left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{k} (\boldsymbol{x}) $$`
where<br>
`$$ \boldsymbol{k} (\boldsymbol{x}) = \left( \kappa (\boldsymbol{x}_1, \boldsymbol{x}), \kappa (\boldsymbol{x}_2, \boldsymbol{x}), \cdots, \kappa (\boldsymbol{x}_n, \boldsymbol{x}) \right)^T $$`
 
