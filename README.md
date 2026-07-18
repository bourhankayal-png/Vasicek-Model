# Vasicek Model — PDE Pricing & Calibration

Numerical study of the Vasicek short-rate model, with a focus on the PDE pricing of zero-coupon bonds, finite-difference schemes, and calibration to a real AAA euro-area yield curve.

## Project goals

- derive the Vasicek pricing PDE from the short-rate SDE
- solve the zero-coupon bond PDE numerically
- compare implicit Euler, explicit Euler, and Crank–Nicolson
- validate the solver against the analytical formula and Monte Carlo
- study the limits of Vasicek calibration on market data

## Main features

- closed-form Vasicek zero-coupon bond solution
- finite-difference discretization in space and time
- sparse linear solves with reusable LU factorization
- stability analysis, including explicit Euler CFL instability
- time and space convergence studies
- cross-validation: PDE vs analytical vs Monte Carlo
- calibration on ECB AAA spot-rate data

## Key takeaways

- Crank–Nicolson gives the best accuracy/stability trade-off
- implicit Euler is robust but more diffusive
- explicit Euler is useful mainly as a stability benchmark
- Vasicek is pedagogical and tractable, but limited for exact curve fitting

## Tech stack

- Python
- NumPy
- SciPy
- Pandas
- Matplotlib
- Jupyter

## Repository structure

- `notebook/` — main notebook
- `figures/` — generated plots
- `data/` — market data snapshots
- `README.md` — project overview

## References

- O. Vasicek, *An equilibrium characterization of the term structure* (1977)
- Feynman–Kac representation for pricing under the risk-neutral measure
