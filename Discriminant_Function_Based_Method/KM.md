## Kernel Methods

Linear Discriminant Model<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{w}^T \boldsymbol{\phi} (\boldsymbol{x}) $$`
Kernel Function<br>
`$$ k({bf x}, \boldsymbol{x'}) = \boldsymbol{\psi} (\boldsymbol{x})^T \boldsymbol{\psi} (\boldsymbol{x'})^T $$`
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{\Psi} = (\boldsymbol{\psi} (\boldsymbol{x}_1), \boldsymbol{\psi} (\boldsymbol{x}_2), \cdots, \boldsymbol{\psi} (\boldsymbol{x}_n) )^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Regression problem can be reformulated as follows:<br>
`$$ \boldsymbol{w} = \boldsymbol{\Psi}^T \boldsymbol{a} $$`
`$$ g(\boldsymbol{\psi} (\boldsymbol{x}) ) = \boldsymbol{a}^T \boldsymbol{\Psi} \boldsymbol{\psi}(\boldsymbol{x}) = \sum_{i=1}^{n} a_i k(\boldsymbol{x_i}, \boldsymbol{x}) $$`
Finally, all of terms containing `$ \boldsymbol{\psi} $` are given the form of `$ \boldsymbol{\Psi} \boldsymbol{\Psi}^T $` and `$ G = \boldsymbol{\Psi} \boldsymbol{\Psi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ \boldsymbol{\Psi} \boldsymbol{\Psi}^T = \begin{bmatrix} k(\boldsymbol{x}_1, \boldsymbol{x}_1) & k(\boldsymbol{x}_1, \boldsymbol{x}_2) & \cdots & k(\boldsymbol{x}_1, \boldsymbol{x}_n) \\  k(\boldsymbol{x}_2, \boldsymbol{x}_1) & k(\boldsymbol{x}_2, \boldsymbol{x}_2) & \cdots & k(\boldsymbol{x}_2, \boldsymbol{x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ k(\boldsymbol{x}_n, \boldsymbol{x}_1) & k(\boldsymbol{x}_n, \boldsymbol{x}_2) & \cdots & k(\boldsymbol{x}_n, \boldsymbol{x}_n) \end{bmatrix} $$`

