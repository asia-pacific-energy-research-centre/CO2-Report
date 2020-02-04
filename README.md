[![GitPitch](https://gitpitch.com/assets/badge.svg)](https://gitpitch.com/asia-pacific-energy-research-centre/aperc-data-science-project/master?p=pitchme&grs=github)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/asia-pacific-energy-research-centre/aperc-data-science-project/master?urlpath=lab)

# APERC CO2 Report

This repository contains data and notebooks to produce the analysis and figures in the 2020 APERC CO2 Report. 

The report is expected to be published in June 2020.

## Using Conda

### Creating the Conda environment

After adding any necessary dependencies to the Conda `environment.yml` file you can create the 
environment in a sub-directory of your project directory by running the following command.

```bash
$ conda env create --prefix ./env --file environment.yml
```

Once the new environment has been created you can activate the environment with the following 
command.

```bash
$ conda activate ./env
```

Note that the `env` directory is *not* under version control as it can always be re-created from 
the `environment.yml` file as necessary.

### Updating the Conda environment

If you add (remove) dependencies to (from) the `environment.yml` file after the environment has 
already been created, then you can update the environment with the following command.

```bash
$ conda env update --prefix ./env --file environment.yml --prune
```

### Listing the full contents of the Conda environment

The list of explicit dependencies for the project are listed in the `environment.yml` file. To see the full list of packages installed into the environment run the following command.

```bash
conda list --prefix ./env
```

## Using Docker

In order to build Docker images for your project and run containers you will need to install 
[Docker](https://docs.docker.com/docker-for-windows/install/) and 
[Docker Compose](https://docs.docker.com/compose/install/).

Detailed instructions for using Docker to build and image and launch containers can be found in 
the `docker/README.md`.
