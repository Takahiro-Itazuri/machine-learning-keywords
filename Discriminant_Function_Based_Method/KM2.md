## Kernel Methods

Linear Discriminant Model can be reformulated by using Kernel Function `$\kappa$`  as follows:<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{a}^T \boldsymbol{\Phi} \boldsymbol{\phi}(\boldsymbol{x}) = \sum_{i=1}^{n} a_i \kappa (\boldsymbol{x_i}, \boldsymbol{x}) $$`
Finally, all of terms containing `$ \boldsymbol{\phi} $` are given the form of `$ \boldsymbol{\Phi} \boldsymbol{\Phi}^T $` and `$ G = \boldsymbol{\Phi} \boldsymbol{\Phi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ \boldsymbol{\Phi} \boldsymbol{\Phi}^T = \begin{bmatrix} \kappa (\boldsymbol{x}_1, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_n) \\  \kappa (\boldsymbol{x}_2, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ \kappa (\boldsymbol{x}_n, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_n) \end{bmatrix} $$`

