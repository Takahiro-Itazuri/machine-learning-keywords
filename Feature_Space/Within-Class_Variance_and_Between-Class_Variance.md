## Within-Class Variance and Between-Class Variance
Average Vector  
`$$ \bar{\boldsymbol{x}}_i = \frac{1}{n_i} \sum_{\boldsymbol{x}_p \in C_i} \boldsymbol{x}_p $$`
Variance
`$$ V_i = \frac{1}{n_i} \sum_{\boldsymbol{x}_p \in C_i} \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)^T \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)$$`
Within-Class Variance
`$$ V_w = \frac{1}{n} \sum_{i=1}^{M} \sum_{\boldsymbol{x}_p \in C_i} \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right)^T \left( \boldsymbol{x}_p - \bar{\boldsymbol{x}}_i \right) $$`
Between-Class Variance
`$$ V_b = \frac{1}{n} \sum_{i=1}^{M} n_i \left( \bar{\boldsymbol{x]}_i - \bar{\boldsymbol{x}}} \right)^T \left( \bar{\boldsymbol{x]}_i - \bar{\boldsymbol{x}}} \right) $$`


