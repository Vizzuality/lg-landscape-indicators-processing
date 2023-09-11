lg-landscape-indicators
==============================

LandGriffon Landscape Level Indicators

Scripts to compute land use change indicatiors on earthengine.

Requires an EarthEngine service account. Put service account json, project name,
and export bucket in ``.env`` file.

--------

## Setup

### The environment

To run the notebooks you need to create an environment with the dependencies. There are two options:

#### Docker

If you have [docker](https://docs.docker.com/engine/install/) in your system,
you run a jupyter lab server with:

``` bash
docker compose up --build
```

And if you want to get into the container, use a terminal in jupyter lab,
vscode remote development or run this command:

```shell
docker exec -it lg_landscape_indicators_notebooks /bin/bash
```

#### Conda environment

Create the environment with:

``` bash
mamba env create -n lg_landscape_indicators -f environment.yml
```

This will create an environment called lg-landscape-indicators with a common set of dependencies.

### `git` (if needed) and pre-commit hooks

If this project is a new and standalone (not a module in a bigger project), you need to initialize git:

``` bash
git init
```

If the project is already in a git repository, you can skip this step.

To install the **pre-commit hooks**, with the environment activated and in the project root directory, run:

``` bash
pre-commit install
```

## Update the environment

If you need to update the environment installing a new package, you simply do it with:

``` bash
mamba install [package]  # or `pip install [package]` if you want to install it via pip
```

then update the environment.yml file so others can clone your environment with:

``` bash
mamba env export --no-builds -f environment.yml
```
