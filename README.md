# Population Dynamics

Models of population dynamics built for BIOL 460.

## Contents

| Notebook | Description |
| --- | --- |
| [`notebooks/shark-tuna-model.ipynb`](notebooks/shark-tuna-model.ipynb) | Predator–prey ([Lotka–Volterra](https://en.wikipedia.org/wiki/Lotka%E2%80%93Volterra_equations)) model of sharks and tuna, simulated with SciPy's `solve_ivp`, with perturbations (sharks removed, tuna fished, one population wiped out) shown over time and on the phase plane, plus year-round fishing built into the ODE. |

The notebook walks through: tuna alone, sharks alone, both together, the oscillation, perturbations, the phase plane and flow lines, year-round fishing, complete decline, and the math behind it.

The notebook is saved with its outputs, so the plots show on GitHub without running anything.

## The model

$$S' = m\beta S T - dS$$

$$T' = bT - \beta S T$$

`S` is sharks, `T` is tuna, `b` is the tuna birth rate, `d` is the shark death rate, `beta` is the chance a meeting kills the tuna, and `m` is the sharks produced per tuna eaten. The notebook sets all four parameters to 1, so the equilibrium $(T, S) = (d/(m\beta),\ b/\beta)$ sits at $(1, 1)$.

## Running locally

Requires Python 3.9 or newer.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/shark-tuna-model.ipynb
```

Use **Kernel → Restart Kernel and Run All Cells** to rerun every cell from the top.

Run `deactivate` to leave the virtual environment when done.
