# silab_collections

This package aims to provide often-used routines for measurements, analysis and data visualization.

## Installation

A Python >= 3.7 installation is needed. It is recommended to create an isolated Python environment using [miniconda](https://docs.conda.io/en/latest/miniconda.html).
After doing so, install the dependencies via

    conda install numpy scipy pytables pytest matplotlib pip

Followed by 

    pip install basil_daq tqdm
    
To finally install the `silab_collections` package, activate your environment and type

    python setup.py develop

To include specific lab devices, you should clone the Basil repository and use the YAML files located at: 
    
    https://github.com/SiLab-Bonn/basil/tree/master/examples/lab_devices.

To load the YAML configuration file, you can use the following code:

    import yaml

    with open('keithley2450_pyvisa.yaml', 'r') as file:
        iv_setup = yaml.safe_load(file)
        # cv_setup = yaml.safe_load(file)

This approach is preferable to manually defining the setup in the script, as shown below:

    cv_setup = {
        'transfer_layer': 
            [...],
        'hw_drivers':
            [...]
    }

Additionally, ensure that you adapt the settings in the YAML file to match the specific device you are using.


## Examples
Check out the `examples` folder

