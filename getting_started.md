---
title: Getting started
nav_order: 2
---

## Logging in

### VSC accounts

The main JupyterHub server can be reached at [jupyterhub.hpc.kuleuven.be](
https://jupyterhub.hpc.kuleuven.be). You will be asked to authenticate with
your central KU Leuven credentials.

### Temporary VSC accounts

For `vsctmp` accounts, the server address is [jupyterhub2.hpc.kuleuven.be](
https://jupyterhub2.hpc.kuleuven.be), where you will be prompted for a
username and password.


## Starting a Jupyter Notebook App

After logging in, you will be able to launching a Jupyter Notebook App by
selecting a job profile and a compute project.

> **_NOTE:_** This assumes that you have at least one compute project (with
  credits) associated with your VSC account.

The list of job profiles allows you to choose between different numbers of
cores, numbers of GPUs, and walltime durations. Keep in mind that 'heavier'
jobs profiles may lead to queue times when the cluster (Genius) is being
heavily used.

After submitting your request, you will need to wait a moment until the job
has started on the cluster. Currently, the best way to check this is to
login to Genius with your VSC account and execute the `showq` command.

Then, you can navigate to the "Home" tab and access the Dashboard of your
Jupyter Notebook App via the "My Server" button.


## Running a Notebook document

In the Dashboard, you can either open one of your existing Notebook documents
(if any) or create a new one. For new Notebook documents, you will have the
choice between ones with a Python kernel or with an R kernel. These are then powered by the CPU cores
(and possibly GPU cards) allocated to your compute job on the cluster.

## Recorded tutorial

A detailed explanation and step-by-step tutorial of the JupyterHub can be found [here](https://kuleuven.mediaspace.kaltura.com/media/JupyterHub-LunchBox-2021-10-19/1_lxer6oid).
The two example notebooks used in the tutorial can be found [here](https://github.com/w-lampaert/JupyterHub_examples). 
The example conda environments created as on the [software installation page](https://github.com/hpcleuven/jupyterhub-doc/blob/master/software_installation.md) can be used
for these notebooks.

