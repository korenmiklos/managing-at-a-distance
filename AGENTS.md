# Managing at a Distance: Project Summary

## Research Question

How do distance and nationality affect the matching process between firms and geographically distant managers? What are the welfare implications of spatial frictions in managerial labor markets?

## Methodology

### Theoretical Framework

The project employs a structural matching model combining optimal transport theory with friction modeling:

1. **Frictionless Baseline**: Complementary production function A × Z with perfect assortative matching via Monge-Kantorovich duality theorem. However, frictionless models are "highly sensitive" - one new manager causes complete reshuffling of all matches below a threshold, which is unrealistic.

2. **Friction Modeling**: Choo-Siow (2006) framework introducing idiosyncratic preference shocks (Gumbel distributed) with friction parameter σ:
   - Firm utility: Joint output - Wage + ε_firm (Gumbel noise)
   - Manager utility: Wage + ε_manager (Gumbel noise)
   - σ → 0: Perfect assortative matching (frictionless)
   - σ → ∞: Random assignment (search without assignment)
   - Intermediate σ: Partial sorting with soft-max (logit) structure replacing hard max
   - Wage effects cancel due to transferability (advantageous since wages often unobserved)

3. **Dynamic Extension**: Calvo-style random dissolution with Poisson arrival rate λ:
   - Matches dissolve randomly, independent of quality and characteristics
   - Creates "fake dynamics" generating mobility for identification
   - Bellman equation structure: agents care about present value of matches
   - Higher dissolution rates weaken sorting incentives

### Key Innovation

Rather than estimating individual fixed effects (which suffer from downward bias in firm-manager correlations), the model focuses on estimating second moments: variance of firm productivity var(A), variance of manager skill var(Z), and correlation corr(A,Z).

### Identification Strategy

Mobility-based identification exploiting quasi-experimental variation from random match dissolution creates a system of three moments identifying three parameters under bivariate normality (log-normal in levels):

**Three moments, three parameters:**
- Firm-to-firm mobility: depends on var(A) and corr(A,Z)
- Manager-to-manager mobility: depends on var(Z) and corr(A,Z)
- Cross-sectional variation: depends on both variances and correlation
- System identifies var(A), var(Z), and corr(A,Z) jointly

**Key advantages:**
- Avoids downward bias in standard fixed effects correlations
- Random effects approach estimating second moments rather than individual fixed effects
- Can extend to include observables and group effects (e.g., foreign vs. domestic managers)

## Data

### Current Status
- Hungarian employer-employee data: 2002-2021
- German and Austrian data integration: In progress
- Focus: German-Hungarian-Austrian triangle for cross-country identification

### Requirements
Requires at least two countries to separate quality effects from friction effects. Administrative data allows city-level analysis (e.g., Hamburg-Gyor flows).

## Empirical Applications

1. **Static Model**: Estimate friction parameter σ for each year within Hungary, tracking evolution of sorting over time
2. **Dynamic Model**: Exploit mobility patterns to estimate firm and manager quality distributions
3. **Gravity Equations**: Model manager flows as function of distance, borders, and nationality

## Implementation Plan

### Phase 1: Static Model
- Develop estimation procedure for nonlinear system
- Implement on Hungarian data
- Track friction evolution: preliminary estimates show increasing correlation in Hungary from early 1990s to later periods

### Phase 2: Dynamic Model  
- Formalize moment conditions under general distributions
- Develop estimation procedure exploiting mobility patterns
- May offer stronger identification than static version despite added complexity
- Technical challenges: bilateral dissolution decisions, switching costs, Bellman equations

### Phase 3: Cross-Country Analysis
- Complete German/Austrian data integration
- Estimate gravity equations with structural interpretation
- Separate distance decay from nationality premiums

## Policy Relevance

- Effects of reducing mobility frictions (e.g., EU integration)
- Welfare implications of managerial misallocation
- Optimal policies for attracting foreign managerial talent

## Literature Positioning

Fills gaps in existing work by:
- Linking cross-country manager-firm data (rare in literature)
- Providing structural approach to managerial assignment
- Novel application of optimal transport methods to labor economics

Differs from existing work (Grunthert-Steinmeier-Antoni QJE, Giroud papers) by focusing on manager-firm matching across countries rather than within-firm establishment distances.

## Timeline and Publication Target

### Two-Year Deliverables

**Year 1:**
- Static model development and estimation
- Working paper version of managing at a distance framework
- Preliminary German data integration

**Year 2:**
- Dynamic model implementation
- Cross-country gravity estimation
- Policy applications and welfare analysis

### Publication Target

Top-5 general interest journal potential based on:
- Methodological contribution
- Unique administrative data
- Policy relevance for labor mobility and firm performance

## Technical Notes

### Parametric Distribution Options

The matching density has the form:
$$\mu(a,z) = e^{az/\sigma}\Phi(a)\phi(z)$$

Under bivariate normality, the friction parameter σ connects to the correlation between firm and manager types. The log specification:
$$\ln\mu(a,z) = \frac{az}{\sigma} + \ln \Phi(a) + \ln\phi(z)$$

provides tractable moment conditions. Alternative distributions (Pareto, gamma, exponential) explored but normal distribution offers cleanest connection between structural friction parameter and reduced-form correlation.

### Dynamic Steady State (Choo-Siow–Calvo)

With Poisson dissolution δ and discount ρ, define $Q(a,z)=az/(\rho+\delta)$. Under logit choices on both sides, the steady-state matching measure satisfies
$$\mu^*(a,z) = e^{Q(a,z)/(2\sigma)}\sqrt{\Phi(a)\,\phi(z)}.$$
Wages drop out of $\mu^*$; identification comes from flows and marginals.

### Within-Destination Sorting Slope

In the production-with-labor variant, within a destination $d$ the log-odds across firms $i,j$ for the same manager type satisfy
$$\ln \mu_{mi} - \ln \mu_{mj} = (\sigma/\nu)(\ln A_{id}-\ln A_{jd}),$$
providing a reduced-form diagnostic for frictions relative to output elasticity $\nu$.

### Distance and Commuting Costs

Distance and borders enter via observed costs/retention (e.g., $\kappa_{od}$ or $\tau_{od}$), shifting the intensive margin of cross-location matches; the marginal commuting condition pins the threshold skill for cross-border moves.

### Two-Sided Meeting (Stock–Flow) Model

An alternative dynamic microfoundation lets unemployed managers meet firms with rate $\lambda_2$ and empty firms meet managers with rate $\lambda_1$. A match forms with joint probability $\pi(a,z)\,\Pi(a,z)$ (mutual acceptance). This nests the static Choo–Siow structure in limiting cases (e.g., negligible discounting), but generally the manager’s value depends on the firm’s acceptance probability, complicating Bellman equations and identification. Empirically, this introduces meeting-rate parameters alongside $\sigma$ and may require instruments or external variation for $\lambda_1,\lambda_2$.

### NEF and MLR Ordering

Within types, the induced conditional firm distribution $f_z(A) \propto \sqrt{\mu_{0A}}\,e^{zA}$ lies in the natural exponential family, implying monotone likelihood ratio ordering in $A$ across higher $z$. This delivers testable positive assortative matching and provides reduced-form diagnostics consistent with the structural model.
