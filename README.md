
# Numerical Methods in Black Hole Binary Modeling

This repository contains a computational physics project developed within the course  
**Laboratory of Computational Physics**, held at the **University of Padova** during the academic year **2022–2023**.

The project was carried out under the supervision of **Prof. Giuliano Iorio**.

---

## Project overview

The aim of this project is the **estimation and analysis of time delays in merging binary black hole systems**, with a strong focus on **numerical methods, data analysis, and computational efficiency** rather than on observational astronomy.

Starting from populations of stellar binaries generated with the **SEVN** framework, we studied the formation and merger times of binary black holes by combining:

- **Deterministic numerical integration**
- **Adaptive time-step methods**
- **Machine learning regressors**
- **Statistical analysis of distributions**

The project represents an example of how **computational physics techniques** can be applied to complex physical systems characterized by large time scales and nonlinear dynamics.

---

## Physical and computational background

The total merger delay time is defined as:

\[
t_{\text{delay}} = t_{\text{form}} + t_{\text{GW}}
\]

where:
- \( t_{\text{form}} \) is the time required for stellar binaries to evolve into a black hole binary,
- \( t_{\text{GW}} \) is the gravitational-wave driven merger time.

The gravitational-wave time \( t_{\text{GW}} \) is computed by solving **Peters’ equations** for orbital decay and circularization, which describe the evolution of:
- semi-major axis
- orbital eccentricity

---

## Implemented methods

### Numerical integration

The following numerical solvers were implemented and compared:

- **Euler method**
- **Fourth-order Runge–Kutta (RK4)** (used as benchmark)
- **Adaptive time-step schemes**, designed to handle extremely large time scales efficiently

The adaptive approach was essential to balance **precision, memory usage, and execution time**.

---

### Machine learning approaches

To reduce computational cost, we also implemented **data-driven surrogate models**:

- **XGBoost Regressor**
- **Deep Neural Network (DNN)**

The ML models were trained on synthetic datasets generated from the numerical RK4 solutions and were designed to predict merger times without explicitly solving the differential equations.

Among the tested models, **XGBoost achieved the best compromise between accuracy and computational speed**, making it a strong alternative to full numerical integration when large datasets are involved.

---

## Data analysis

The distributions of merger time delays were analyzed using different binning strategies:

- Fixed logarithmic binning
- **Bayesian Blocks**, a non-arbitrary and data-adaptive method widely used in astrophysics

The analysis confirmed:
- Power-law behavior of the time-delay distributions
- Convergence of the exponent toward the theoretically expected value
- Dependence of merger probability on metallicity

---

The notebooks include:
- Numerical solvers for Peters’ equations
- Machine learning training and validation
- Statistical analysis and visualization of results

---

## Scope and skills demonstrated

Although the physical system studied involves black holes, the core focus of this project is on:

- Numerical methods for differential equations
- Adaptive algorithms for stiff and long-time-scale systems
- Machine learning as a computational accelerator
- Statistical analysis of complex distributions
- Scientific Python workflow

This project is therefore intended as a **computational physics portfolio project**, rather than a specialization in astrophysics.

---

## References

- G. Iorio et al., *Compact object mergers: exploring uncertainties from stellar and binary evolution with SEVN*, MNRAS (2023)
- Peters, P. C., *Gravitational Radiation and the Motion of Two Point Masses*, Phys. Rev. (1964)


