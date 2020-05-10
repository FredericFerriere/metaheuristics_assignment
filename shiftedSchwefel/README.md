# Shifted Schwefel

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

Custom algorithm.

Focus in first dimension to start with. We can use a simple 1d search algorithm (brent) and optimise along this dimension to find x1*.  
Plug x1* into the solution vector, freeze this value for dimension 1 and use the same algorithm to find the optimum for dimension 2, x2*.  Use the same procedure iteravely for all subsequent dimensions.

Algorith complexity: For each dimension 1, the function is convex, so very quick.

## Dimension 50

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-6.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 1030

computational Time: 0.05 s


## Dimension 500

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-6.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 10505

computational Time: 1.02 s

Nota: Given the nature of the algorithm, we cannot obtain convergence curves.
