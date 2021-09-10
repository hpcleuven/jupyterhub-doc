---
title: Known issues
nav_order: 3
---

### Known issues

1. After submitting a request for a Jupyter Notebook App, a waiting page
   is displayed. When the job has started and the Jupyter Notebook App is
   running, the automatic forwarding to the Dashboard usually fails.
   You have to refresh the page manually using your browser in this case.

2. Jupyter Notebook Apps cannot be stopped using the web frontend.
   Running jobs on the supercomputer can be stopped by deleting
   the corresponding job with `qdel`.

3. If a job is queueing for longer than a few minutes, these will be
   automatically cancelled by JupyterHub.

4. The greeting page is generated the first time a user is visiting it. This
   has the following implications:
   * The available credits of the projects are **not** updated everytime
     the JupyterHub main page is opened.
   * Newly allocated projects may not show up in the list.
