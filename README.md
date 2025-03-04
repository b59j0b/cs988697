java c
Statistical model 
Suppose we have a random i.i.d. sample X = (X1, . . . , Xn) from the shifted Cauchy distribution Cauchy(θ) with density f(x|θ) = f(x − θ) (θ ∈ R), that is,

We are interested in estimating the location parameter θ.
Arranging the values X1, X2, . . . , Xn in ascending order, consider the order statistics
X(1) < X(2) < · · · < X(n) .
Since the Cauchy distribution is continuous, with probability 1 there are no ties in the observations, so all the inequalities may be presumed to be strict.
The sample median Mn is defined as the value separating the order statistics into two “equal parts”; more precisely, if n = 2k + 1 then Mn = X(k+1), so that
X(1) < · · · < X(k) < Mn = X(k+1) < X(k+2) < · · · < X(2k+1).
If n = 2k then the usual convention is to set Mn = 2/1(X(k)+X(k+1).
In this practical, you will consider the following four estimators of the parameter θ:

The MLE  is the maximiser of the log-likelihood, i.e.

where

The coefficient 2/n in the estimator  (modified sample median) is explained with the help of Theorem 9.3 in the lecture notes (cf. formula (9.26)) and by the fact that Fisher’s information in this model is given by (see Appendix 2 below)

Task 
The objective of the practical is to explore and compare the asymptotic properties of the four estimators above (where analytical calculations may not be possible).
To this end, use computer simulations to verify if these estimators are consistent (i.e., ˆθ n approaches the true value θ as n → ∞) and also to assess their accuracy by evaluating, for different values of the sample size n, their mean squared error MSEθ(ˆθn) = Eθ((ˆθn − θ)2) and the coverage probability Pθ(|ˆθn − θ| ≤ ε), say for ε = 0.1 and ε = 0.05.
Specific guidelines and questions to address:
1. Fix a certain value of θ and simulate代 写Statistical model
代做程序编程语言 your Cauchy samples from Cauchy(θ) using the R command rcauchy.
2. To visually verify consistency of estimator ˆθn = ˆθ(Xn), one method is to sample the values X1, X2, . . . , Xn sequentially and to plot the sequence of resulting values ˆθn as a (random) function of n ∈ N. What behaviour of such a plot would you expect for a consistent estimator?
3. When assessing the quality of the estimators, the sequential approach may be too computationally demanding, so it is recommended to confine oneself with some representative (increasing) values of the sample size n, say n = 10, 100, 500, 1000, . . .
4. To evaluate numerically the mean squared error and the coverage probability (for a given sample size n), make use of the Monte Carlo method (based on the Law of Large Numbers), according to which the expected value E(Y ) of a random variable Y can be approximated by the sample mean Y m = (Y1 + · · · + Ym)/m of a (large) i.i.d. sample Y = (Y1, . . . , Ym) from this distribution:

In practical applications, the number of replicates m should be large enough so that any two different estimation runs would yield reasonably close approximate values.
5. To illustrate the maximum likelihood estimation (MLE) method, plot the log-likelihood function e(θ|X) as a function of parameter θ for several different values of n (and with the corresponding sample values X1, . . . , Xn fixed). This can be done using the R function plot, but first you will have to define the function e(θ |X) using suitable R commands. Is there always a unique root of the likelihood equation e'θ = 0?
6. To calculate MLE numerically, it is recommended to use the R command optim; note however that it minimises a given function.
7. Summarise your findings by drawing the conclusions and recommendations.





         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
