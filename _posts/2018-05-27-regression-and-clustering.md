### Day 7

**ridge regression, LASSO regression**: ridge use l2 norm, LASSO use l1 and have built-in feature selection

**k means**: 1. assign (closest centroid) 2. optimize (ck is kth centroid, min SSE, aSSE/ack=0, ck=mean(xi))

optimize: 1. bisecting k means: all are one cluster at first; use k=2 means to break each one and calculate the overall min SSE, and choose to break that cluster; iterate to make k=k(expected) 2. mini batch k means: only use some samples to get the optimized centroid

**expectation maximization algorithm**: 

1. MLE(maximum likelihood estimate): (model with unknow params, samples) -> (model params)

2. Jensen's inequality: if f is convex, then E[f(X)] >= f(E(X)]


<https://blog.csdn.net/daunxx/article/details/51578787> ridge regression

<https://blog.csdn.net/taoyanqi8932/article/details/53727841> k means

<https://blog.csdn.net/zhihua_oba/article/details/73776553> expectation maximization algorithm

<https://blog.csdn.net/u012500237/article/details/65437525> hierarchial clustering
