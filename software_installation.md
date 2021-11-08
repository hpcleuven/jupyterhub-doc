---
title: Software installation
nav_order: 4
---

## User-defined kernels

The standard kernels in our JupyterHub setup include Python 3.6 and R 3.6.3,
both with only few packages installed. These are sufficient for demonstration
purposes, but may not contain specific packages that you may require. As a
solution, you may set up your own kernel based on one of your local environments.

We will illustrate this process for both a MiniConda-installed Python and R environment.
Please consult the [VscDocumentation page on Python package management](
docs.vscentrum.be/en/latest/software/python_package_management.html) or the
[VscDocumentation page on R package management](
https://docs.vscentrum.be/en/latest/software/r_package_management.html) for
MiniConda installation instructions.

### Environment creation: Python

We will create a MiniConda environment with the following Python packages:

- `python 3.9`
- `numpy`
- `scipy`
- `pandas`
- `tensorflow-gpu`
- `ipykernel`

> **_NOTE:_** Instead of creating a new environment you can also introduce
  an existing environment to your JupyterHub. In this case you can skip the
  creation of the environment.
> **_NOTE:_** Always include the ipykernel package in your environment, 
  as this is necessary to install the kernel. 


1. Create a new Conda environment (here named `p27env`):
   ```
   conda create -n p39env python=3.9 numpy scipy pandas tensorflow-gpu ipykernel
   ```

2. Activate the environment:
   ```
   conda activate p39env
   ```

3. Install the associated IPython kernel in ``${VSC_HOME}/.local`` so that
   JupyterHub can find it:
   ```
   python -m ipykernel install  --prefix=${VSC_HOME}/.local/ --name 'p39env'

4. Connect to JupyerHub and verify that the new 'p39env' kernel appears.
   It should look like this: ![](./images/jupyter_envs.PNG)

5. Test the environment and make sure that it works as expected.


### Environment creation: R
 
For R, let's create an environment with following packages, and let's name it r41env:

- `R 4.1`
- `data.table`
- `ggplot2`
- `factoextra`
- `irkernel`
- `jupyter_client`

> **_NOTE:_** Instead of creating a new environment you can also introduce
  an existing environment to your JupyterHub. In this case you can skip the
  creation of the environment.
> **_NOTE:_** Always include the jupyter_client and the irkernel package, to be 
  able to install the kernel. 

1. Create the new R environment: 
  ```
  conda create -n r41env r-base=4.1 r-data.table r-ggplot2 r-factoextra r-irkernel jupyter_client -c conda-forge
  ```
2. Activate the environment:
  ```
  conda activate r41env
  ```   
3. Install the kernel in ``$VSC_HOME/.local`` to be able to use it in JupyterHUB:
  ```
  Rscript -e 'IRkernel::installspec(prefix="${VSC_HOME}/.local/", name="r41env", displayname="r41env")'
  ```
4. Connect to JupyterHUB and verify if you can find your newly created R environment in the kernel list.
