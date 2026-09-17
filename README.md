# Assignment 2: Supernova Hubble Diagram Fitting

This is the starter repository for PHYS690 Assignment 2. You will use a public Type Ia supernova data set to move from data inspection to visualization, model fitting, residual analysis, covariance interpretation, model comparison, and command-line reproduction.

The notebook downloads the public Pantheon supernova table from the Pantheon data-release repository:

```text
https://raw.githubusercontent.com/dscolnic/Pantheon/master/lcparam_full_long.txt
```

Do not commit downloaded data files, generated scratch outputs, or virtual environments.

## Repository Layout

```text
.
├── .gitignore
├── README.md
├── requirements.txt
├── figures/
│   └── .gitkeep
├── notebooks/
│   └── assignment2_supernova_hubble_diagram.ipynb
└── scripts/
    └── make_supernova_model_comparison.py
```

## Setup

Open this repository folder in VS Code and use `Terminal > New Terminal`.

On macOS:

```bash
python3 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
```

On Windows Git Bash:

```bash
python -m venv .venv
source .venv/Scripts/activate
python -m pip install -r requirements.txt
```

After installing packages, open `notebooks/assignment2_supernova_hubble_diagram.ipynb` and select the `.venv` Python kernel.

## Assignment Work

Complete the guided notebook in `notebooks/`. You will compare two reasonable modeling choices for the supernova Hubble diagram:

- a low-redshift Hubble-law model;
- a one-parameter cosmographic extension that allows curvature in the Hubble diagram.

Your final result should include model comparison diagnostics, residual plots, covariance interpretation, and a command-line script that reproduces the final figures. Save final figures in `figures/`.

You must also complete the command-line script:

```bash
python scripts/make_supernova_model_comparison.py
```

The completed script should reproduce and save the final notebook figures:

- `figures/supernova_hubble_fit.png`
- `figures/supernova_residuals.png`

It should also save a concise fit summary table, such as:

- `figures/supernova_fit_summary.csv`

You should also update this `README.md` so another person can rerun your notebook and understand what your model comparison does and does not establish.

## Submission

This repository should remain private inside the `WM-PHYS690-Fall2026` GitHub organization. Make meaningful commits as you work, then push your final work.

Finally, submit a pull request from the `submission` branch into `main` in your private assignment repository. This will inform Prof. Stevens that your submission is ready to be evaluated.
