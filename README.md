# Population Dynamics

Models of population dynamics built for BIOL 460.

## Contents

| Notebook | Description |
| --- | --- |
| [`notebooks/shark-tuna-model.ipynb`](notebooks/shark-tuna-model.ipynb) | Predator–prey (Lotka–Volterra) model of sharks and tuna, simulated with SciPy's `solve_ivp`, with perturbations (sharks removed, tuna fished, one population wiped out) shown over time and on the phase plane, plus year-round fishing built into the ODE. |

## The model

$$S' = m\beta S T - dS$$

$$T' = bT - \beta S T$$

`S` is sharks, `T` is tuna, `b` is the tuna birth rate, `d` is the shark death rate, `beta` is the chance a meeting kills the tuna, and `m` is the sharks produced per tuna eaten.

## Running locally

Requires Python 3.9 or newer.

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook notebooks/shark-tuna-model.ipynb
```
