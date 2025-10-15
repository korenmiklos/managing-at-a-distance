# Matching of managers to firms

# Single dimension

Firms differ in capital $K_j$. Managers differ in productivity $A_i$. The total output of a manager-firm pair is $A_i K_j$.

Firms hire managers that maximize revenue net of wages $w_i$, but only do so with a soft-max. (This can be microfounded with a Gumbel cost shock.) 

$$
\mu_{ij} = \frac {\exp[(A_iK_j-w_i)/T]}{1+\sum_m \exp[(A_mK_j-w_m)/T]}
$$

$$
\mu_{0j} = \frac {1}{1+\sum_m \exp[(A_mK_j-w_m)/T]}
$$

$$
\ln\mu_{ij} = \ln\mu_{0j} + {\frac1T(A_iK_j-w_i)}
$$

$$
\ln\mu_{ij} = \ln\mu_{0j} + {\frac1TR_{ij}-\frac1Tw_i}
$$

$$
R_{ij}=w_i+T(\ln\mu_{ij} - \ln\mu_{0j})
$$

# Dynamic matching

There are $n_{xt}$ managers of type $x$ and $m_{yt}$ firms of type $y$ and time $t$. 

Going in to period $t$, some managers are already matched. They will have to decide whether to sever the relationship and rematch. Rematching managers obtain utility $U_{xt}$, rematching firms obtain $V_{yt}$.

Matching is done in a logit framework a la Choo-Siow (2006, JPE), so that

$$
U_{xt} := T \ln[\exp(\mathcal U_{xyt}/T) + \sum_y \exp((w_{xyt}+\beta \mathcal U_{xy,t+1})/T)]
$$

$$
V_{yt} := T \ln[\exp(\mathcal V_{xyt}/T) + \sum_x \exp((\Phi_{xyt}-w_{xyt}+\beta \mathcal V_{xy,t+1})/T)]
$$

From Artuc et al

$$
\mathcal U_{xyt} = w_{xyt}+\max_{z} \{\varepsilon_{xzt}-C+\beta E_t\mathcal U_{xz,t+1}\}
$$

$$
\mathcal U_{xyt} = w_{xyt}+\max_{z} \{\varepsilon_{xzt}-C+\beta E_t\mathcal U_{xz,t+1}\}
$$

$$
E_{t-1}\mathcal U_{xyt} = w_{xyt}+ T\ln\sum_z\exp()
$$

If deciding to switch, she will also have to pay switching cost $C$.

$$
\Omega(\bar\varepsilon_{xyt}) = -T\ln m_{xyt,\text{stay}}
$$

Equation (8) from Artuc et al

$$
\beta E_t\left[w_{xz,t+1}-w_{xy,t+1}+T(\ln m_{x,y\to z,t+1}-\ln m_{x,y\to y,t+1})\right] = (1-\beta)C_x+T(\ln m_{x,y\to z,t}-\ln m_{x,y\to y,t})
$$

Same for firms (not in Artuc et al)

$$
\beta E_t\left[Q_{xz,t+1}-w_{xz,t+1}-Q_{kz,t+1}+w_{kz,t+1}+T(\ln m_{k\to x,z,t+1}-\ln m_{k\to k,z,t+1})\right] = (1-\beta)C_y+T(\ln m_{k\to x,z,t}-\ln m_{k\to k,z,t})
$$

# Artuc et al notation, but firms can also dissolve a relationship

The probability of a relationship not dissolving depends on both firm and worker being happy in that relationship.

$$
V_{it}+J_{it} - \beta E_t(V_{it+1}+J_{it+1}) = Q_{it}-T\ln(n_{iit}m_{iit})
$$

The probability of a new relationship forming depends on both firm and worker accepting that relationship. Probability of worker from $i$ wanting to go to $j$

$$
n_{ijt} =\nu_{it} \exp[(\beta E_t(V_{jt+1}-V_{it+1})-C_x)/T] = \tilde\nu_{it} \exp(\beta E_tV_{jt+1}/T)
$$

Probability of firm from $k$ wanting to hire this worker instead,

$$
m_{kjt} =\mu_{kt} \exp[(\beta E_t(J_{jt+1}-J_{kt+1})-C_y)/T] = \tilde\mu_{kt}\exp(\beta E_tJ_{jt+1}/T)
$$

Probability of an $(i,k)$ match finding a new match acceptable

$$
n_{ijt}m_{kjt} = \tilde\nu_{it} \tilde\mu_{kt} \exp[\beta E_t(V_{jt+1}+J_{jt+1})/T]
$$

[[ERC-2023-AdG]]