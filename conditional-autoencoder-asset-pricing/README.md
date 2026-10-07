# Enter the Autoencoder

**Conditional autoencoders, return forecasting and portfolio evaluation**  
Hans Andrias Gregoriussen · MSc Economics, University of Copenhagen · 2024

This project accompanies my master's thesis, *Enter the Autoencoder: Putting the Conditional Autoencoder Asset Pricing Model under Scrutiny*. I investigate how conditional autoencoders compare with established factor models when modelling individual stock returns and characteristic-managed portfolio returns.

The empirical study uses monthly US equity data from CRSP/Compustat over approximately 1980–2020, 94 stock characteristics and an average of around 4,120 stocks per month. It compares CA0–CA3 with IPCA, principal component regression (PCR), partial least squares (PLS), and Fama–French models.

[Read the thesis and its results](thesis/msc_thesis.pdf).

## What the project demonstrates

- **Machine learning and econometrics:** TensorFlow/Keras conditional autoencoders alongside statistical factor models.
- **Time-series validation:** chronological training, validation and test periods, regularisation and out-of-sample evaluation.
- **Forecast and strategy evaluation:** Total and Predictive R² for both individual returns r_t and portfolio returns x_t; equal/value-weighted long-short portfolios, Sharpe ratios and pricing errors.
- **Model scrutiny:** characteristic importance, separate factor/beta network analysis, and robustness to five added noise characteristics.
- **Simulation design:** linear and nonlinear five-factor data-generating processes and Monte Carlo model comparisons.

## Start here

The thesis provides the research questions, methodology, tables and figures. These notebooks provide a short route through the implementation:

| Step | Notebook | What to inspect |
|---|---|---|
| 1 | [Conditional autoencoder](notebooks/02_models/01_conditional_autoencoder.ipynb) | Beta/factor networks, hidden layers and training loops. |
| 2 | [IPCA, PCR and PLS](notebooks/02_models/02_ipca_pcr_pls.ipynb) | Benchmark estimation and return predictions. |
| 3 | [Long-short portfolios](notebooks/03_evaluation/01_long_short_portfolios.ipynb) | Turning predictions into portfolios and performance measures. |
| 4 | [CA network importance](notebooks/04_characteristic_importance/03_ca_network_importance.ipynb) | Permutation functions, network components and figure generation. |
| 5 | [CA predictive noise robustness](notebooks/05_robustness/03_ca_predictive_noise_robustness.ipynb) | Added noise inputs and evaluation across CA architectures. |
| 6 | [Linear predictive simulation](notebooks/06_simulations/03_ca_linear_predictive_r2.ipynb) | Synthetic data, model fitting and forecast evaluation. |

## Notebook organisation

| Folder | Contents |
|---|---|
| `notebooks/01_data` | Data preparation and characteristic-managed portfolios. |
| `notebooks/02_models` | Empirical CA and benchmark models; one individual-return-input variant. |
| `notebooks/03_evaluation` | Return metrics, trading portfolios and pricing errors. |
| `notebooks/04_characteristic_importance` | CA and benchmark importance analyses. |
| `notebooks/05_robustness` | Noise robustness and result aggregation. |
| `notebooks/06_simulations` | Four focused CA scenarios, benchmark simulations and result tables. |

## Research and execution context

These are historical research notebooks originally developed in Google Colab. Model depth and other settings were changed across research runs; thesis Figure 4 combines outputs from different notebooks. A saved notebook is a source snapshot rather than a complete record of every previous run.

The original research code is preserved, with saved outputs cleared and selected duplicate/debug cells omitted. Empirical notebooks refer to external SQLite/Parquet data and saved HDF5 results. They require those inputs and adaptation of the historical file paths. The simulation notebooks generate synthetic data, but the full Monte Carlo loops are substantial training jobs. This portfolio edition has not rerun the models or reproduced the thesis tables.

See [source notes](docs/source_notes.md), [data inputs](data/README.md), [dependencies](docs/dependencies.md), and [source provenance](docs/source_provenance.json) for the corresponding details.
