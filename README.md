# PySyncDyn

Python package for analyzing protein dynamics through Synchronous Dynamics maps from CPMG Relaxation Dispersion Data.

## Overview

PySyncDyn automates the workflow for analyzing CPMG-RD data, including:

- Calculation of effective transverse relaxation rates (R2eff)
- Pairwise fitting using the Carver-Richards model
- Generation of Dynamic Correlation (SyncDyn) maps
- Computation and visualization of SyncDyn Scores

## Requirements

- Python 3.6+
- Required packages:

```bash
pip install pandas numpy scipy matplotlib seaborn openpyxl tqdm numba xlsxwriter scikit-learn
```

- PyMOL (for structure visualization)

## Quick Start

1. Configure your analysis parameters in `UserInput.ini`:
   - Set protein name
   - Specify list file paths
   - Define CPMG parameters
   - Set analysis options

2. Run the main workflow:

```bash
python GenSyncDyn.py -i UserInput.ini
```

3. To visualize scores in PyMOL:
   - Configure `PymolParams.ini`
   - Run:

```bash
python Score2Pymol.py -i PymolParams.ini
```

## Workflow Steps

1. `GenR2Eff.py`: Calculates R2eff values from list files
2. `PairFit.py`: Performs pairwise fitting using Carver-Richards model
3. `PlotSyncDyn.py`: Generates dynamic correlation maps
4. `Score2Pymol.py`: Visualizes scores on protein structure

 
## Contact

Manu Veliparambil Subrahmanian (mvelipar@umn.edu)
