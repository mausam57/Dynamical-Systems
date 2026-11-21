# Nonlinear Dynamics, Vehicle Simulation & Scientific Computing

A collection of Python simulations, state-space solvers, and phase-portrait animations developed to explore dynamical systems, structural stability, and vehicle suspension modeling.

## Featured Simulations

### 1. Reduced-Order Euler Column Buckling (Bistable Double-Well Dynamics)
* File: `simulations/euler_buckling_bistable_dynamics.ipynb`
* Overview: Models post-buckling lateral deflection of a slender column using a single-mode Duffing-type equation ($\ddot{q} + c\dot{q} - \mu q + q^3 = 0$).
* Implementation: Custom 4th-order Runge-Kutta (RK4) integrator paired with a dual-panel animation showing physical beam deflection alongside state-space trajectories ($q$ vs. $\dot{q}$) settling into stable equilibrium wells at $\pm\sqrt{\mu}$.

![Euler Buckling Simulation](assets/Euler%20Buckling.gif)

---

### 2. Nonlinear Damped Pendulum & Phase Portrait
* File: `simulations/nonlinear_pendulum_phase_portrait.ipynb`
* Overview: Simulates large-angle nonlinear pendulum motion ($\ddot{\theta} + \frac{g}{L}\sin\theta + b\dot{\theta} = 0$) across multiple initial conditions.
* Implementation: Uses `scipy.integrate.solve_ivp` (RK45) to generate synchronized real-time pendulum motion and multi-trajectory phase portraits ($\theta$ vs. $\omega$), illustrating stable spiral sinks and unstable saddle points.

![Simple Pendulum Phase Portrait](assets/pendulum.gif)

---

### 3. Non-Normal Linear Transient Growth
* File: `simulations/non_normal_transient_growth.ipynb`
* Overview: Demonstrates short-term transient energy amplification in asymptotically stable linear systems with non-orthogonal eigenvectors ($A = \begin{bmatrix} -0.009 & 1 \\ 0 & -0.01 \end{bmatrix}$).
* Relevance: Highlights why eigenvalue analysis alone can miss short-term peak responses in fluid shear flows and lightly damped mechanical structures.

---

### 4. Time-Varying 2D Half-Vehicle Dynamics (In Progress)
* File: `simulations/half_vehicle_time_varying_dynamics.ipynb`
* Overview: Simulates pitch and heave transient response of a 2D half-car suspension model with time-varying mass subjected to road bump disturbances using coupled ODE solvers in `SciPy`.

---

## Numerical Methods & Study Notebooks
Located in `numerical-methods-notes/`:
* `ode_solvers_analytical_vs_numerical.ipynb` — Comparison of analytical solutions, Forward Euler, and `solve_ivp` for 2nd-order damped linear systems.
* `matrix_diagonalization_eigendecomposition.ipynb` — Verification of similarity transforms ($D = T^{-1}AT$) and unit eigenvector normalization.
* `markov_chain_steady_state.ipynb` — Iterative state-transition convergence for discrete stochastic matrices.
* `taylor_series_approximations.ipynb` — Polynomial series convergence comparisons for $\sin(x)$, $\cos(x)$, $e^x$, and $\tan(x)$.

---

## Tools & Libraries
* Language: Python 3.11+
* Scientific Stack: `NumPy`, `SciPy` (`solve_ivp`), `Matplotlib` (`FuncAnimation`, `PillowWriter`)

---

## Acknowledgments
Several numerical methods and dynamical systems exercises in this repository were inspired by Prof. Steve Brunton's Control Bootcamp and Data-Driven Science & Engineering lecture series, with custom phase-portrait visualizations and animations implemented independently.

---

## Author
**Mausam Bista**  
Mechanical Engineering Graduate (Tribhuvan University, IOE) | Graduate Teaching Fellow  
[GitHub](https://github.com/mausam57) | [LinkedIn](https://www.linkedin.com/in/mausam-bista-23b51027a/)
