$$
A_{id} z_{mo}^\nu n_{id}^{1-\nu}
$$
FOC wrt labor
$$
(1-\nu) A_{id}(z_{mo}/n_{id})^\nu  = w_d
$$
$$
(1-\nu)^{1/\nu} (A_{id}/w_d)^{1/\nu}z_{mo}  = n_{id}
$$
$$
(1-\nu)^{1/\nu-1} (A_{id}/w_d)^{1/\nu-1}z_{mo}^{1-\nu}  = n_{id}^{1-\nu}
$$
Revenue
$$
z_{mo}A_{id}^{1/\nu} (1-\nu)^{1/\nu-1} w_d^{1-1/\nu},
$$
of which $\nu$ shares goes to manager income, but only $\kappa_{od}$ fraction are retained, the rest are lost with commuting 
$$
V_{mod} = z_{mo}\kappa_{od}\nu (1-\nu)^{1/\nu-1} A_{id}^{1/\nu}  w_d^{1-1/\nu}.
$$
Following Choo-Siow2006 and Monte2018, we introduce idiosyncratic managers preferences for work locations. Let $\pi_{mi}$ be the probability that manager $m$ works for firm $i$.

$$
\ln \pi_{mi} = c_m +
\sigma \ln V_{mi} = c_m + 
\sigma\ln \left[z_{mo}\kappa_{od}\nu (1-\nu)^{1/\nu-1} A_{id}^{1/\nu}  w_d^{1-1/\nu}\right],
$$
where $c_m$ can be pinned down from the fact that probabilities sum to 1.

Sorting across firms with different size in the same destination $d$:
$$
\ln \pi_{mi} - \ln \pi_{mj} =
\frac\sigma\nu (\ln A_{id} - \ln A_{jd})
$$

The marginal manager is indifferent between working at home or commuting as a manager. (You cannot commute as a worker.)

$$
w_o = \tilde V_{mod} = \tilde z_{o}\kappa_{od}\nu (1-\nu)^{1/\nu-1} A_{id}^{1/\nu}  w_d^{1-1/\nu}.
$$
so that
$$
\tilde z_{o} = \frac{w_o}{w_d}  \kappa_{od}^{-1}\nu^{-1} (1-\nu)^{1-1/\nu} (w_d/A_{id})^{1/\nu}.
$$
Only better managers would commute from far-away regions. The revenue of the firm run by the marginal commuting manager
$$
w_o \kappa_{od}^{-1}\nu^{-1}.
$$

## Using Choo-Siow
Let firms be indexed by their productivity and managers be indexed by their skill. This is WLOG because there is also a marginal distribution of each. Similarly, by choice of units, we set $T=1$.
$$
	f(A_j|z_i) = \frac{\mu_{ij}}
		{\int_k \mu_{ik}dk} 
$$
$$
\ln\mu_{zA} = z A + \frac1{2}(\ln\mu_{z0} + \ln\mu_{0A})
$$
$$
\mu_{zA} = \sqrt{\mu_{z0}\mu_{0A}} e^{z A} 
$$

The firm-size distribution for given manager type
$$
f_z(A) = \frac{\mu_{zA}}
	{\int_a \mu_{za}da}
= \frac {\sqrt{\mu_{0A}} e^{z A} }
	{\int_a \sqrt{\mu_{0a}} e^{z a} da}
= \Phi_z\sqrt{\mu_{0A}} e^{z A} .
$$
This is an element of the *natural exponential family*. This implies that for higher $z$s, the productivity distribution of firms is dominating in the monotone likelihood ratio sense.

Using the cumulant-generating function, we can derive the mean productivity as
$$
\frac {\partial\ln\int_a \sqrt{\mu_{0a}} e^{z a} da}
	{\partial z} =
\frac {\int_a a \sqrt{\mu_{0a}} e^{z a} da}
	{\int_a \sqrt{\mu_{0a}} e^{z a} da}
$$

$$
\ln f_z(A) 
= \ln\Phi_z + \frac12\ln\mu_{0A}+{z A}/\sigma .
$$



$$
\Pr(Q \le x|z_i) =
\frac
	{\int_{j: A_j\le x/z_i}\alpha_i \beta_j e^{z_i A_j/T} dj}
	{\int_{j}\alpha_i \beta_j e^{z_i A_j/T} dj}
$$
$$
 =
\frac
	{\int_{j: A_j\le x/z_i} \beta_j e^{z_i A_j/T} dj}
	{\int_{j}\beta_j e^{z_i A_j/T} dj}
$$
The density function
$$
\frac {d}{dx}=
\beta_{j:z_iA_j=x} e^{x/T}
$$

Take a set of firms managed by the same $i$ type of managers (good Westerners, say)
$$
\ln\mu_{ij} - \ln \mu_{ik} = \frac1T
(Q_{ij} - Q_{ik})
= \frac1T
z_i(A_j-A_k)
$$

Wages
$$
\ln \mu_{ij} - \ln\mu_{i0}= 
\frac1T w_{ij} 
$$

- [x] create graph of FSD by expat
[[MKTMGR]]

[[ERC-2023-AdG]]