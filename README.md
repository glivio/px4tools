# px4tools

A log analysis toolbox for the [PX4 autopilot](http://px4.io/) written in python.

## Features

* **Flight Plotting** using standard python libraries.
* Automatic **System Identification** from log data.
* Automatic **Control Design** from log data.
* **Cross-Platform** deployment, testing, and support (Windows/OSX/Linux).
* Well integrated with **Jupyter** notebook and **Pandas**.
* Natively uses pandas **CSV format** so easily integrated with all log formats.

### px4tools Manual
https://px4tools.readthedocs.io/en/latest/#

## Install

1. Create venv
	```bash
	python3 -m venv venv
	source venv/bin/activate	
	```
2. Install dependecies
	```bash
	pip install jupyter pandas==0.23.1 matplotlib control numpy pyulog scipy
	pip install https://github.com/matplotlib/basemap/archive/master.zip
	```
3. Clone px4tools
	```bash
	git clone git@github.com:glivio/px4tools.git
	cd px4tools
	python setup.py build install
	```
4. Start jupyter notebook
	```bash
	jupyter-notebook
	```
	
## Troubleshooting
### System Identification
```bash
TypeError: No support for MIMO without slycot
```

Install slycot ```bash pip install slycot```. If you get the error ```bash ERROR: Failed building wheel for slycot```, you need to install slycot from source (see [here](https://github.com/python-control/Slycot)).
For that, you need fortran compiler (```bash sudo apt install gfortran```)

## Examples:

1. [Automatic System Identification and Control Design](https://github.com/dronecrew/px4tools/blob/master/examples/Log%20based%20System%20Identification%20and%20Control%20Design.ipynb)
2. [General Flight Data Plotting](https://github.com/jgoppert/lpe-analysis/blob/master/15-09-30%20Kabir%20Log.ipynb)
3. [ULOG basic use](https://github.com/dronecrew/px4tools/blob/master/examples/ulog%20analysis.ipynb).
4. [ULOG noise analysis](https://github.com/dronecrew/px4tools/blob/master/examples/ulog%20noise%20analysis.ipynb).
