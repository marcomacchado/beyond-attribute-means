# Beyond Attribute Means

Code to reproduce **Beyond Attribute Means: Joint First- and Second-Order Change Detection in Popular Music**.

Authors: Marco Antônio Machado and Flavio Figueiredo — Universidade Federal de Minas Gerais (UFMG).

## Data

Download MGPHot from https://zenodo.org/records/15372063 and place these files in `data/`:

- `mgphot_genes.tsv`
- `mgphot_gene_values.tsv`

See `data/README.md` for file details and the dataset citation. The analysis uses 21,299 tracks, 58 attributes and the years 1958–2022.

## Reproduce the experiments

Using Python 3.12, install the dependencies:

```sh
python -m pip install -r requirements.txt
```

From the repository directory, start Jupyter:

```sh
python -m jupyterlab
```

Open `MIR_orders_joint_paper.ipynb`, restart the kernel and run all cells in order.

The default configuration runs 5,000 bootstrap repetitions, 5,000 relational-null realizations and seven leave-one-category-out analyses. The notebook generates the manuscript's table and figures in `results/` and `figs/`.

For a short execution check, set `QUICK_CHECK = True`. This uses 10 repetitions and saves outputs separately in `quick_check/`; these outputs are not the paper's validation results.

Keep the `reference/` folder: `null_rng_start.json` initializes the null-model random sequence, and `published_validation.csv` provides comparison values for the computed results.
