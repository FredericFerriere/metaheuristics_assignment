# Shifted Griewank

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

I chose conjugate gradient as the function has a quadratic lead term.

## Dimension 50

### Parameters

Stopping criterion: || gradient || < tol, with tol=1e-6 and infinity norm.

### Results

Optimum found: -180 (known optimum -180)

number of function evaluations: 404

computational Time: 0.08 s

convergence curve

![](convergenceCurve_dim_50.png)

## Dimension 500

### Parameters

Stopping criterion: || gradient || < tol, with tol=1e-6 and infinity norm.

### Results

Optimum found: -180 (known optimum -180)

number of function evaluations: 1001

computational Time: 5.02 s

convergence curve

![](convergenceCurve_dim_500.png)

### Calculating the number of function evaluations

The algorithm provides the number of iterations. The number of function evaluations is:  
(1 + 2 * dimension) * numberIterations  
since for each iteration and each dimension, gradient is numerically approximated.
