# Shifted Schwefel

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

Custom algorithm.

Focus on first dimension to start with. We can use a simple 1d search algorithm (brent) and optimise along this dimension to find x1*.  
Plug x1* into the solution vector, freeze this value for dimension 1 and use the same algorithm to find the optimum for dimension 2, x2*.  Use the same procedure iteratively for all subsequent dimensions.

Algorith complexity: For each dimension 1, the function is convex, so very quick.

## Dimension 50

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-6.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 3,090

computational Time: 0.03 s


## Dimension 500

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-6.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 31,515

computational Time: 0.41 s

Nota: Given the nature of the algorithm, we cannot obtain convergence curves.

### Calculating the number of function evaluations

The algorithm provides the number of iterations. The number of function evaluations is:  
3 * numberIterations  
Indeed, we transform the d-dimensional problem into d 1-dimensional problems. So gradient calculation at each iteration only involves 1 dimension.
