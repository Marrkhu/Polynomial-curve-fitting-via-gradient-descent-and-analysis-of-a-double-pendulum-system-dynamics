# Polynomial-curve-fitting-via-gradient-descent-and-analysis-of-a-double-pendulum-system-dynamics

## **Overview**
This notebook implements polynomial curve fitting via gradient descent and analyses a double-pendulum system’s dynamics.

---

## **Objectives**
- Implement a polynomial model (`polyModel`) and add Gaussian noise (`polyModelWithNoise`)  
- Derive and apply gradient functions for batch gradient descent  
- Track Mean Squared Error (MSE) convergence over iterations  
- Analyse the motion of the second mass in a double-pendulum (mass m₂) under high-energy initial conditions  
- Evaluate MSE versus prediction horizon for pendulum trajectories

---

## **Methodology**
- **Polynomial Fitting:**  
  - Define `polyModel(x, θ)` for evaluating polynomials  
  - Generate noisy data and perform batch gradient descent to minimise MSE  
  - Visualise true vs. fitted curves and MSE trends  

- **Double Pendulum Analysis:**  
  - Simulate or import true trajectories for mass m₂ with initial state z₀ = [π/2, 0, π/2, 0]  
  - Train a predictive model on short-sequence data to forecast future positions  
  - Compute and plot predicted vs. true (x₂, y₂) time-series  
  - Measure MSE across multiple prediction horizons

---

## **Key Results**
- **Polynomial Fitting:**  
  - MSE dipped from ~0.01 to ~0.008 by step 40 before minor fluctuations  
  - Best-fit θ parameters closely matched the true polynomial coefficients  

- **Pendulum Predictions:**  
  - x₂ trajectories captured primary oscillations accurately; y₂ displayed phase shifts and larger errors  
  - Optimal prediction horizon around 40 steps yielded minimum MSE (~0.7)  
  - Longer horizons saw MSE rise and fluctuate, indicating over-fitting on short windows

---

## **Limitations & Future Work**
- Noise level impacts gradient-descent stability; consider adaptive learning rates  
- Expand pendulum model to include joint coupling and friction  
- Test deeper recurrent architectures or physics-informed networks for longer-term forecasts

