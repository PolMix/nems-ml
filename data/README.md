# General
Here you can find all data and notebooks conserning generating, processing and visual inspection of datasets.

# Notebooks
### `data_formatting.ipynb`
This notebook concerns processing data frow raw format to a more convenient for machine learning one.

Note: you need to make sure that raw dataset file is present at `data/raw` (this is true by default).

Options:
- You can choose any dataset from `data/raw`. For this just replace the default name of raw dataset (`Dataset.txt` by default) with preferred name in the notebook
- You can specify parameter limitations for your experiments

### `data_review.ipynb`
Here you may make a visual inspection of processed dataset: both X and Y data are represented and visualized individually.

Note: you need to make sure that raw dataset file is present at `data/processed` (true by default).

# Folders
### `raw`
Here raw data taken right after FEM simulations are presented.

### `processed`
Here you can find processed FEM simulation data. Convertion of raw data into processed one is performed by means of notebook `data_formatting.ipynb`.

### `lognorm_generator`
Here notebook for generating single input batch for FEM simulation is located. See details in `lognorm_generator/README.md`.
