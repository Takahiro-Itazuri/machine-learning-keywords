## Kernel Ridge Regression

Linear Discriminant Model<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x}) ) = \boldsymbol{w}^T \boldsymbol{\phi} (\boldsymbol{x}) $$`
Kernel Function<br>
`$$ \kappa (\boldsymbol{x}, \boldsymbol{x'}) = \boldsymbol{\phi} (\boldsymbol{x})^T \boldsymbol{\phi} (\boldsymbol{x'}) $$`
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{\Phi} = (\boldsymbol{\phi} (\boldsymbol{x}_1), \boldsymbol{\phi} (\boldsymbol{x}_2), \cdots, \boldsymbol{\phi} (\boldsymbol{x}_n) )^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Solution of normal ridge regression problem is given as follows:<br>
`\begin{align} \boldsymbolw} = \left( \boldsymbol\Phi}^{T} \boldsymbol\Phi} + \lambda \boldsymbolI} \right)^{-1} \boldsymbol\Phi}^{T} \boldsymboly} \end{align}`
This equation can be reformulated as follows:<br>
`\begin{align} \boldsymbol{\Phi}^{T} \left( \boldsymbol{\Phi} \boldsymbol{w} - \boldsymbol{y} \right) + \lambda \boldsymbol{w} = \boldsymbol{0} \\ \boldsymbol{w} = - \frac{1}{\lambda} \boldsymbol{\Phi}^{T} \left( \boldsymbol{\Phi} \boldsymbol{w} - \boldsymbol{y} \right) \end{align}`
Here, we define `$ \boldsymbol{a} = - \frac{1}{\lambda} \left( \boldsymbol{\Phi} \boldsymbol{w} - \boldsymbol{y} \right) $`, and then we get the next equation.<br>
`$$ \boldsymbol{w} = \boldsymbol{\Phi}^T \boldsymbol{a} $$`

