Here you can find the scripts which are utilized in notebooks of this repostory.

### `dataset_processing.py`
Functions for preprocessing raw dataset right after finite element method (FEM) simulations

### `dataset_preprocessing_pandas.py`
Functions for:
- splitting data into training, validation and testing set of data
- normalization of data sets

These scripts are used both for classic and neural models.

### `dataset_preprocessing_torch.py`
Class which initializes dataset object before constructing dataloaders. This method is used right after using scripts from `dataset_preprocessing_pandas.py`, only applied for neural models.

### `classic_ml.py`
Functions:
1. Estimate of time elapsed by model calculations (`get_elapsed_time` and `get_elapsed_time_tabnet`)
2. Calculation of MSE and R2 metrics for all output parameters (`calculate_metrics`)
3. Calculation of min and max values of MSE and R2 metrics on all output parameters (`get_min_max_metrics`)
4. Visualizations:
  - metrics for a model (`plot_metrics`, `plot_metrics_dense`)
  - comparison between different models' MSE and R2 metrics (`compare_models`)
  - plotting distributions of parameters (`plot_distribution`)

Also contains `CustomCV` class which can be utilized for carrying out cross-validation that supports metrics calculations on all the folds and for all parameters. It has several functions for visualization purposes.


### `neural_ml.py`
Functions:
1. Estimate of time elapsed by model calculations (`get_elapsed_time_mlp` - for MLP model, `get_elapsed_time_branched` - for BMLP model)
2. Calculation of MSE and R2 metrics for all output parameters (`calculate_metrics_torch`). This is a basic function that is ubiquitously used in other functions in this file
3. Converting calculated MSE and R2 metrics into readable format (`get_readable_metrics_mlp` - for MLP model, `get_readable_metrics_branched` - for BMLP model, `get_readable_metrics_tandem` - for tandem model (supports both X and Y parameters), `get_readable_metrics_tandem_cond` - for conditional tandem model (supports both X and Y parameters))
4. Calculation of MSE and R2 metrics on validation datasets:
  - `calculate_val_metrics_mlp` - for MLP model
  - `calculate_val_metrics_branched` - for BMLP model
  - `calculate_val_metrics_branched_sep` - for BMLP model with long branch outputs separation
  - `calculate_val_metrics_tandem` - for tandem model
  - `calculate_val_metrics_tandem_cond` - for conditional tandem model
5. Training functions:
  - `train_mlp` - for MLP model
  - `train_branched` - for BMLP model
  - `train_branched_sep` - for BMLP model with long branch outputs separation
  - `train_tandem` - for tandem model
  - `train_tandem_cond` - for conditional tandem model
  - `train_branched_wrapped` - for BMLP model with trainable loss coefficients in loss function

Also contains `ProgressPlotter` class (credit to MSU.AI team) which is utilized for plotting training loss curves in all models.

