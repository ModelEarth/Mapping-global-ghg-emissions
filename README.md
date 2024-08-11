# Mapping global greenhouse gases emissions

The goal of this project is to build sankey diagrams to represent all possible calculation scopes for greenhouse gases footprints. We use EXIOBASE3 to calculate the footprints and plotly.graph_objs.sankey to build the diagrams. 

## Requirements

```bash
$ pip install -r requirements.txt
```

## Usage

Running runme.py requires 50GB of disk space as it will download all exiobase data.

```bash
$ python runme.py
```
It will:

* download EXIOBASE data and save it in Data/EXIO3
* download Kbar data and save it in Data/Kbar, convert files to .feather
* run functions from exiobase_functions.py to calculate the footprints
* run functions from sankey_function.py to generate files that will be used as inputs for building the sankey diagrams
* run save_sankey() from fig_sankey.py to generation sankey figures and save them in Results/Sankey_figs

## Application

The application to visualize all the sankey diagrams is available in another repository: https://github.com/baptiste-an/Application-mapping-GHG


## How to revert to Python 3.10 using pyenv

To run requirements.txt above, you may need Python 3.10.  Check your version using `python --version`.  
You can use pyenv to limit where you run Python 3.10. [About pyenv](https://model.earth/io/coders/python/).

For Python 3.10, right-click your local repo and open a terminal.

```bash
pyenv install 3.10  # Skip if you've already installed 3.10
pyenv local 3.10
python3.10 -m venv env  # Before re-running, delete the existing env folder, or skip this line and reuse the env folder.
source env/bin/activate  # On Windows .\env\Scripts\activate
python --version
```
Now you can continue with the requirments install above.

## Citation

Andrieu, B., Le Boulzec, H., Delannoy, L., Verzier, F., Winter, G., Vidal, O., Mapping global greenhouse gases emissions: an interactive, open-access, web application. Available at: