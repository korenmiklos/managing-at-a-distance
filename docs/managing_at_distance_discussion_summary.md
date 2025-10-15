# Managing at a Distance Project: Research Discussion Summary

## Main Research Question and Motivation

The "managing at a distance" project focuses on understanding the matching process between firms and geographically distant managers, particularly examining the role of spatial frictions in managerial allocation. The core research question investigates how distance and nationality affect the assignment of managers to firms, with specific attention to German-Hungarian manager-firm relationships.

The motivation stems from the need to quantify frictions in managerial labor markets and understand their welfare implications. Unlike standard fixed effects approaches that suffer from downward bias in correlations between firm and manager effects, this project proposes a structural approach to identify the degree of misallocation.

## Theoretical Approach

### Frictionless Matching Framework

The theoretical foundation builds on optimal transport theory and assignment models. The baseline frictionless model assumes:
- Complementary production function: A × Z (firm productivity × managerial skill)
- Perfect assortative matching under positive cross-derivatives
- Optimal transport solutions via Monge-Kantorovich duality theorem

The speakers noted that while frictionless models provide elegant theoretical results, they are "highly sensitive" - introducing even one new manager causes complete reshuffling of all matches below a certain threshold, which is unrealistic.

### Friction Modeling: Tru-CO 2006 Framework

To address the limitations of frictionless models, the project adopts the Tru-CO (2006) framework that introduces idiosyncratic preference shocks:

**Firm's perspective:**
- Utility = Joint output - Wage + ε_firm (Gumbel distributed noise)

**Manager's perspective:**  
- Utility = Wage + ε_manager (Gumbel distributed noise)

The friction parameter σ controls the degree of sorting:
- σ → 0: Perfect assortative matching (frictionless case)
- σ → ∞: Random assignment (search model without assignment)
- Intermediate σ: Partial sorting with strength determined by friction level

### Shimer-Smith Framework

The discussion also referenced the Shimer-Smith (2000) model as an alternative approach for incorporating frictions through fixed costs of match dissolution. However, this was noted as "quite complicated" for the current application.

## Static Model Approach

The static version focuses on estimating the friction parameter σ for each year within Hungary. Key elements include:

**What We Learned:**
- The model generates probability of matching that depends on joint production and friction level
- Wage effects cancel out due to transferability, which is advantageous since wages are typically unobserved
- The soft-max (logit) structure replaces the hard max of frictionless models

**What We Agreed On:**
- Static model should be developed first as foundation
- Estimation would allow tracking of friction evolution over time
- Model provides "explainable structural" approach close to reduced form

**What Still Needs to be Done:**
- Work out the exact estimation procedure for the nonlinear system
- Develop identification strategy for the static case
- Implement estimation on Hungarian data

## Dynamic Model Approach

### Calvo-Style Random Dissolution

The dynamic extension introduces a Calvo-style framework where:
- Matches dissolve randomly with Poisson arrival rate λ
- Dissolution is independent of match quality and agent characteristics
- Creates "fake dynamics" that generate mobility for identification

**Bellman Equation Structure:**
- Agents care about present value of matches, not just current period utility
- Expected match duration affects sorting strength
- Higher dissolution rates weaken sorting incentives

**What We Learned:**
- Random dissolution creates representative sample of newly unmatched agents
- Mobility patterns become informative about underlying match qualities
- Framework maintains tractability while adding realistic dynamics

**What We Agreed On:**
- Dynamic version provides better identification opportunities
- Should help estimate manager and firm fixed effects through mobility
- Creates natural connection to search literature

## Identification Strategy

### Mobility-Based Identification

The key insight is that random dissolution generates quasi-experimental variation:

**Firm-to-Firm Mobility:**
- Depends on correlation between firm and manager types
- Reflects variance of firm productivity distribution

**Manager-to-Manager Mobility:**  
- Depends on same correlation parameter
- Reflects variance of manager skill distribution

**Cross-Sectional Variation:**
- Combined effect of both variances and their correlation

**Three Moments, Three Parameters:**
- Variance of firm productivity (var(A))
- Variance of manager skill (var(Z))  
- Correlation between firm and manager types (corr(A,Z))

**What We Learned:**
- Under log-normality assumptions, the system becomes exactly identified
- Preliminary estimates showed correlation increasing over time in Hungary (early 1990s to later periods)
- Method avoids downward bias of standard fixed effects approaches

**What We Agreed On:**
- Focus on "random effects" approach estimating second moments rather than individual fixed effects
- Can potentially add observables and group effects (e.g., foreign vs. domestic managers)

**What Still Needs to be Done:**
- Formally derive the moment conditions for general distributions
- Work out identification under non-log-normal assumptions
- Develop estimation procedure for the dynamic case

## Data Requirements and Applications

### German-Hungarian Linked Manager Database

**Current Data Status:**
- Hungarian employer-employee data: 2002-2021
- German data integration: Required for cross-country identification
- Need to link manager flows between countries

**Identification Requirements:**
- At least two countries needed to separate quality effects from friction effects
- Three countries available: Germany, Austria, Hungary
- City-pair analysis possible (e.g., Hamburg-Gyor, Gyor-Hamburg)

**What We Learned:**
- Cannot identify border/nationality effects with single country data
- Need cross-country variation to separate average quality effects from spatial frictions
- Administrative data provides unprecedented detail for this type of analysis

**What We Agreed On:**
- German data acquisition is crucial for the project
- Focus initially on German-Hungarian-Austrian triangle
- Use city-level variation for gravity equation estimation

**What Still Needs to be Done:**
- Complete German data integration
- Develop protocols for cross-country manager identification
- Create consistent occupation and industry classifications across countries

## Connection to Gravity Equations and Spatial Frictions

### Gravity Framework Application

The project naturally extends to gravity equation estimation:
- Dependent variable: Number of managers from origin country/city working in destination
- Explanatory variables: Distance, common border, common language/nationality
- Structural interpretation through friction parameter σ

**Modeling Distance Effects:**
- Friction parameter τ as function of distance and nationality
- Separate identification of distance decay from nationality premiums
- Connection to international trade gravity literature

**What We Learned:**
- Even basic gravity estimation could yield top-tier publication
- Model provides structural interpretation of gravity coefficients
- Unique dataset allows unprecedented analysis of managerial flows

**What We Agreed On:**
- Start with gravity estimation as foundation
- Extend to productivity analysis of foreign managers
- Connect to existing trade literature on expert managers

## Timeline and Publication Strategy

### Two-Year Deliverables

**Year 1 Targets:**
- Static model development and estimation
- Working paper version of managing at a distance framework
- Preliminary German data integration

**Year 2 Targets:**
- Dynamic model implementation
- Cross-country gravity estimation
- Policy applications and welfare analysis

**What We Agreed On:**
- Static version should be completed first
- Dynamic version may actually be easier to implement due to identification advantages
- Aim for working paper circulation by end of first year

**Publication Targets:**
- Top-5 general interest journal potential due to methodological contribution
- Unique data and novel structural approach
- Policy relevance for labor mobility and firm performance

**What Still Needs to be Done:**
- Prioritize static vs. dynamic model development
- Coordinate with data acquisition timeline
- Develop conference presentation strategy

## Academic and Policy Context

### Literature Positioning

The project fills several gaps in existing literature:
- Few papers have linked cross-country manager-firm data
- Limited structural approaches to managerial assignment
- Novel application of optimal transport methods to labor economics

**Differentiation from Existing Work:**
- Gunthert, Steinmeier, and Antoni (QJE) focus on within-firm establishment distances
- Xavier Giroud papers examine investment and plant-level effects
- Current project focuses on manager-firm matching across countries

### Policy Applications

**Potential Policy Questions:**
- Effects of reducing mobility frictions (e.g., EU integration)
- Welfare implications of managerial misallocation
- Optimal policies for attracting foreign managerial talent

**What We Agreed On:**
- Strong policy relevance given EU labor mobility initiatives
- Natural experiments possible through infrastructure improvements
- Connection to broader questions about talent allocation and economic development

This summary captures the key elements of the managing at a distance project discussion, focusing specifically on the theoretical framework, empirical strategy, and implementation plan while filtering out discussions of other research projects.