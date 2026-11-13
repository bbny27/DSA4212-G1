DSA4212 Group 1 LaTeX report

Compile main.tex with pdfLaTeX twice from this directory, or run
latexmk -pdf main.tex

For Overleaf, upload this ZIP as a new project and set main.tex as the
main document. The eight chapter files and four vector figures are included.

Reproduce Figures 1–4
---------------------
Open DSA4212-G1_Report_Figures.ipynb in Jupyter from this directory.
Install the dependencies listed in the first cell's instructions, then
restart the kernel and run all cells. The notebook includes the full
analysis and plotting code. It uses the bundled figure_data/ logs, checks
their SHA-256 hashes, and writes the four vector PDFs to figures/.
The archive can regenerate the figures offline once the packages are
installed. The standalone notebook downloads missing logs from the pinned
repository. Recompile main.tex after regenerating the figures.

Data provenance
---------------
Repository: https://github.com/bbny27/DSA4212-G1
Commit: e2863a9c4a7d237938771be24634e8711d109616

Sections 2 and 3 use code/configurations.ipynb, code/methods.ipynb,
code/Experiment_1.ipynb, and the saved histories in
code/results/experiment_1/20261107T080438768362Z/. The extended
budget comparison uses experiment1_budget200.json and its
matched 50-call prefixes.

The global BO-EI continuation uses code/Experiment 2A.ipynb and the
larger run in code/results/experiment_2a_bo/20261107T083253056685Z/.

The CMA-ES sweeps use code/Experiment_Bec.ipynb and the saved summaries
under code/results/experiment_bec/. The update-rule comparison uses
experiments/06_mean_and_step_size_updates/ within
cmaes_two_basin_experiments/.

The trust-region sweep uses code/Experiment_2C.ipynb and
code/results/experiment2c_sweep.jsonl.

The controlled starting designs use code/Experiment_3.ipynb and
code/results/experiment_3/20261109T072157885642Z/.
