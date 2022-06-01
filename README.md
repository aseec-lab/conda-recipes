# ASEEC Lab Conda Recipes

Some useful conda recipes we use in the ASEEC Lab at UC Davis.

## Getting Started

To build a recipe you must have `conda` and `conda-build`.

For the former, I suggest installing [Miniconda3](https://docs.conda.io/en/latest/miniconda.html). 
Once you have installed `conda`, create a new environment for builds with the following command:
```sh
conda create -n build -c conda-forge conda-build
conda activate build
```

Then, to build a recipe, go to the parent directory of the recipe you want to build, and run the following:

```sh
(export CONDA_BLD_PATH=<build-path> ; conda-build <recipe-dir>)
```
Note: if `CONDA_BLD_PATH` is not specified, the package tarbell will be installed somewhere in your conda root directory depending on the active environment.

After the tarbell is generated (it will be in the folder specified by `CONDA_BLD_PATH`), you can install it to your active environment using:
```sh
conda install <path/to/package/tarbell>
```

## Helpful Links

- [official documentation](https://docs.conda.io/projects/conda-build/en/latest/user-guide/tutorials/build-pkgs.html)
- [tutorial 1](https://python-packaging-tutorial.readthedocs.io/en/latest/conda.html)
- [tutorial 2](https://www.underworldcode.org/articles/build-conda-packages/)

But honestly one of the best ways is to look at existing recipes.

Some nice examples:
- [memfault recipes](https://github.com/memfault/conda-recipes)
- [conda-forge](https://github.com/conda-forge) (somewhat daunting)