### Day 7

**ridge regression, LASSO regression**: ridge use l2 norm, LASSO use l1 and have built-in feature selection

**k means**: 1. assign (closest centroid) 2. optimize (ck is kth centroid, min SSE, aSSE/ack=0, ck=mean(xi))

optimize: 1. bisecting k means: all are one cluster at first; use k=2 means to break each one and calculate the overall min SSE, and choose to break that cluster; iterate to make k=k(expected) 2. mini batch k means: only use some samples to get the optimized centroid

**expectation maximization algorithm**: 

1. MLE(maximum likelihood estimate): (model with unknown params, samples) -> (model params)

2. Jensen's inequality: if f is convex, then E[f(X)] >= f(E(X)], and only when X is contant, the equality happens

3. EM algo: (multi model with unknown params, samples, priorer) -> (classification, model params) iterative

logL(theta) = sum(log(p(xi;theta)) from MLE = sum(log(sum(z,p(xi,zj;theta))) = sum(log(sum(z,Qi(zj) * p(xi,zj;theta) / Qi(zj)) >=sum(sum(n,z,Qi(zj) log(p(xi,zj;theta)/Qi(zj)) )) from jensen's inequality where sumQi(zj) is Expectation, and log is concave

Qi(zj) can take any function st. sum(z,Qi(zj))=1, but to make the lower bound max, we want log(p(xi,zj;theta)/Qi(zj)) to be const, which means p(xi,zj;theta)/Qi(zj) is const c, since sum(z,Qi(zj))=1, sum(z,p(xi,zj;theta))=c, p(xi;theta)=c, Qi(zj)=p(xi,zj;theta)/c=p(xi,zj;theta)/p(xi;theta)=p(zj|xi;theta) postier

E: Qi(zj)=postier from priorer(known) and likelihood(from theta we get from laster iteration)

M: theta=argmax(theta, sum(sum(n,z, Qi(zj) log(p(xi,zj;theta)/Qi(zj)) )) )

p(xi,zj;theta)/Qi(zj)=p(xi;theta)

k means used the thought of EM algo

**hierarchial clustering**: top down or bottom up

top down: all same cluster at first; for each cluster, get furtherest two points, and separate; repeat until k reached or min dist reached(cannot separate)

bottom up: used most. all points in diff clusters at first; get dist of each two clusters(max points, min points, avg dist, mid dist, centroid dist) and find the closest two cluster to merge; repeat until k reached or dist reached(cannot merge)

<https://blog.csdn.net/daunxx/article/details/51578787> ridge regression

<https://blog.csdn.net/taoyanqi8932/article/details/53727841> k means

<https://blog.csdn.net/zhihua_oba/article/details/73776553> expectation maximization algorithm

<https://blog.csdn.net/u012500237/article/details/65437525> hierarchial clustering
