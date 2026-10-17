# Population Dynamics

Models of population dynamics built for BIOL 460.

## Contents

| Notebook | Description |
| --- | --- |
| [`notebooks/shark-tuna-model.ipynb`](notebooks/shark-tuna-model.ipynb) | Predator–prey (Lotka–Volterra) model of sharks and tuna, simulated with SciPy's `solve_ivp`, with perturbations (sharks removed, tuna fished, one population wiped out) shown over time and on the phase plane, plus year-round fishing built into the ODE. |

## Running locally

Requires Python 3.9 or newer.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/shark-tuna-model.ipynb
```
