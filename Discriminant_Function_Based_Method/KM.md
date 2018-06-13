## Kernel Methods

Linear Discriminant Model<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{w}^T \boldsymbol{\phi} (\boldsymbol{x}) $$`
Kernel Function<br>
`$$ \kappa (\boldsymbol{x}, \boldsymbol{x'}) = \boldsymbol{\phi} (\boldsymbol{x})^T \boldsymbol{\phi} (\boldsymbol{x'}) $$`
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{\Phi} = (\boldsymbol{\phi} (\boldsymbol{x}_1), \boldsymbol{\phi} (\boldsymbol{x}_2), \cdots, \boldsymbol{\phi} (\boldsymbol{x}_n) )^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Regression problem can be reformulated as follows:<br>
`$$ \boldsymbol{w} = \boldsymbol{\Phi}^T \boldsymbol{a} $$`
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{a}^T \boldsymbol{\Phi} \boldsymbol{\phi}(\boldsymbol{x}) = \sum_{i=1}^{n} a_i \kappa (\boldsymbol{x_i}, \boldsymbol{x}) $$`
Finally, all of terms containing `$ \boldsymbol{\phi} $` are given the form of `$ \boldsymbol{\Phi} \boldsymbol{\Phi}^T $` and `$ G = \boldsymbol{\Phi} \boldsymbol{\Phi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ \boldsymbol{\Phi} \boldsymbol{\Phi}^T = \begin{bmatrix} \kappa (\boldsymbol{x}_1, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_1, \boldsymbol{x}_n) \\  \kappa (\boldsymbol{x}_2, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_2, \boldsymbol{x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ \kappa (\boldsymbol{x}_n, \boldsymbol{x}_1) & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_2) & \cdots & \kappa (\boldsymbol{x}_n, \boldsymbol{x}_n) \end{bmatrix} $$`

