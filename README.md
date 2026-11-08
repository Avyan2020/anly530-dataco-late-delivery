# Predicting Late Delivery at Order Placement (ANLY 530, KA1)

**Research question.** Using only information available when an order is placed, how well can a model predict late delivery, and do discrimination and calibration hold under time-ordered (rolling-origin) validation rather than a random split?

**Status.** Milestone 1 (research design and feasibility). The notebook in `notebooks/` is an exploratory data audit. Modelling is planned for Milestone 2 and the final paper.

## Data
DataCo Smart Supply Chain dataset (Constante et al., 2019), https://doi.org/10.17632/8gx2fvg2k6.5

The raw file is **not** stored here. Download it from Mendeley Data, check the license terms, and place it at:

    data/DataCoSupplyChainDataset.csv

(`data/` is git-ignored. The file is typically latin-1 encoded; the notebook handles this.)

## Environment
Python 3.10 or newer.

    python -m venv .venv
    source .venv/bin/activate        # Windows: .venv\Scripts\activate
    pip install -r requirements.txt
    jupyter notebook notebooks/01_exploratory_audit.ipynb

## Contents
- `notebooks/01_exploratory_audit.ipynb`: rows/orders, target rate by quarter, missingness, leakage audit, order-placement feature contract.
- `requirements.txt`: package requirements.
- `data/`: empty placeholder for the raw file.

## Reproducibility
Seed 42 for all randomness. Time-ordered splits are defined by calendar quarter, with all rows of an order kept in the same split.

## Contribution
Individual project by Koushik Dutta.

## Reference
Constante, F., Silva, F., & Pereira, A. (2019). *DataCo smart supply chain for big data analysis* (Version 5) [Data set]. Mendeley Data. https://doi.org/10.17632/8gx2fvg2k6.5
