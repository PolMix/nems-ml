Use code in `input_parameter_generator.ipynb` to generate a single batch of 8 input parameters for FEM simulations. As an output, this notebook returns .txt file of specified format that is appropriate to be put into FEM simulation software (note that this format may vary for different FEM software).

**How to use**:
1. launch notebook
2. if required specify range and number of generated samples
3. follow the notebook
4. if required you may modify format of the output data
5. download saved file and put it into your FEM software as input parameter values

If required, you may specify range of each parameter and number of samples in each batch (default number is ~200).

Note that parameter limitations are applied for some parameters (e.g. "Temperature (K)"). You may turn it off manually by deleting that part of code.
