# gyptis-binder

Binder environment for the live [gyptis](https://gyptis.gitlab.io) notebook on
[bvial.info](https://bvial.info/blog/posts/2024-02-29-gyptis/).

The page runs its code cells on [mybinder.org](https://mybinder.org) through
[Thebe](https://github.com/jupyter-book/thebe). This repository only pins the
environment, so the Binder image stays cached between visits.

- `environment.yml`: gyptis from conda-forge, pinned.
- `postBuild`: executes `gyptis.ipynb` once at build time to warm the FEniCS JIT cache.
- `start`: points live kernels at that cache and matches BLAS/OpenMP threads to the CPU quota.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/benvial/gyptis-binder/main?filepath=gyptis.ipynb)
