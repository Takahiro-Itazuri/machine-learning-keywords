## Kernel Ridge Regression
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{\Phi} = (\boldsymbol{\phi} (\boldsymbol{x}_1), \boldsymbol{\phi} (\boldsymbol{x}_2), \cdots, \boldsymbol{\phi} (\boldsymbol{x}_n) )^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression for `$ g(\boldsymbol{\phi} (\boldsymbol{x})) $` is given as follows:<br>
`$$ \boldsymbol{w} = \mathop{\rm arg~min}\limits_\boldsymbol{w} \frac{1}{2} {\| \boldsymbol{\Phi w} - \boldsymbol{y} \|}^{2} + \frac{\lambda}{2} {\| \boldsymbol{w} \|}^{2} $$`
`$$ \boldsymbol{\Phi}^T \left( \boldsymbol{\Phi} w - \boldsymbol{y} \right) + \lambda \boldsymbol{w} = \boldsymbol{0} $$`
`$$ \boldsymbol{w} = - \frac{1}{\lambda} \boldsymbol{\Phi}^T \left( \boldsymbol{\Phi w} - y \right) = \boldsymbol{\Phi}^T a $$`
`$$ \boldsymbol{a} = \mathop{\rm arg~min}\limits_\boldsymbol{a} \frac{1}{2} {\| \boldsymbol{\Phi} \boldsymbol{\Phi}^T \boldsymbol{a} - \boldsymbol{y} \|}^{2} + \frac{\lambda}{2} {\| \boldsymbol{\Phi}^T \boldsymbol{a} \|}^{2} $$`
`$$ \boldsymbol{a} = {\left( \boldsymbol{\Phi} \boldsymbol{\Phi}^T + \lambda \boldsymbol{I} \right)}^{-1} \boldsymbol{y} = {\left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)}^{-1} \boldsymbol{y} $$`
Therefore, `$ g(\boldsymbol{\phi} (\boldsymbol{x})) $` can be calculated without `$ \boldsymbol{\phi} $`<br>
`$$ g(\boldsymbol{\phi} (\boldsymbol{x})) = \boldsymbol{y}^T \left( \boldsymbol{G} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{k} (\boldsymbol{x}) $$`
where<br>
`$$ \boldsymbol{k} (\boldsymbol{x}) = \left( k(\boldsymbol{x}_1, \boldsymbol{x}), k(\boldsymbol{x}_2, \boldsymbol{x}), \cdots, k(\boldsymbol{x}_n, \boldsymbol{x}) \right)^T $$`


