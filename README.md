# Jupyter Notebook for OOD Deployment on UoL General Compute

This app has been derived from the app shared by FAS-RC, which was derived from the template provided by the OSC OpenOnDemand Team, and has been modified for UoL use.<br>
[RAS-RC](https://github.com/fasrc/ood-jupyter-app)<br>
[OSC](https://github.com/OSC/bc_example_jupyter)

It launches a JupyterLab or Notebook server within a batch job.

## Prerequisites
This Batch Connect app requires the following software be available on **compute nodes** :

- [Miniforge3](https://github.com/conda-forge/miniforge/) This is installed in /opt
- [Jupyter Lab and Notebook](http://jupyter.readthedocs.io/en/latest/) These are installed in to the Miniforge location with a directory/environment for each jupyterlab version. 

It is assumed jupyterlab, notebook, jupyter-resource-usage and nb_conda_kernels have been installed on the host in a Python virtual environment.

The CONDA_EXE environment varible must be set to the path of a conda executable in template/script.sh.erb.
nb_conda_kernels will use the conda executable directly to search for additional kernels installed in the users' conda environments, but otherwise the conda environment containing the conda executable will not be used.

## Install

This repo is deployed by Ansible to /var/www/ood/apps/sys/ on the ondemand node.<br>
The form and submit files can be overriden by files in /etc/ood/config/apps/...

