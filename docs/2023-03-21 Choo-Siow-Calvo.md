Managers have a distribution of skills, $z \sim G(z)$. Firms have a distribution of productivities $a \sim F(a)$. When a manager and a firm matches, they produce an output of $az$. The distributions and the production function are time invariant.

At any given point in time, there is a stock of unmatched managers, unmatched firms, and manager-firm matches. Given the constant $F$ and $G$ distributions, matching can be charactezied by the joint measure of matches, $\mu(a, z, t)$.
$$
F(a) = \int \mu(a, z, t)dz + \mu_1(a,t)
$$
and
$$
G(z) = \int \mu(a, z, t)da + \mu_2(z,t).
$$
Each match is dissolved by a Calvo fairy at a Poisson rate $\delta$, independent of $a$ and $z$. This creates an outflow from $\mu$ into $\mu_1$ and $\mu_2$. 

### Managers
Unemployed managers can a look for a job with Poisson arrival $\lambda$. They then get a draw of a match-specific cost for each unmatched firm. This cost is $\sigma\xi$, where $\xi$ is distributed independtly across potential firm matches with a standard Gumbel distribution and $\sigma>0$ is a parameter.

Which firm will the manager choose? The value of working for firm $a$ is given by the Hamilton-Jacobi-Bellman equation,
$$
\rho V(a,z,t) = w(a,z,t) - \delta [V(a,z,t) - V_0(z,t)],
$$
where $V_0$ is the value of being an unemployed manager.
$$
V(a,z,t) = \frac 
 {w(a,z,t)+\delta V_0(z,t)}
 {\rho+\delta}
$$
The value net of matching cost is 
$$
\frac 
 {w(a,z,t)+\delta V_0(z,t)}
 {\rho+\delta} - \sigma \xi
$$
Denote $W := w/(\rho+\delta)$ the perpetual value of wages.

Before knowing the realization of the matching cost, the probability that the manager chooses firm $a$ is given by a logit equation,
$$
\pi(a,z,t) = \frac {e^{W(a,z,t)/\sigma}e^{\varrho V_0/\sigma}}
  {e^{V_0/\sigma}+\int e^{W(A,z,t)/\sigma}e^{\varrho V_0/\sigma}dA},
$$
$$
= \frac {e^{W(a,z,t)/\sigma}}
  {e^{(1-\varrho)V_0(z,t)/\sigma}+\int e^{W(A,z,t)/\sigma}dA},
$$
with $\varrho = \delta/(\delta+\rho)\in(0,1)$.

The probabilty of the manager choosing to remain unemployed is $\pi_0(z,t) = e^{V_0/\sigma}/[e^{V_0/\sigma}+\int e^{W(A,z,t)/\sigma}e^{\varrho V_0/\sigma}dA]$. The relative probabilities are
$$
\frac {\pi(a,z,t)}
	{\pi_0(z,t)}
=
e^{W(a,z,t)/\sigma}e^{(\varrho-1) V_0(z,t)/\sigma}
$$
Suppose all willing managers are hired (we will verify this in equilibrium). Then the Kolmogorov equations are
$$
\dot \mu(a,z,t) = \lambda\pi(a,z,t)\mu_2(z,t) - \delta \mu(a,z,t)
$$
and
$$
\dot \mu_2(z,t) = -\lambda [1-\pi_0(z,t)]\mu_2(z,t) + \delta\int \mu(a,z,t)da.
$$
A $1-\pi_0$ fraction of potential matches will be attractive enough to go back to work, reducing the mass of unemployed managers. All kinds of employed managers are fired with hazard $\delta$.

In steady state,
$$
\mu_2^*(z) = \frac {\delta}
	{\lambda [1-\pi_0^*(z)]} 
\int \mu^*(a,z)da	
$$
and
$$
\mu^*(a,z) = 
\frac {\pi^*(a,z)}
	{1-\pi_0^*(z)} 
\int \mu^*(A,z)dA.
$$
This looks promising! The key object of interest is 
$$
\frac {\pi^*(a,z)}
	{1-\pi_0^*(z)}
	= \frac {e^{W^*(a,z)/\sigma}e^{\varrho V_0^*/\sigma}}
  {\int e^{W^*(A,z)/\sigma}e^{\varrho V_0^*/\sigma}dA}
$$
and the $V_0$ term cancels so that
$$\tag{*}
\mu^*(a,z) = 
\frac {e^{W^*(a,z)/\sigma}}
  {\int e^{W^*(A,z)/\sigma}dA}\int \mu^*(A,z)dA
= e^{W^*(a,z)/\sigma} \phi(z).
$$
### Firms
The value of a firm is
$$
\rho J(a,z,t) = az - w(a,z,t) - \delta[J(a,z,t) - J_0(a,t)],
$$
with
$$
J(a,z,t) = \frac{az}{\rho+\delta} -W(a,z,t) + \varrho J_0(a,t).
$$
Denoting $Q(a,z):=az/(ρ+δ)$ and using the same steps as above
$$\tag{**}
\mu^*(a,z) = 
\frac {e^{[Q(a,z)-W^*(a,z)]/\sigma}}
  {\int e^{[Q(a,Z)-W^*(a,Z)]/\sigma}dZ}\int \mu^*(a,Z)dZ
= e^{[Q(a,z)-W^*(a,z)]/\sigma}\Phi(a).
$$
We have used the fact that matching is one to one, so $\mu(a,z)$ is the same whether we calculate from flows of managers or flows of firms.

Take the geometric average of (\*) and (\*\*):
$$
\mu^*(a,z) = 
 e^{Q(a,z)/2\sigma}\sqrt{\phi(z)\Phi(a)}.
$$
This is the Choo-Siow formula!

## Steady-state switching
In steady state, some matches are dissolved and new ones are formed. Let's follow a firm through such a process.

Dissolving firms are a random sample of all firm-manager pairs. So the joint distribution of firm productivities and manager skills is $\mu^*(a,z)$. The distribution of sales is
$$
\Pr[Q \le q] = \int_0^\infty \int_0^{q/a} 
	\mu^*(a,z) dz da
$$
The next match is also going to be drawn from $\mu^*(a,z)$ but for the same $a$. 

> NOT QUITE: we need to divide by the sume of mu across firm pairs. We **normalize** $\iint \mu^*(a,z)dadz=1$.

The joint distribution of $Q$ and $Q'$ is
$$
\Pr(Q\le q, Q' \le q') = 
\int_a\Pr(Q\le q, Q' \le q'|a) f(a)da.
$$
Conditional on $a$, the two events are independent, so the probability of both happening is the product of the probabilities.
$$
\Pr(Q\le q, Q' \le q'|a) = \Pr(Q\le q|a)Pr(Q\le q'|a)
=
	\frac {\int_0^{q/a} \mu^*(a,z)dz}
		{\int_0^{\infty} \mu^*(a,z)dz}
	\frac {\int_0^{q'/a} \mu^*(a,z)dz}
		{\int_0^{\infty} \mu^*(a,z)dz}
$$
The density of $a$ is $f(a) = \int_0^{\infty} \mu^*(a,z)dz$.
$$
F(Q,Q') = \int_a	\frac {\int_0^{q/a} \mu^*(a,z)dz\int_0^{q'/a} \mu^*(a,z)dz}
		{\int_0^{\infty} \mu^*(a,z)dz}
da
$$
To derive the joint density function,
$$
F_1(q,q') = 
\int_a	\frac {\mu^*(a,q/a)\int_0^{q'/a} \mu^*(a,z)dz}
		{a\int_0^{\infty} \mu^*(a,z)dz}
da
$$
$$
F_{12}(q,q') = f(q,q')=
\int_a	\frac {\mu^*(a,q/a)\mu^*(a,q'/a)}
		{a^2\int_0^{\infty} \mu^*(a,z)dz}
da
$$
$$
\mu^*(a,q/a) = 
 e^{q/2\sigma}\sqrt{\phi(q/a)\Phi(a)}.
$$
factor out terms independentof $a$
$$
f(q,q')=
e^{(q+q')/2\sigma}\int_a	\frac {\sqrt{\phi(q/a)\phi(q'/a)}\Phi(a)}
		{a^2\int_0^{\infty} \mu^*(a,z)dz}
da
$$
## The Tinder model
Unemployed managers get the possibility to pick a fim with Poisson arrival $\lambda_2$. They draw a firm from logit $\pi(a,z)$. Empty firms get to pick with Poisson arrival $\lambda_1$. They draw a manager from logit $\Pi(a,z)$. A match is formed if both sides picked one another, with probability $\pi(a,z)\Pi(a,z)$. 

Challenge: the value of picking firm $a$ depends on the probability whether they accept, $\Pi(a,z)$. If they don't accept, the manager goes back to being unemployed and spend some time there. This is not an issue in Choo-Siow because it is a static model. Probably if $\rho=0$, we get back Choo-Siow.

Let's try a Bellman. Value of being in a match for a manager is $V(a,z)$. Value of "swiping right" is
$$
\tilde V(a, z) = \Pi(a,z)V(a,z) + [1-\Pi(a,z)] V_0(z)
$$
so that
$$
\tilde V(a,z)-V_0(z) = \Pi(a,z)[V(a,z) - V_0(z)].
$$
Logit:
$$
\pi(a,z) \propto e^{\Pi(a,z)} V_0(z)].
$$
Logit:
$$
\pi(a,z) \propto e^{\Pi(a,z)V(a,z)}/e^{\Pi(a,z)V_0(z)}
$$
This hopelessly depends on $\Pi$. 

Maybe I just don't understand Choo-Siow. There are no two independent draws.

## Notes copied from B2.tex
To study how managers with skill $z$ and firms with productivity $a$ match, consider a manager $m$ is contemplating job offers from various firms. At firm $i$, they would make wage $w_{im}$. Their overall utility from working for firm $i$ is
$$
V_{im} = w_{im} - \tau_{im} - \sigma \xi_{im},
$$
where $\tau_{im}$ is the observed cost of working for firm $i$ (say, commuting costs increasing in distance to the firm), and $\xi_{im}$ is an unobserved, idiosyncratic matching cost with a standard Gumbel distribution \pcite{Choo2006-ki,Galichon2019-gi}. Importantly, the matching cost is independent of firm and manager quality $a_i$ and $z_m$ and observed matching cost $\tau_{im}$.

Before knowing the realization of the matching cost, the probability that the manager chooses firm $i$ is given by a logit equation,
$$
\pi_{im} = \frac {e^{(w_{im}-\tau_{im})/\sigma}}
  {\sum_j e^{(w_{jm}-\tau_{jm})/\sigma}}.
$$
The profit of the firm from hiring manager $m$ is
$$
J_{im} = a_i z_m - w_{im} - \sigma \varepsilon_{im},
$$
where $\varepsilon_{im}$ is a firm-specific matching cost of the \emph{same distribution} as, but independently draw from $\xi$. We have used the simple match-specific production $a_iz_m$, but other specifications can also be included.

Before knowing the realization of the matching cost, the probability that the firm chooses manager $m$ is given by a logit equation,
$$
\Pi_{im} = \frac {e^{(a_i z_m - w_{im})/\sigma}}
  {\sum_k e^{(a_iz_k - w_{ik})/\sigma}}.
$$
For a match to form, both the firm and the manager has to agree. The probability that both find each other suitable is
$$
\mu_{im} = \pi_{im}\Pi_{im} = \frac {e^{(a_i z_m - \tau_{im})/\sigma}}
  {\phi_i \Phi_m}.
$$
The joint distribution $\mu_{im}$ shows the equilibrium likelihood of matches between a particular firm $i$ and manager $m$ and how this depends on productivity, manager skill and frictions.

There is positive assortative matching: better managers are more likely to match with better firms. The parameter $\sigma$ captures the strength of the sorting. If there is a large heterogeneity in matching costs, $\sigma$ is large, and sorting is weaker. At the other extreme, as $\sigma$ tends to zero, sorting becomes perfect: the best managers are only matched with the best firms.

[[ERC-2023-AdG]]