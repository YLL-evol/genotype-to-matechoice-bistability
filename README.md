# Genotype–Phenotype–Mate Choice Feedbacks and the Emergence of Alternative Reproductive Strategies

## Research Question

Under what conditions can genotype–phenotype–mate-choice feedbacks generate an abrupt transition from a monomorphic male population to alternative reproductive strategies?

This project develops a minimal eco-evolutionary model linking genetic variation, trait expression, female mate choice, and fitness feedbacks. The objective is to investigate whether positive sexual selection feedback alone is sufficient to generate bistability, threshold dynamics, and the emergence of alternative reproductive strategies.

## Biological Framework

The model is built around a genotype–phenotype–fitness feedback loop.

Male trait allele frequency (A) influences ornament expression (T).

Female preference allele frequency (B) influences mate preference strength (P).

Trait expression and preference jointly determine mating success (M).

Fitness (W) emerges from the balance between mating benefits and viability costs.

Fitness feeds back into allele frequencies in subsequent generations.

Environmental conditions modulate trait costs.

## Causal Graph

A → T

B → P

T + P → M

M → W

W → A(next generation)

W → B(next generation)

E → Cost(T)

Cost(T) → W

## Methods
### Dynamical Simulation

Forward simulations were performed over multiple generations using deterministic and stochastic evolutionary dynamics.

### Bifurcation Analysis

Parameter sweeps were conducted across mate-choice strength to identify potential critical transitions.

### Basin of Attraction Analysis

The state space of initial male trait frequencies and female preference frequencies was systematically explored.

Attractors and basin boundaries were reconstructed from simulation outcomes.

### Sensitivity Analysis

Global Sobol sensitivity analysis quantified the relative contribution of mating preference strength, trait cost, and competition intensity.

### Uncertainty Quantification

Monte Carlo simulations were used to evaluate the robustness of evolutionary outcomes under stochastic perturbations.

### Model Comparison

Alternative mate-choice functions were compared:

- Linear preference
- Exponential preference
- Logistic preference

### Distribution Matching

Simulated trait distributions were compared against reference distributions using:

- Kolmogorov–Smirnov distance
- Wasserstein distance

## Main Results
1. Bistability Emerged

The system exhibited two stable attractors:

- Low-trait equilibrium
- High-trait equilibrium

Initial conditions determined which attractor was reached.

2. Basin Boundary Detected

A separatrix divided the state space into alternative evolutionary outcomes.

Logistic approximation recovered a first-order estimate of the boundary.

Random Forest models revealed that the true boundary was nonlinear.

3. Male Trait Frequency Dominated Dynamics

The estimated basin boundary:
P(state=1)=1+exp(−(−17.40+17.85A+9.35B))

suggested that male trait frequency exerted a stronger influence on long-term outcomes than female preference frequency.

4. No Stable Polymorphism

Despite bistability, stochastic simulations consistently converged toward fixation of the preferred trait.

The model did not maintain long-term coexistence of alternative reproductive strategies.

5. Positive Feedback Alone Was Insufficient

Distribution matching analyses showed strong disagreement between simulated and empirical trait distributions.

This suggests that Fisherian runaway feedback alone is unlikely to explain persistent alternative reproductive strategies.

Additional mechanisms may be required:

- Negative frequency-dependent selection
- Conditional reproductive tactics
- Resource competition
- Density dependence

## Future Directions

The next model generation will replace a single trait allele frequency with explicit competing male strategies.

Examples include:

- Ornamented males vs sneaker males
- Territorial males vs satellite males

This extension will allow direct investigation of frequency-dependent selection and stable polymorphism.

## Technical Stack

Python

NumPy

Pandas

SciPy

Matplotlib

Scikit-Learn

SALib

NetworkX

## Motivation

This repository explores how simple causal assumptions can generate complex evolutionary dynamics. The emphasis is not only on simulation, but on connecting biological hypotheses, causal structure, dynamical systems theory, uncertainty quantification, and model validation within a reproducible research framework.

## Acknowledgement
Thanks my old friend Alexandros Kaminas discuss with me about the models. 
