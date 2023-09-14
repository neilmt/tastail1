
# Installation

## Setting up a user environment

As a `tastail1` user, it is easiest to install using the [mamba](https://mamba.readthedocs.io/en/latest/index.html) package manager, as follows:


1. Install mamba with the [Mambaforge](https://github.com/conda-forge/miniforge#mambaforge) executable for your operating system.
2. Open the command line (or the "miniforge prompt" in Windows).

3. mamba create -n tastail1 -c conda-forge -c neilmt tastail1
4. Activate the tastail1 mamba environment: `mamba activate tastail1`


All together:

--8<-- "README.md:docs-install-user"
### Running the example notebooks
If you have followed the non-developer installation instructions above, you will need to install `jupyter` into your `tastail1` environment to run the [example notebooks](https://github.com/arup-group/tastail1/tree/main/examples):

``` shell
mamba install -n tastail1 jupyter
```

With Jupyter installed, it's easiest to then add the environment as a jupyter kernel: 

``` shell
mamba activate tastail1
ipython kernel install --user --name=tastail1
jupyter notebook
```

### Choosing a different environment name
If you would like to use a different name to `tastail1` for your mamba environment, the installation becomes (where `[my-env-name]` is your preferred name for the environment):

``` shell
mamba create -n [my-env-name] -c conda-forge --file requirements/base.txt
mamba activate [my-env-name]
ipython kernel install --user --name=[my-env-name]
```
## Setting up a development environment

The install instructions are slightly different to create a development environment compared to a user environment:

--8<-- "README.md:docs-install-dev"

For more detailed installation instructions specific to developing the tastail1 codebase, see our [development documentation][setting-up-a-development-environment].
