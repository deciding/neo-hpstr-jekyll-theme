###Day1

Reinforcement learning: bellman optimization condition(DP), delta rule(gradient descent), tempral difference learning, q learning

hypothesis sets, empirical error, true error, complexity of hypotheses sets, regularization(LASSO,Decision Tree, GD), bias-variance trade-off, loss functions, target function, hypothesis function(objective function), cross-validation


###Day2

Convex optimization(Fermat theory, derivative is 0), Lagrangian multiplier, Primal-dual problems(minmax-maxmin), Gradients & subgradients(for non-differentiable), ℓ1(Least Absolute Error) and ℓ2(Least Squred Error) regularized objective functions


non-constrained min

constrained equality(lagrangian multiplier)

constrained inequality(KKT, u>=0, f'-sum(g')=0, sum(ug(x*))=0, it is just maxmin)


Batch gradient descent & stochastic gradient descent, Coordinate gradient descent

https://www.zhihu.com/question/58584814 duality

https://www.quora.com/Why-small-l1-norm-means-sparsity/answer/Prasoon-Goyal l1 sparsity

https://www.cnblogs.com/pinard/p/5970503.html GD

https://blog.csdn.net/lansatiankongxxc/article/details/46386341 subgradient


###Day3

logistic regression: not regression, use (0,1) sigmoid to model classification as Linear regression, but since loss function is not convex, we don't use GD directly. instead of get min of non-convex loss function, we use MLE(min likelihood estimate) to get max of all sample possiblity(likelihood function). we use Gradient Ascdent at this point.

https://blog.csdn.net/w401229755/article/details/51712581 logistic regression
