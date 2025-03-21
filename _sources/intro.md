# Welcome to the PyPSA & PyPSA-Eur workshop
*26-28 March 2025, Berlin, Germany*

This webpage contains PyPSA & PyPSA-Eur workshop materials for the colleagues from the Moldovan Ministry of Energy & the Technical University of Moldova. These materials are used as a part of the broader training program titled “Modelarea sistemului energetic al Moldovei folosind PyPSA” on behalf of the BMBF-funded Green Deal Ukraina, a project under Helmholtz-Zentrum Berlin. 

## Google Colab

You can work with the workshop materials without a local Python installation using online service [Google Colab](https://colab.google) which provides an online Python environment. This requires a Google account.

Open any jupyter notebook and click on the rocket 🚀 in the top right corner. It will launch a Colab workspace in your browser with the jupyter notebook loaded.

If that does not work download the `.ipynb` file and import it in [Google Colab](https://colab.research.google.com/)


## Setting up your Python environment locally

### Anaconda

Coordinating the compatibility between different Python software packages and
their multiple versions can be difficult! Fortunately, the problem is solved by
using a Python _distribution_ and/or _package manager_.

For instance, you can install on your computer the popular [Anaconda Python
Distribution](https://www.anaconda.com/download/).

For **Linux and MacOS users**, you can access the command line by opening the
_terminal_ program.

For **Windows users**, you should first install Anaconda (described above) or
`miniconda` (described below), which gives you access to the "Anaconda Prompt"
desktop application. Instructions for this are given on the [Anaconda
Website](https://docs.anaconda.com/anaconda/user-guide/getting-started/#write-a-python-program-using-anaconda-prompt-or-terminal).
From the Anaconda Prompt, you should be able to run `conda`.

## Managing environments with `conda`

Python coupled with a package manager provides a way to make isolated,
reproducible _environments_ where you have control over all installed packages
and configurations.

Here is [a great short article](https://medium.com/data-science/conda-essential-concepts-and-tricks-e478ed53b5b) that contains all the essential concepts and tips about using `conda`.

### Tip: use lightweight `miniconda`

Do yourself a favor --- use a lightweight installation called
[`miniconda`](https://docs.conda.io/en/latest/miniconda.html). It is very likely that you don't want the full Anaconda Python Distribution.


## Environment for this course: `workshop`

### ... with `conda` (recommended)

The latest environment specification for this course can be downloaded under the following link as a [`YAML`-file](https://en.wikipedia.org/wiki/YAML):

https://github.com/Irieo/workshop-pypsa-gdumd/blob/main/environment.yaml

There is a download button at the top-right corner.

After navigating to the folder where the `environment.yaml` file is stored ([here](https://tutorials.codebar.io/command-line/introduction/tutorial.html)'s a tutorial how to navigate with the command line),
you can reate this environment using `conda`

    conda env create -f environment.yaml

Activate this environment

    conda activate workshop

The environment has to be activated whenever you open a new terminal,
*before* starting a new Jupyter window with

    jupyter lab

### ... with `pip`

If you want to use `pip` for managing your environment, download

https://github.com/Irieo/workshop-pypsa-gdumd/blob/main/requirements.txt

There is a download button at the top-right corner.

After navigating to the folder where the `requirements.txt` file is stored,
you can install the required packages with

    pip install -r requirements.txt

This should allow you to start a new Jupyter window:

    jupyter lab

## Acknowledgements

We acknowledge funding from the German Federal Ministry for Education and Research (BMBF) under grant 03SF0715 (Green Deal Ukraine project).

More about the Green Deal Ukraine project: https://greendealukraina.org/
