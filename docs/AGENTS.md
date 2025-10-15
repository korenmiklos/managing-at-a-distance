# Managing at a Distance: Project Summary

## Research Question

How do distance and nationality affect the matching process between firms and geographically distant managers? What are the welfare implications of spatial frictions in managerial labor markets?

## Methodology

### Theoretical Framework

The project employs a structural matching model combining optimal transport theory with friction modeling:

1. **Frictionless Baseline**: Complementary production function A × Z with perfect assortative matching
2. **Friction Modeling**: Choo-Siow (2006) framework introducing idiosyncratic preference shocks (Gumbel distributed) with friction parameter σ
3. **Dynamic Extension**: Calvo-style random dissolution with Poisson arrival rate λ generating mobility for identification

### Key Innovation

Rather than estimating individual fixed effects (which suffer from downward bias in firm-manager correlations), the model focuses on estimating second moments: variance of firm productivity var(A), variance of manager skill var(Z), and correlation corr(A,Z).

### Identification Strategy

Mobility-based identification exploiting quasi-experimental variation from random match dissolution:
- Firm-to-firm mobility reflects var(A) and corr(A,Z)
- Manager-to-manager mobility reflects var(Z) and corr(A,Z)
- Three moments identify three parameters under log-normality

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
- May be easier to implement than static version due to stronger identification

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

## Publication Target

Top-5 general interest journal potential based on:
- Methodological contribution
- Unique administrative data
- Policy relevance for labor mobility and firm performance
