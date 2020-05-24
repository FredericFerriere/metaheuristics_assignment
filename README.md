# metaheuristics_assignment

Summary of Results

|  Problem  |  Known Optimum  |  Optimum Found  | RunTime |   Number of function evaluations  |
|  ---  |  ---  |  ---  |  ---  |  ---  |
|  Djibouti38  |  6656  |  6659  |  1.45s |  31,758   |
|  Qatar194  |  9352  |  10547  |  41.1s |  224,466   |
|  ShiftedSphere_50  |  -450  |  -450  |  0.01 s |  303  |
|  ShiftedSphere_500  |  -450  |  -449.99  |  0.05 s |  3,003  |
|  ShiftedSchwefel_50  |  -450  |  -450  |  0.03 s |  3,090   |
|  ShiftedSchwefel_500  |  -450  |  -450  |  0.41 s |  31,515   |
|  ShiftedRosenbrock_50  |  390  |  390  |  0.69 s |  67,569   |
|  ShiftedRosenbrock_500  |  390  |  390.01  |  72.5 s |  5,643,638   |
|  ShiftedRastrigin_50  |  -330  |  -330  |  0.14 s |  4,067   |
|  ShiftedRastrigin_500  |  -330  |  -330  |  1.94 s |  41,250   |
|  ShiftedGriewank_50  |  -180  |  -180  |  0.08 s |  404   |
|  ShiftedGriewank_500  |  -180  |  -180  |  5.02 s |  1,001   |
|  ShiftedAckley_50  |  -140  |  -140  |  1.35 s |  35,678   |
|  ShiftedAckley_500  |  -140  |  -140  |  25.6 s |  491,073   |

Shifted functions all use gradient type algorithms. As such, and since no gradient function is provided, gradients are numerically evaluated. Scikitlearn optimizer sometimes provides the number of iterations rather than the number of function evaluations. In this case, I've assumed centered gradient calculations, ie 2 function evaluations per dimension per iteration.
