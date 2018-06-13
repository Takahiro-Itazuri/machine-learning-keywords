## Kernel Ridge Regression
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{\Psi} = (\boldsymbol{\psi} (\boldsymbol{x}_1), \boldsymbol{\psi} (\boldsymbol{x}_2), \cdots, \boldsymbol{\psi} (\boldsymbol{x}_n) )^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression for `$ g(\boldsymbol{\psi} (\boldsymbol{x})) $` is given as follows:<br>
`$$ \boldsymbol{w} = \mathop{\rm arg~min}\limits_\boldsymbol{w} \frac{1}{2} {\| \boldsymbol{\Psi w} - \boldsymbol{y} \|}^{2} + \frac{\lambda}{2} {\| \boldsymbol{w} \|}^{2} $$`
`$$ \boldsymbol{\Psi}^T \left( \boldsymbol{\Psi} w - \boldsymbol{y} \right) + \lambda \boldsymbol{w} = \boldsymbol{0} $$`
`$$ \boldsymbol{w} = - \frac{1}{\lambda} \boldsymbol{\Psi}^T \left( \boldsymbol{\Psi w} - y \right) = \boldsymbol{\Psi}^T a $$`
`$$ \boldsymbol{a} = \mathop{\rm arg~min}\limits_\boldsymbol{a} \frac{1}{2} {\| \boldsymbol{\Psi} \boldsymbol{\Psi}^T \boldsymbol{a} - \boldsymbol{y} \|}^{2} + \frac{\lambda}{2} {\| \boldsymbol{\Psi}^T \boldsymbol{a} \|}^{2} $$`
`$$ \boldsymbol{a} = {\left( \boldsymbol{\Psi} \boldsymbol{\Psi}^T + \lambda \boldsymbol{I} \right)}^{-1} \boldsymbol{y} = {\left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)}^{-1} \boldsymbol{y} $$`
Therefore, `$ g(\boldsymbol{\psi} (\boldsymbol{x})) $` can be calculated without `$ \boldsymbol{\psi} $`<br>
`$$ g(\boldsymbol{\psi} (\boldsymbol{x})) = \boldsymbol{y}^T \left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{k} (\boldsymbol{x}) $$`
where<br>
`$$ \boldsymbol{k} (\boldsymbol{x}) = \left( k(\boldsymbol{x}_1, \boldsymbol{x}), k(\boldsymbol{x}_2, \boldsymbol{x}), \cdots, k(\boldsymbol{x}_n, \boldsymbol{x}) \right)^T $$`


