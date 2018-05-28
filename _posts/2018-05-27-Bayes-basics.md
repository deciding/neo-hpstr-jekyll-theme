### Day7

**Bayes**: prior, posterior, likelihood. statistics vs. probablity, probability function vs. likelihood function. MLE vs. MAP(maximum a posteriori) 

MAP: based on yi=f(theta;xi), instead of yi=f(xi;theta). f(theta;xi)=f(theta,xi)/f(xi), f(theta,xi)=f(xi;theta) * f(theta), suppose we know f(theta) distribution ahead of time

**discrimitive and generative model**: similar to MAP, but we use MLE on p(x|y;theta) * p(y;theta), then we can get p(y|x) based on theta we get, and get argmax(y, p(y|x))=argmax(y,p(x|y) * p(y)). this is generative model instead of get y directly from x(discrimitive model). 

GDA(Gaussion Discriminative Analysis) and NB(naive bayes) are this kind. Naive Bayes p(x|y) is based on product(pi(xi|yi)), and p(y) is given. GDA p(x|y) is Gaussian distribution and p(y) is Binomial or Poisson. 

GDA p(y|x) result is actually Logistic Regression result, but reverse is not true

**LDA**: generative model, on topic classification. each document has topic distribution, and each topic has word distribution. currently hard for me to understand

<https://blog.csdn.net/u011508640/article/details/72815981> MAP

<https://blog.csdn.net/Fishmemory/article/details/51711114> discriminative and generative model

<https://blog.csdn.net/aws3217150/article/details/53840029> Latent Dirichlet Allocation
