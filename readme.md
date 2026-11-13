# Two-basin optimisation experiments

The notebooks compare Bayesian optimisation (BO-EI), CMA-ES, TuRBO-1, and
uniform random search on a two-basin objective. Discovery means observing
`f < 1`; precision means observing `f < 0.01`. Entering B's fixed center means
distance to B below `0.5`, equivalent to `f < 0.25` for the configured geometry.

Use Python 3.10 or later and install the dependencies in the notebook kernel:

```python
%pip install numpy pandas scipy matplotlib scikit-optimize cma torch gpytorch threadpoolctl ipython
%pip install git+https://github.com/uber-research/TuRBO.git
```

The second command needs Git and network access. Run Jupyter from the project
root or `code/`, keeping the notebooks beside `methods.ipynb` and
`configurations.ipynb`. Run each experiment's cells in order in a fresh kernel.

| Notebook | Purpose | Saved results |
|---|---|---|
| `code/Experiment_1.ipynb` | Compare four methods over four penalties | `code/results/experiment_1/<timestamp>/` |
| `code/Experiment 2A.ipynb` | Paired BO continuations after a 12-call miss | `code/results/experiment_2a_bo/<timestamp>/` |
| `code/Experiment_2B.ipynb` | CMA-ES population, parent count, geometry, spread, and update rules | New runs: `code/results/experiment_2b/<timestamp>/` |
| `code/Experiment_2C.ipynb` | TuRBO trust-region size and contraction | `code/results/experiment2c_sweep.jsonl` |
| `code/Experiment_3.ipynb` | Exploration and refinement after a shared initial design | `code/results/experiment_3/<timestamp>/` |

`configurations.ipynb` defines the common objective and the settings used by
Experiments 1, 2A, 2B, 2C, and 3. Existing results are retained, including previous
results that are no longer used.

Run the regression checks from the project root:

```powershell
python -m unittest discover -s code/tests -v
```
