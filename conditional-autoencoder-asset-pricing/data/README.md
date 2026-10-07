# Data inputs

The empirical notebooks use CRSP/Compustat-derived data stored as SQLite, Parquet and HDF5 files. Inputs and saved trained-model results are referenced by historical Colab paths; the datasets are not included in this repository.

Common references include tidy_finance_ML.sqlite, beta_input_CRSP.parquet, beta_input_revised_unbalanced.parquet, beta.parquet, portfolio_ret_CRSP.parquet and x_t_preprocessed.parquet. Noise robustness also refers to final_df and xt_all_dates in Parquet/HDF5 form. Evaluation notebooks load previously saved predictions and scores.

The simulation notebooks construct their own synthetic inputs. Their full settings use 100 Monte Carlo repetitions, with linear and nonlinear five-factor scenarios.
