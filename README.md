# eddy - Extracting Disk DYnamics

[![status](http://joss.theoj.org/papers/2868c5ad4b6405eba1aaf1cd8ea53274/status.svg)](http://joss.theoj.org/papers/2868c5ad4b6405eba1aaf1cd8ea53274)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.1440052.svg)](https://doi.org/10.5281/zenodo.1440052)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/fc14f5eca31c418388424d4ec38a604b)](https://www.codacy.com/app/richteague/eddy?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=richteague/eddy&amp;utm_campaign=Badge_Grade)

`eddy` is a suite of Python tools to recover precise rotation profiles of protoplanetary disks from Doppler shifted line emission. `eddy` makes fitting of first moment maps and the inference of a rotation velocity from an annulus of spectra a breeze.

## Installation

To install the `eddy` packge, first clone the directory, then in the main directory,

```
pip install .
```

The only real dependencies for this are `numpy`, `scipy`, `matplotlib`, [`emcee`](https://github.com/dfm/emcee) and [`corner`](https://github.com/dfm/corner.py). If you want to run the Gaussian Process method you will also need [`celerite`](https://github.com/dfm/celerite) which can be easily installed if you follow their [installation guide](https://celerite.readthedocs.io/en/stable/python/install/).

If things have installed correctly you should be able to run the [Jupyter Notebooks](https://github.com/richteague/eddy/tree/master/docs) with no errors. If something goes wrong, please [open an issue](https://github.com/richteague/eddy/issues/new).

Something which is `pip` installable is currently work in progress.

## Useage

For guides on how to use `eddy` you will find extensive examples in the [documents](https://github.com/richteague/eddy/tree/master/docs).

In brief, `fit_annulus` contains the functionality to infer the rotation profile from an annulus of Doppler shifted spectra, as discussed in [Teague et al. (2018a,](https://ui.adsabs.harvard.edu/#abs/2018ApJ...860L..12T/abstract)[b)](https://ui.adsabs.harvard.edu/#abs/2018ApJ...868..113T/abstract). Functions to fit the rotation map (we shameless recommend [bettermoments](https://github.com/richteague/bettermoments) to make these), including a flared surface geometry can be found in `fit_cube`. This also contains the functionality to deproject images using the geometrical properties of the best fit model.

## Attribution

If you use `eddy` as part of your research, please cite the [JOSS paper](http://joss.theoj.org/papers/10.21105/joss.01220):

```
@article{eddy,
    doi = {10.21105/joss.01220},
    url = {https://doi.org/10.21105/joss.01220},
    year = {2019},
    month = {feb},
    publisher = {The Open Journal},
    volume = {4},
    number = {34},
    pages = {1220},
    author = {Richard Teague},
    title = {eddy},
    journal = {The Journal of Open Source Software}
}
```

If you made use of the MCMC and Gaussian Processes, then please also cite these dependancies which really made it happen:

```
@article{emcee,
    author = {{Foreman-Mackey}, D. and {Hogg}, D.~W. and {Lang}, D. and {Goodman}, J.},
    title = {emcee: The MCMC Hammer},
    journal = {PASP},
    year = 2013,
    volume = 125,
    pages = {306-312},
    eprint = {1202.3665},
    doi = {10.1086/670067}
}

@article{celerite,
    author = {{Foreman-Mackey}, D. and {Agol}, E. and {Angus}, R. and
              {Ambikasaran}, S.},
    title = {Fast and scalable Gaussian process modeling
             with applications to astronomical time series},
    year = {2017},
    journal = {AJ},
    volume = {154},
    pages = {220},
    doi = {10.3847/1538-3881/aa9332},
    url = {https://arxiv.org/abs/1703.09710}
}
```
