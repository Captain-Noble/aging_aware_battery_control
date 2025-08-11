After changing these:

1. Add a terminal SoH constraint to both MPCs
e.g. ensure tilde_Q_end ≥ 0.80 · Q₁ (or equivalently l_t ≤ 0.20) at the end of each horizon.

2. Parameter sweep & trade-off plots
Vary γ over a grid, resolve each MPC, then plot
• revenue vs lifetime (arbitrage)
• RMS(Δz) vs lifetime (smoothing)
Skip or flag runs that become infeasible under the new SoH constraint.
“Efficiency / fast-charging” variant
3. Keep the ageing term and SoH constraint, but replace the price term with an efficiency metric (e.g. min ∑‖ b ‖²) to study the fast-charge/lifetime trade-off.
Extend the ageing model & run multi-cell batches
4. Parameterise chemistry (Q₁, C_max, etc.) so we can load different cells (LFP, NMC, …) and benchmark each under the same workflow.