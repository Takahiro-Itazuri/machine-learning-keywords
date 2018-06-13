## Least Squares Method
Least Squares Method minimizes the sum of square errors.<br>
Given `$ n $` samples `$ (\boldsymbol{x}_1, y_1), \cdots, (\boldsymbol{x}_n, y_n) $`<br>
`$$ \boldsymbol{X} = (\boldsymbol{x}_1, \boldsymbol{x}_2, \cdots, \boldsymbol{x}_n)^T $$`
`$$ \boldsymbol{y} = (y_1, y_2, \cdots, y_n)^T $$`
Least Squares Method can be formulated as follows:<br>
`$$ \boldsymbol{w} = \mathop{\rm arg~min}\limits_\boldsymbol{w} \frac{1}{2} \| \boldsymbol{Xw} - \boldsymbol{y} \|^2 $$`
`$$ \boldsymbol{w} = (\boldsymbol{X}^T \boldsymbol{X})^{-1} \boldsymbol{X}^T y $$`


