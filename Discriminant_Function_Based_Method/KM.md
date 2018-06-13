## Kernel Methods
Linear Discriminant Model<br>
`$$ g({\bf \phi} ({\bf x}) ) = {\bf w}^T {\bf \phi} ({\bf x}) $$`
Kernel Function<br>
`$$ k({bf x}, {\bf x'}) = {\bf \psi} ({\bf x})^T {\bf \psi} ({\bf x'})^T $$`
Given `$ n $` samples `$ ({\bf x}_1, y_1), \cdots, ({\bf x}_n, y_n) $`<br>
`$$ {\bf \Psi} = ({\bf \psi} ({\bf x}_1), {\bf \psi} ({\bf x}_2), \cdots, {\bf \psi} ({\bf x}_n) )^T $$`
`$$ {\bf y} = (y_1, y_2, \cdots, y_n)^T $$`
Regression problem can be reformulated as follows:<br>
`$$ {\bf w} = {\bf \Psi}^T {\bf a} $$`
`$$ g({\bf \psi} ({\bf x}) ) = {\bf a}^T {\bf \Psi} {\bf \psi}({\bf x}) = \sum_{i=1}^{n} a_i k({\bf x_i}, {\bf x}) $$`
Finally, all of terms containing `$ {\bf \psi} $` are given the form of `$ {\bf \Psi} {\bf \Psi}^T $` and `$ G = {\bf \Psi} {\bf \Psi}^T $`, called Gram Matrix, is given as follows:<br>
`$$ {\bf \Psi} {\bf \Psi}^T = \begin{bmatrix} k({\bf x}_1, {\bf x}_1) & k({\bf x}_1, {\bf x}_2) & \cdots & k({\bf x}_1, {\bf x}_n) \\  k({\bf x}_2, {\bf x}_1) & k({\bf x}_2, {\bf x}_2) & \cdots & k({\bf x}_2, {\bf x}_n) \\ \vdots & \vdots & \ddots & \vdots \\ k({\bf x}_n, {\bf x}_1) & k({\bf x}_n, {\bf x}_2) & \cdots & k({\bf x}_n, {\bf x}_n) \end{bmatrix} $$`


