This repository contains data and notebooks for the paper [`Aging-Aware Battery Control via Convex Optimization`](https://stanford.edu/~boyd/papers/aging_aware_battery_control.html). 
![Smoothing Animation](smoothing.gif)
## Environment and Library Versions

To reproduce the results in this notebook, use the following versions:

| Library     | Version       |
|-------------|---------------|
| Python      | 3.12.2         |
| pandas      | 2.2.3          |
| numpy       | 1.26.4         |
| cvxpy       | 1.6.0          |
| matplotlib  | 3.10.0         |


### Instructions
To ensure reproducibility, create a virtual environment and install the specified versions.  
Example using `pip`:

```bash
python3 -m venv venv
source venv/bin/activate
pip install pandas==2.2.3 numpy==1.26.4 cvxpy==1.6.0 matplotlib==3.10.0


New requirements:

Add a terminal SoH constraint to both MPCs

e.g. ensure tilde_Q_end ≥ 0.80 · Q₁ (or equivalently l_t ≤ 0.20) at the end of each horizon.

Parameter sweep & trade-off plots

Vary γ over a grid, resolve each MPC, then plot
• revenue vs lifetime (arbitrage)
• RMS(Δz) vs lifetime (smoothing)

Skip or flag runs that become infeasible under the new SoH constraint.

“Efficiency / fast-charging” variant

Keep the ageing term and SoH constraint, but replace the price term with an efficiency metric (e.g. min ∑‖ b ‖²) to study the fast-charge/lifetime trade-off.

Extend the ageing model & run multi-cell batches

Parameterise chemistry (Q₁, C_max, etc.) so we can load different cells (LFP, NMC, …) and benchmark each under the same workflow.

