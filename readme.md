# Two-basin optimisation experiments

This project compares Bayesian optimisation, CMA-ES, TuRBO-1, and random search on a two-basin objective. We study whether each method finds the better basin and how well it refines a solution afterwards.

- **Experiment 1** compares the methods across different penalty strengths.
- **Experiment 2A** tests whether more exploration helps BO recover after an early miss.
- **Experiment 2B** varies CMA-ES population size, parent count, initial spread, domain geometry, and update rules.
- **Experiment 2C** studies TuRBO's trust-region size, contraction, and restarts.
- **Experiment 3** compares exploration and refinement when the initial observations are near either basin.

The notebooks are in `code/`. Shared optimisation methods are defined in `methods.ipynb`, and experiment settings are in `configurations.ipynb`.

Use a Python 3.12 environment with Jupyter or another notebook editor. Install the dependencies in the same environment as the notebook kernel:

```bash
python -m pip install numpy pandas scipy matplotlib scikit-optimize cma torch gpytorch threadpoolctl ipython jupyter
python -m pip install git+https://github.com/uber-research/TuRBO.git
```

The second command requires Git. Open the notebooks from the project root or the `code/` folder, then run each notebook's cells in order from a fresh kernel. The shared notebooks are loaded automatically.

Saved results are under `code/results/`, grouped by experiment. Experiment 2C resumes completed trials from its checkpoint; choose a new checkpoint path in the configuration when changing its optimisation settings.
