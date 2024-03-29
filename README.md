# permmod

## What is it?

permmod is a Python package that is used to calculate the permeability of two-chamber-method measurements.
This type of measurement is based on Brace's pulse decay method and extends it to include pressure- and 
temperature-dependent material parameters. More details are available in the following paper.

## How to use it.

In order to use the package there must be a measurement-, a database- and a measurement_units-file in the following 
folder structure:
```
Measurements
│   database.csv
│   measurement_units.csv   
│
└───raw_data
│   │   measurement_file1.txt
│   │   ...
│   
└───sim_data
│   │   ...
│   
└───pics
│   │   ...
```

An example of the structure of the folders and the 3 files is given in the **example folder**. 

To evaluate a measurement, you can proceed as follows:
```sh
from permmod import Measurement

path = 'raw_data/measurement_file1.txt'
measurement = Measurement(path=path)
measurement.calculate_permeability([1e-19, 0.001], parameter='both')
```
For more information see the documentation

## Installation
The source code is hosted on GitHub at:
https://github.com/kirchma/permmod

Binary installers for the latest released version are available at the [Python
Package Index (PyPI)](https://pypi.org/project/permmod/)

```sh
# PyPI
pip install permmod
```