[[ERC-2023-AdG]]

Try a parametric distribution for $\mu(a,z)$. We know that
$$
\mu(a,z) = e^{az/\sigma}\Phi(a)\phi(z)
$$
(with different parametrization).
$$
\ln\mu(a,z) = \frac{az}{\sigma} + \ln \Phi(a) + \ln\phi(z)
$$
The conditional distribution is
$$
\mu(z|a) = 
\frac {e^{az/\sigma}\phi(z)}
	{\int_x e^{ax/\sigma}\phi(x)dx}.
$$
Can this have an infinite support over $z$? A necessary but not sufficient condition is that
$$
\lim_{z\to\infty} \mu(z|a) = 0,
$$
so that $\phi(z)$ has to decrease faster than exponential with coefficient $-a/\sigma$.


The gamma distribution is parametrized as
$$
f(x)=\frac{\beta^\alpha}{\Gamma(\alpha)} x^{\alpha - 1} e^{-\beta x }
$$
A multivariate gamma is the [matrix gamma distribution](https://en.wikipedia.org/wiki/Matrix_gamma_distribution)

https://en.wikipedia.org/wiki/Exponential_family

Let $\mu(a,z|a)$ be an exponential distribution with ???

### Pareto
$$
\ln f(x) = \ln\alpha +\alpha\ln x_m-(\alpha+1)\ln x
$$
not looking good
### Normal
$$
\ln f(x) = -\frac{1}{2}\ln(2\pi) - \frac{1}{2}\ln\sigma^2 
- \frac{1}{2\sigma^2}\mu^2
- \frac{1}{2\sigma^2}x^2
+ \frac{1}{\sigma^2}\mu x
$$
MLR shifting it with $ax/\sigma$ (a different $\sigma$ though) amounts to shifting the mean of the distribution.

Write down a bivariate normal distribution for $a$ and $z$ and show how $\sigma$ is linked to the correlation.

$$
\mu(a,z) = e^{az/\sigma}\Phi(a)\phi(z)
$$
Let $a$ be exponential conditional on $z$:
$$
\mu(a|z) = (\lambda-z/\sigma) e^{-(\lambda-z/\sigma) a}
$$
> It may be possible to derive a nice parametric distribution
