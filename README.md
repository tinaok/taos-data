# TAOS project data accces Demonstration

## Accesing  data stored on an HPC server in Ifrmeer, [DATARMOR](https://pcdm.ifremer.fr/Equipement) from cloud enviromment.  

This repository is made to make an demonstration of data access in TAOS project (link to website of taos here?).  
This repository is meant to demonstrate data access to the DATARMOR HPC server from cloud enviroment. The datalake at the HPC center is only open to HPC users. Recently, DATARMOR has taken a huge step in opening access to certain data using HTTPS. For Pangeo (Xarray) users, loading numerous files can take a long time. Here, we show a demo of optimized data access using Kerchunk and Intake.

### Access to physical oceanography model data
[MARC](https://marc.ifremer.fr) provides a realistic replay of the coastal ocean and demonstrates the capabilities of the numerical models developed at [LOPS](https://www.umr-lops.fr). 

#### From a Binder hub
By clicking the "Binder" button here, you will have access to a Jupyter notebook. 
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/tinaok/taos-data/HEAD?urlpath=lab/tree/taos-data/notebooks/ref-marc.ipynb)
The notebook will give you the possibility to navigate and load almost all the MARC data stored on Datarmor (in total XX T, from 20XX to 2023). If your workflow is made in Xarray, you just need to copy and paste some lines demonstrated in this notebook into your workflow. 

#### From Datarmor
You can connect to jupyterhub of datarmor by clicking [this link](https://datarmor-jupyterhub.ifremer.fr/) and start your jupyter instance by specifying enviroment as /home/datawork-lops-iaocea/conda-env/pangeo-notebook_2023_03_05 

Or you can log on to datarmor and create  your own jupyterlab enviroment (or add in your existing enviroment) using following command.

micromamba create -n pangeo-notebook_2023.03.05 
micromamba install pangeo-notebook=2023.03.05 jupyterhub zstandard -n pangeo-notebook_2023.03.05 -c conda-forge
wget https://raw.githubusercontent.com/pangeo-data/pangeo-docker-images/master/pangeo-notebook/environment.yml
micromamba install -f environment.yml  -n pangeo-notebook_2023.03.05 
micromamba activate pangeo-notebook_2023.03.05
pip install dask-hpcconfig


#### From your PC
You can create your own jupyterlab enviroment (or add in your existing enviroment) on your PC.
micromamba create -n pangeo-notebook_2023.03.05 
micromamba install pangeo-notebook=2023.03.05  zstandard -n pangeo-notebook_2023.03.05 -c conda-forge
wget https://raw.githubusercontent.com/pangeo-data/pangeo-docker-images/master/pangeo-notebook/environment.yml
micromamba install -f environment.yml  -n pangeo-notebook_2023.03.05 


## Access to TAOS project observation data (?)

demonstration of notebook in R (?) 
binder link here(?) 

## Demo of accessing in-situ /satelite data stored on DATARMOR.  
