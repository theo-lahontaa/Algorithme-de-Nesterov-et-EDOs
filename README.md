# Nesterov Algorithm and Ordinary Differential Equations

This repository presents a project studying the connection between the **Nesterov accelerated gradient method** and **second-order ordinary differential equations (ODEs)**.  
The work includes theoretical derivations, discretization via explicit Euler schemes, and numerical experiments comparing Nesterov’s method with classical gradient descent.

A full written report is provided:
**Algorithme de Nesterov et Équations Différentielles Ordinaires** :contentReference[oaicite:0]{index=0}

---

## Project Content

- Derivation of the ODE:
  $$\ddot{x}(t) + \frac{\alpha}{t}\dot{x}(t) + \nabla f(x(t)) = 0$$  
  and its discretization using explicit Euler steps.

- Comparison between:
  - Euler discretization of the ODE  
  - The update rules of Nesterov’s accelerated gradient method  

- Identification of structural differences:
  - gradient evaluated at \(x_k\) vs. extrapolated point \(y_k\)  
  - different momentum coefficients  
  - conditions under which Euler reproduces Nesterov’s recursion

- Extension to a modified ODE with viscous damping:
  $$\ddot{x} + \frac{\alpha}{t}\dot{x} + \beta \dot{x} + \nabla f(x) = 0$$  
  and recovery of Nesterov updates through suitable parameter choices.

---

## Numerical Experiments

- Comparison of **gradient descent** and **Nesterov acceleration** on  
  \(f(x) = \frac14 x^4\)

- Visualizations:
  - trajectories \(x_k\)  
  - evolution of \(f(x_k)\)  
  - effect of different values of \(\alpha\) on stability and oscillations  
  - convergence rates:  
    - GD → \(O(1/k)\)  
    - Nesterov → \(O(1/k^2)\)

- Empirical analysis of α:
  - α = 1, 2 → unstable oscillations  
  - α = 10 → slow convergence  
  - **α ≈ 3 → most balanced behaviour**

- Experiments on better-conditioned quadratic functions showing faster convergence for both methods.

---

## File Provided

- `Algorithme_de_Nesterov_et_EDOs.pdf` — complete project report (theory + numerical results)

---

## Academic Context

This project was carried out within the Master 2 MSS course  
**“Optimisation en grande dimension : approches déterministes et stochastiques”**  
at the University of Bordeaux.

