About camb
==========

Home: https://camb.info/

Package license: modified LGPL

Feedstock license: BSD 3-Clause

Summary: Code for Anisotropies in the Microwave Background

Code for Anisotropies in the Microwave Background
by Antony Lewis and Anthony Challinor

Features:
  - Support for closed, open and flat models
  - Scalar, vector and tensor modes including polarization
  - Output Cl, matter transfer functions, matter power spectrum and σ8
  - Fast computation to ~0.3-0.1% accuracy, with controllable accuracy level
  - Relatively structured and easily extendable Fortran 90 code
  - Efficient support for massive neutrinos
  - Absolute computations from correctly normalized initial power spectra
  - Computation of lensed CMB power spectra and lensing potential power spectrum
  - Internally parallelized for fast execution on multi-processor machines
  - Use CAMB with CosmoMC for Monte-Carlo parameter estimation
  - Constant equation of state quintessence (or variable PPF)
  - Support for general correlated adiabatic/isocurvature initial conditions
  - Accurate full-sky calculation of lensed power spectra (astro-ph/0502425)
  - Integrated interface to HALOFIT for non-linear fitting
  - support for arbitrary neutrino mass splittings
  - For 21cm, lensing and number count power spectra see this extension
  - For perturbed recombination and effect on small-scale baryons see this extension
  - Calculation of local primordial and CMB lensing bispectra
  - Easy-to-use Python wrapper


Current build status
====================

[![Linux](https://img.shields.io/circleci/project/github/conda-forge/camb-feedstock/master.svg?label=Linux)](https://circleci.com/gh/conda-forge/camb-feedstock)
[![OSX](https://img.shields.io/travis/conda-forge/camb-feedstock/master.svg?label=macOS)](https://travis-ci.org/conda-forge/camb-feedstock)
[![Windows](https://img.shields.io/appveyor/ci/conda-forge/camb-feedstock/master.svg?label=Windows)](https://ci.appveyor.com/project/conda-forge/camb-feedstock/branch/master)

Current release info
====================

| Name | Downloads | Version | Platforms |
| --- | --- | --- | --- |
| [![Conda Recipe](https://img.shields.io/badge/recipe-camb-green.svg)](https://anaconda.org/conda-forge/camb) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/camb.svg)](https://anaconda.org/conda-forge/camb) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/camb.svg)](https://anaconda.org/conda-forge/camb) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/camb.svg)](https://anaconda.org/conda-forge/camb) |
| [![Conda Recipe](https://img.shields.io/badge/recipe-pycamb-green.svg)](https://anaconda.org/conda-forge/pycamb) | [![Conda Downloads](https://img.shields.io/conda/dn/conda-forge/pycamb.svg)](https://anaconda.org/conda-forge/pycamb) | [![Conda Version](https://img.shields.io/conda/vn/conda-forge/pycamb.svg)](https://anaconda.org/conda-forge/pycamb) | [![Conda Platforms](https://img.shields.io/conda/pn/conda-forge/pycamb.svg)](https://anaconda.org/conda-forge/pycamb) |

Installing camb
===============

Installing `camb` from the `conda-forge` channel can be achieved by adding `conda-forge` to your channels with:

```
conda config --add channels conda-forge
```

Once the `conda-forge` channel has been enabled, `camb, pycamb` can be installed with:

```
conda install camb pycamb
```

It is possible to list all of the versions of `camb` available on your platform with:

```
conda search camb --channel conda-forge
```


About conda-forge
=================

conda-forge is a community-led conda channel of installable packages.
In order to provide high-quality builds, the process has been automated into the
conda-forge GitHub organization. The conda-forge organization contains one repository
for each of the installable packages. Such a repository is known as a *feedstock*.

A feedstock is made up of a conda recipe (the instructions on what and how to build
the package) and the necessary configurations for automatic building using freely
available continuous integration services. Thanks to the awesome service provided by
[CircleCI](https://circleci.com/), [AppVeyor](https://www.appveyor.com/)
and [TravisCI](https://travis-ci.org/) it is possible to build and upload installable
packages to the [conda-forge](https://anaconda.org/conda-forge)
[Anaconda-Cloud](https://anaconda.org/) channel for Linux, Windows and OSX respectively.

To manage the continuous integration and simplify feedstock maintenance
[conda-smithy](https://github.com/conda-forge/conda-smithy) has been developed.
Using the ``conda-forge.yml`` within this repository, it is possible to re-render all of
this feedstock's supporting files (e.g. the CI configuration files) with ``conda smithy rerender``.

For more information please check the [conda-forge documentation](https://conda-forge.org/docs/).

Terminology
===========

**feedstock** - the conda recipe (raw material), supporting scripts and CI configuration.

**conda-smithy** - the tool which helps orchestrate the feedstock.
                   Its primary use is in the construction of the CI ``.yml`` files
                   and simplify the management of *many* feedstocks.

**conda-forge** - the place where the feedstock and smithy live and work to
                  produce the finished article (built conda distributions)


Updating camb-feedstock
=======================

If you would like to improve the camb recipe or build a new
package version, please fork this repository and submit a PR. Upon submission,
your changes will be run on the appropriate platforms to give the reviewer an
opportunity to confirm that the changes result in a successful build. Once
merged, the recipe will be re-built and uploaded automatically to the
`conda-forge` channel, whereupon the built conda packages will be available for
everybody to install and use from the `conda-forge` channel.
Note that all branches in the conda-forge/camb-feedstock are
immediately built and any created packages are uploaded, so PRs should be based
on branches in forks and branches in the main repository should only be used to
build distinct package versions.

In order to produce a uniquely identifiable distribution:
 * If the version of a package **is not** being increased, please add or increase
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string).
 * If the version of a package **is** being increased, please remember to return
   the [``build/number``](https://conda.io/docs/user-guide/tasks/build-packages/define-metadata.html#build-number-and-string)
   back to 0.
