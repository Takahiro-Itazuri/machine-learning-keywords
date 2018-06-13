## Ridge Regression
Ridge Regression is Least Squares Method with L2 Regularization.<br>
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf X} = ({\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n)^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Ridge Regression can be formulated as follows:<br>
`$$ {\bf w} = \mathop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf Xw} - {\bf y} \|^2 + \lambda \| {\bf w} \|^2 $$`
`$$ {\bf w} = \left( {\bf X}^T {\bf X} + \lambda {\bf I} \right)^{-1} {\bf X}^T {\bf y} $$`


