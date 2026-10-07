# Environment notes

The historical runtime was Google Colab. No verified package lockfile is available from the uploaded material, and no model run was performed during recovery.

| Code area | Referenced dependencies |
|---|---|
| Common numerical workflow | Python, NumPy, Pandas, SciPy, scikit-learn, Matplotlib, Seaborn, tqdm |
| CA models | TensorFlow / Keras |
| Empirical and simulated IPCA | ipca |
| Parquet/HDF5 storage | pyarrow or fastparquet; PyTables (tables) |
| Raw-data notebook | R, rpy2, tidyverse/dplyr, RSQLite |
| Additional FF/panel experiments | pandas-datareader, statsmodels, linearmodels |
| Historical notebook runtime | Google Colab / IPython magic and shell commands |

Some notebooks write their own utils.py before importing it. Select the matching helper definition when extracting code. N11 contains an ace_tools import with a saved ModuleNotFoundError; replace the display helper in a future runnable revision.

Setup cells contain historical installs and upgrades rather than a consistent environment specification. N28 cell 4 uses bare `pip install parallelbar`, an IPython-style setup command that does not parse as ordinary Python. Three orphaned indented debug snippets in N32 (27/38/39) also fail standalone Python parsing and are omitted from the working copy. The focused simulation source cells pass static Python parsing after excluding their Colab commands.

Static Python parsing ignores prefixed Colab shell/magic lines and skips R cells. It does not verify library/API compatibility, data shapes, numerical correctness, or full sequential execution.
