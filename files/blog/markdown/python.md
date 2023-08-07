---
output:
  pdf_document: default
  html_document: default
header-includes: \usepackage{graphicx}
---

# Tips and tricks for machine learning experiments
## with examples in python Numpy and Scipy packages




### Sanity check of gradients in python
Computing gradients, and even more Hessians, is very tedious but worth the effort. Symbolic computation with Sympy may come in handy. You may also find the matrix cookbook (https://www.math.uwaterloo.ca/~hwolkowi/matrixcookbook.pdf) is useful.

A very common source of optimization not converging well is human error in the computation of the gradient. You can use scipy.optimize.check_grad() to check that your gradient is correct. It returns the norm of the different between the gradient given, and a gradient computed numerically:

```{python}
optimize.check_grad(f, jacobian, [2, -1])
```

See also ```scipy.optimize.approx_fprime()``` to find your errors.



### Einstein's Sum
np.einsum


### Miscs

1. logsumexp
2. log of determinant: write it as the sum of log of eigenvalues
3. 
