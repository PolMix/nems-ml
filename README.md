# General info
This work is devoted to numerical study of nanoelectromechanical systems (NEMS) by means of machine learning techniques. Read more about the aims of this work in file `thesis.pdf`.

Milestones of the conducted work are listed below.

# 1. Finite element method (FEM)
In order to obtain data for training machine learning models, FEM simulation results are utilized. In particular, series of NEMS configuration that vary in 8 input parameters (lenght and width of nanobeam, thickness of the 1st and the 2nd layers, temperature, gate voltage, gate distance and mechanical beam pretension) are simulated providing outputs containing 5 crucial parameters (resonant frequency, quality factor, effective mass, thermoelastic losses and mechanical noise spectral density value) of every mode from the 1st to 4th one for given inputs.

For a better control over input parameter distribution, all input parameters were preliminarily generated using code in `data/input_parameter_generator/input_generator.ipynb`. By means of this code batches of input parameters (each of \~200 elements) were generated and used as input for FEM.

# 2. Processing of raw dataset
FEM output is processed to a more conventional representation for machine learning tasks by means of code in `data/data_formatting.ipynb`. Also, anomalies of the raw dataset can be detected and eliminated.

# 3. Visual inspection of processed dataset
In `data/data_review.ipynb` input and output parameters distribution in processed dataset are visualized. On rare occasions some anomalies can be detected with the help of these visualizations.

# 4. Classic machine learning
Models used:
- `LinearRegressor` (for a baseline)
- `RandomForestRegressor`
- `TabNetRegressor` + `Optuna`
- `XGBRegressor` + `Optuna`
- `XGBRegressor` + custom `Cross Validation`

Also, custom scaler class was developed.

See details in `training/classic/README.md`.

# 5. Neural networks
Models:
- Fully Connected Networks with different architectures
- Loss-wrapped neural network

For details, see `training/neural/README.md`.
