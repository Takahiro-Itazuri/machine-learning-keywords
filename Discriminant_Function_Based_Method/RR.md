## Ridge Regression
Ridge Regression is Least Squares Method with L2 Regularization.<br>
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{X} = (\boldsymbol{x}_1, \boldsymbol{x}_2, \cdots, \boldsymbol{x}_n)^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression can be formulated as follows:<br>
`$$ \boldsymbol{w} = \mathop{\rm arg~min}\limits_\boldsymbol{w} \frac{1}{2} \| \boldsymbol{Xw} - \boldsymbol{y} \|^2 + \frac{\lambda}{2} \| \boldsymbol{w} \|^2 $$`
`$$ \boldsymbol{w} = \left( \boldsymbol{X}^T \boldsymbol{X} + \lambda \boldsymbol{I} \right)^{-1} \boldsymbol{X}^T \boldsymbol{y} $$`


