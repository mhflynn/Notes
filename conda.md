## Notes regarding use of conda to install python packages and create virtual environments

> These notes assume Anaconda has already been installed.  
> The perspective of these notes is on a Mac

## Contents
- [Working with virtual environments](#Working-with-virtual-environments)
  - [Create a virtual environment](#Create-a-virtual-environment)
  - [Activate a virtual environment](#Activate-a-virtual-environment)
  - [Deactivate a virtual environment](#Deactivate-a-virtual-environment)
  - [Remove a virtual environment](#Remove-a-virtual-environment)
  - [List environments](#List-environments)
  - [List environment packages](#List-environment-packages)
- [Working with Jupyter kernels](#Working-with-Jupyter-kernels)
  - [Install ipykernel in current environment](#Install-ipykernel-in-current-environment)
  - [List jupyter kernels](#List-jupyter-kernels)
  - [Uninstall a kernel](#Uninstall-a-kernel)
- [ToDo](#ToDo)
- [Helpful Links](#Helpful-links)
- [Secondary Links](#Secondary-links)

## Working with virtual environments
#### Create a virtual environment 
`conda create --name myenv`

- No packages will be installed
- The environment will use the current (conda) version of python
  - To use a specific version of python: `conda create --name myenv python=3.6`
- The directory for the virtual environment will be created under anaconda program directory
  - e.g. `~/opt/anaconda/envs/myenv`
- To specify a directory for the virtual environment: 
  - `conda create --name myenv --prefix ./myenv`

#### Activate a virtual environment
`conda activate --name myenv`

#### Deactivate a virtual environment
`conda activate` or `source deactivate`

#### Remove a virtual environment
`conda env remove --name myenv`

#### List environments
`conda env list` or `conda info envs`

#### List environment packages
`conda list`

## Working with Jupyter kernels
### Install ipykernel in current environment
`python -m pip install ipykernel`  
`python -m ipykernel install [--user] [--name <machine-readable-name>] [--display-name <"User Friendly Name">]`

### List jupyter kernels
`jupyter kernelspec list`

### Uninstall a kernel
`jupyter kernelspec uninstall myenv`

## ToDo
- Create environment and ipykernel for use with Jupyter
- Conda search and pip search
- When to use pip
- Details for conda and pip packages
- conda shell interaction [conda init]


## Helpful links
* [Understanding *conda* and *pip*](https://www.anaconda.com/blog/understanding-conda-and-pip)
* [Conda cheat sheet](https://docs.conda.io/projects/conda/en/4.6.0/_downloads/52a95608c49671267e40c689e0bc00ca/conda-cheatsheet.pdf)
* [Conda packages](https://repo.anaconda.com/pkgs/)
* [PyPI](https:/pypi.org)
* [* Using Virtual Environments in Jupyter Notebook and Python](https://janakiev.com/blog/jupyter-virtual-envs/)
* [virtualenv](https://virtualenv.pypa.io/en/latest/)
* [venv](https://docs.python.org/3/library/venv.html)

## Secondary links
* [Pipenv & Virtual Environments](https://docs.python-guide.org/dev/virtualenvs/)
