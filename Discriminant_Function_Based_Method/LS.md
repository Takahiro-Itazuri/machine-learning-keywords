## Least Squares Method
Least Squares Method minimizes the sum of square errors.<br>
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf X} = ({\bf x}_1, {\bf x}_2, \cdots, {\bf x}_n)^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Least Squares Method can be formulated as follows:<br>
`$$ {\bf w} = \mathop{\rm arg~min}\limits_{\bf w} \frac{1}{2} \| {\bf Xw} - {\bf y} \|^2 $$`
`$$ {\bf w} = ({\bf X}^T {\bf X})^{-1} {\bf X}^T y $$`


