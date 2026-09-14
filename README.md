# GEO4902

Examples and tips for GEO4902 course.


## Setting up:

To work with jupyter notebooks/python scripts for htis course there a few things that need be set up first. First, you would need to setup an envrionment to install python packages that are needed for this course. The easiest way to do it is to use miniforge (which provides conda, mamba package managers and their dependancies). If you do not have it on your machine. You can download it at [the official website](https://conda-forge.org/download/).

On Mac/Linux :

After downloading the bash script just run `bash Miniforge3-$(uname)-$(uname -m).sh` in your terminal. Check the output for suggestions on how to make conda/mamba hooks work.

For Windows:

Download and run the installer and run it. To use conda/mamba commands you will have to run them in the miniforge3  prompt, that you can access through Win Key (get startup menu)->Search->Miniforge prompt.

### Create environment

Given that conda hooks work in your terminal (Miniforge promt for Windows). You can create an environment by either using the `environment.yml` from this repo run: 

```
conda env create -f environmnet.yml
```

Or by specifying packages within the command: 
```
conda create -n geo4902 python=3.14 ipykernel xarray netcdf4 numpy scipy matplotlib cmcrameri cartopy threddsclient
```

Follow instructions how to activate geo4902 environment. 

## Running jupyter notebooks

If you use [VSCode](https://code.visualstudio.com/download). You can run notebooks there, by choosing `geo4902` as Python interpreter and as a kernel for your notebook.

If you with to run actual jupyter notebook interface or jupyter lab:
Activate the `geo4902` environment (in terminal) and jupyter packages to it:
```
conda install jupyterlab notebook
```
You might wat to register the kernel in the environment:
```
python -m ipykernel install --user --name=geo4902 --display-name "Python (geo4902)"
```
You can start the note book with `jupyter` or `jupyter lab`  commands. 

