# README

This repo contains jupyter notebooks and data necessary to reproduce the plots included in **Using Active Learning to Improve Quasar Identification for the DESI Spectra Processing Pipeline** (Green et al. 2025). Notebooks are labeled by their figure numbers in the paper:

- `02-som.ipynb` is code for the SOM visualization used in Figure 2.
- `03-entropy.ipynb` reads in the quasarnet ensemble output, calculates the entropy as described in equation (3.2), and produces Figure 3.
- `04-05-purcom.ipynb` reads in the training history of the four QuasarNET weights files and the truth table, to produce the purity/completeness per epoch in Figure 4. It also reads in the bootstrap realizations to produce the same plot of the bootstraps, Figure 5.
- `06-ppv_tpr.ipynb` reads in the truth table and the validation results for each of the four weights files and produces a PPV/TPR curve for different confidence cutoffs (Figure 6).
- `07-08-09-results_unlabeled.ipynb` uses the results of running the eBOSS and DESI weights files on the unlabeled datasets to generate summar plots of results. This includes tests on repeat exposures (Figure 7, 8) and the redshift-redshift comparison of the two weights file outputs (Figure 9).

This repository contains all data necessary to generate all figures *except* the two tables of results on the unlabeled datasets. These two tables (`qnet_6_layers_log_v2_guadalupe.fits.gz` and `dr12_all_guadalupe.fits.gz`) should be downloaded from Zenodo (link TBW) and moved into the `data/` subdirectory to ensure they can be accessed by `07-08-09-results_unlabeled.ipynb`. 