### Day1

<https://www.quora.com/Where-do-I-learn-Machine-Learning>

<https://www.quora.com/How-do-I-learn-Machine-Learning-in-10-days>

<http://aima.cs.berkeley.edu/index.html>

**Reinforcement learning**: bellman optimization condition(DP), delta rule(gradient descent), tempral difference learning, q learning

hypothesis sets, empirical error, true error

complexity of hypotheses sets, **regularization**(LASSO,Decision Tree, GD)

bias-variance trade-off, loss functions, target function, hypothesis function(objective function), cross-validation

<https://www.zhihu.com/question/41775291> reinforcement learning


### Day2

Convex optimization(Fermat theory, derivative is 0), Lagrangian multiplier, **Primal-dual problems**(minmax-maxmin), Gradients & subgradients(for non-differentiable), ℓ1(Least Absolute Error) and ℓ2(Least Squred Error) regularized objective functions


1. non-constrained min

2. constrained equality(lagrangian multiplier)

3. constrained inequality(KKT, u>=0, aL/ax=0, sum(ug(x*))=0, it is just maxmin)

1. use logic to approach maxmin

2. use geometry to approach KKT then approach maxmin


Batch gradient descent & stochastic gradient descent, Coordinate gradient descent

<https://www.zhihu.com/question/58584814> duality

<http://www.chioka.in/differences-between-l1-and-l2-as-loss-function-and-regularization/> l1 and l2 norm

<https://www.quora.com/Why-small-l1-norm-means-sparsity/answer/Prasoon-Goyal> l1 sparsity

<https://www.cnblogs.com/pinard/p/5970503.html> GD

<https://blog.csdn.net/lansatiankongxxc/article/details/46386341> subgradient


### Day3

logistic regression: not regression, use (0,1) **sigmoid** to model classification as Linear regression, but since loss function is not convex, we don't use GD directly. instead of get min of non-convex loss function, we use **MLE**(min likelihood estimate) to get max of all sample possiblity(likelihood function). we use Gradient Ascdent at this point.

<https://blog.csdn.net/w401229755/article/details/51712581> logistic regression

<https://blog.csdn.net/zengxiantao1994/article/details/72787849> MLE

