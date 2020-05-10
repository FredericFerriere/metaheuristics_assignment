# Shifted Rastrigin

## How to run the code

The notebook is self contained:
* The function to optimise is implemented in the file functionToOptimise.py  
* Libraries needed: numpy, scipy

## Algorithm

Custom Algorithm.
We will optimise along each dimension independantly since we can separate the D dimensional optimisation into D 1-dimensional optimisations. The search space is [-5,5] along each dimension. The cos function creates many local optima in that space but we know the frequency so we can split the search space into 10 ranges [-5,-4], [-4,-3], ..., [4,5].  
For each subrange, run a brent optimisation to find a local minimum. The global minimum is the best solution amongst the 10 local minima we obtained.  Repeat this procedure for each dimension, keeping other values in the vector fixed. Note that the algorithm can be parallelised across dimensions and search space.

## Dimension 50

### Parameters

Stopping criterion: | x - xprev | < tol, with tol=1e-3 for each brent search in range [a, a+1].

### Results

Optimum found: -330 (known optimum -330)

number of function evaluations: 4067

computational Time: 0.31 s

## Dimension 500

### Parameters

Stopping criterion: | x - xprev | < tol, with tol=1e-3 for each brent search in range [a, a+1].

### Results

Optimum found: -330 (known optimum -330)

number of function evaluations: 41250

computational Time: 5.05 s

Nota: Given the nature of the algorithm, we cannot obtain convergence curves.
