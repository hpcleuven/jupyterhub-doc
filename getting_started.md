---
title: Getting started
nav_order: 2
---

## Logging in

### VSC accounts

The main JupyterHub server can be reached at [jupyterhub.hpc.kuleuven.be](
https://jupyterhub.hpc.kuleuven.be). You will be asked to authenticate with
your central KULeuven credentials.

### Temporary VSC accounts

For `vsctmp` accounts, the server address is [jupyterhub2.hpc.kuleuven.be](
https://jupyterhub2.hpc.kuleuven.be), where you will be prompted for a
username and password.



## Starting a server

After logging in, you will be able to launch your 'server' by selecting
a job profile and a compute project.

> **_NOTE:_** This assumes that you have at least one compute project (with
  credits) associated with your VSC account.

The list of job profiles allows you to choose between different numbers of
cores, numbers of GPUs, and walltime durations. Keep in mind that 'heavier'
jobs profiles may lead to queue times when the cluster (Genius) is being
heavily used.

After submitting your request, you will need to wait a moment until the job
has started on the cluster. Currently, the best way to check this is to
login to Genius with your VSC account and execute the `showq` command.

Then, you can navigate to the "Home" tab and access your server via the
"My Server" button.
