# Shifted Schwefel

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

Custom algorithm.

We want to minimise f(x, n) where n is the dimension.  
For n = 1: f1 = f(x,1) = | x1-z1 | + fmin  
We can easily solve for x1 using a 1d search (for example Brent algorithm). We obtain x1* and fmin  
Next dimension: set x1 = x1*  
Then f2 = f(x,2) = max(|x1-z1|,|x2-z2|) + fmin = |x2-z2| + fmin since x1-z1 = 0  
we obtain x2 - z2 = +/- (f2 - fmin)  
we evaluate both possible solutions and pick the one that minimizes the f(x2), we obtain x2* and set x2 = x2*
And so on for each following dimension.

Algorith complexity: For dimension 1, 1d search on a convex function, so very quick.
For all other dimensions, 2 function evaluations for each dimension.

## Dimension 50

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-10.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 86

computational Time: 0.01 s


## Dimension 500

### Parameters

Stopping criterion: | f(xnew) - f(x) | < tol, with tol=1e-10.

### Results

Optimum found: -450 (known optimum -450)

number of function evaluations: 536

computational Time: 0.15 s

Nota: Given the nature of the algorithm, we cannot obtain convergence curves.
