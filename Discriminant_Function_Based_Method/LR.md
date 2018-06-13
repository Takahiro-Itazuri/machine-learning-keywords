## Lasso Regression
Lasso Regression is Least Squares Method with L1 Regularization.<br>
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{X} = (\boldsymbol{x}_1, \boldsymbol{x}_2, \cdots, \boldsymbol{x}_n)^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Lasso Regression can be formulated as follows:<br>
`$$ \boldsymbol{w} = \mathop{\rm arg~min}\limits_\boldsymbol{w} \frac{1}{2} \| \boldsymbol{Xw} - \boldsymbol{y} \|^2 + \lambda | \boldsymbol{w} | $$`
Lasso Regression cannot be solved analytically.


