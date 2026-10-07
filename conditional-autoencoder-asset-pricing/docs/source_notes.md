# Source notes

## Architecture variants and thesis figures

The author confirms that Figure 4 combines results from different notebooks and recalls adding hidden layers within the same CA notebook across runs. Separate notebooks for every CA architecture are therefore not expected. The repository preserves the available source snapshots; the thesis is the record of reported results.

## Historical configurations

| Source | Context for inspection or a future rerun |
|---|---|
| CA empirical training | Multiple architecture/functions and chronological CV settings occur in the source. Select the intended version before execution. |
| CA network importance | The saved source includes Pc=5 and a short one-split configuration. Main/beta functions have the same X1-permutation calculation; the factor-network function measures changes in latent-factor variance. These implementation details should be reconciled with the desired R²-based analysis before a new run. |
| Experimental IPCA noise robustness | The saved version uses fwd_ret_excess for training and ret_excess for testing, and retains ret_excess in the feature frame. This historical configuration needs review before interpretation or reuse. |
| PCR noise robustness | PCA is followed by LinearRegression, so this is PCR. A historical importance-output basename contains ipca despite the PCR estimator. |
| Nonlinear predictive CA simulation | The saved focused source selects CA2/CA3. CA0/CA1 can have been different settings of the original experiment; their runs have not been separately matched in this portfolio edition. |
| Result aggregation | Model folders, stored HDF5 keys and some scenario labels reflect different research iterations and must be aligned when rerunning. |

The observations above describe the source snapshots; they do not establish which exact historical settings generated every final thesis result. No new model results were generated when preparing this edition.
