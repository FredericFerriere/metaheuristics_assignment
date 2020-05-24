# Shifted Ackley

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

Custom Algorithm.
We will optimise along each dimension independantly since we can separate the D dimensional optimisation into D 1-dimensional optimisations. The search space is [-32,32] along each dimension. The cos function creates many local optima in that space but we know the frequency so we can split the search space into 10 ranges [-32,-31], [-31,-30], ..., [31,32].  
For each subrange, run a brent optimisation to find a local minimum. The global minimum is the best solution amongst the 64 local minima we obtained.  Repeat this procedure for each dimension, keeping other values in the vector fixed. Note that the algorithm can be parallelised across dimensions and search space.

## Dimension 50

### Parameters

Stopping criterion: | x - xprev | < tol, with tol=1e-3 for each brent search in range [a, a+1].

### Results

Optimum found: -140 (known optimum -140)

number of function evaluations: 35,678

computational Time: 1.35 s

## Dimension 500

### Parameters

Stopping criterion: | x - xprev | < tol, with tol=1e-3 for each brent search in range [a, a+1].

### Results

Optimum found: -140 (known optimum -140)

number of function evaluations: 491,073

computational Time: 25.6 s

Nota: Given the nature of the algorithm, we cannot obtain convergence curves.

### Calculating the number of function evaluations

No calculation needed, the algorithm already returns the number of function evaluations rather than the number of iterations.
