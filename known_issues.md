---
title: Known issues
nav_order: 3
---

### Known issues

1. When the server starts a **waiting page** is displayed. The **automatic
   forwarding** to the notebook usually fails. You have to refresh the
   page manually using your browser in this case.

2. **Servers cannot be stopped** using the web frontend:
   *  Running servers on the supercomputer can be stopped by deleting
      the corresponding job with `qdel`.
   *  Local servers cannot be killed easily at the moment. (Local servers not
      available at the moment).

3. If a job is queueing for longer than a few minutes, these will be
   automatically cancelled by JupyterHub.

4. The greeting page is generated the first time a user is visiting it. This
   has the following implications:
   * The **available credits** of the projects are **not** updated everytime
     the JupyterHub main page is opened
   * Newly allocated project might not show up in the list.
