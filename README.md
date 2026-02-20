# binding-affinity-screening
Synthetic workflow for ligand binding affinity (4PL Kd/CI estimation) and multi-stage screening classification with visualization.

# Binding Affinity & Screening Demo Pipeline

This repository demonstrates a reproducible workflow for:

* Simulating ligand binding curves
* Estimating Kd and confidence intervals using a 4-parameter logistic (4PL) model
* Visualising binding curves
* Simulating staged biochemical screening experiments
* Classifying hits, non-binders, and anomalous signals
* Generating summary figures

All datasets in this repository are synthetic and intended for demonstration and testing purposes.

---

## Repository Structure

```
notebooks/                  Analysis notebooks (run in order)
data/synthetic/affinity/    Synthetic binding curves
data/synthetic/screening/   Synthetic screening plates
outputs/                    Generated results and figures
```

---

## Installation

Create environment and install dependencies:

```bash
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
```

---

## Running the Pipeline

Open the notebooks folder and execute in this order:

### Screening pipeline

1. 01_screening_synth_generator.ipynb
Generate staged screening experiments

2. 02_screening_piechart.ipynb
Visualize category distribution

3. 03_screening_total_scatter.ipynb
Plot screening scatter overview

### Affinity pipeline

4. 04_affinity_synth_generator.ipynb
Generate synthetic affinity curves

5. 05_affinity_4pl_fit_kd_ci.ipynb
Fit 4PL model and calculate EC50 + CI

6. 06_affinity_plot_individual_compounds.ipynb
Plot affinity curves per compound

7. 07_affinity_plot_all_compounds_panels.ipynb
Plot combined affinity panels

Generated figures appear in the `outputs/` directory.

---

## Notes

This project is designed to:

* Test analysis pipelines without experimental data
* Demonstrate hit triaging logic
* Provide a reproducible example for publications or code sharing

---

## License

See LICENSE file.
