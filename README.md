# ML_course2

## Install/Update conda

### Either install conda

Check `https://docs.conda.io/projects/conda/en/latest/user-guide/install/index.html`.
Both miniconda and anaconda will do.

### Or update conda

```sh
conda update conda
```

## Setup conda

Run one of those depending on the shell you're using (bash by default):
- `conda init bash`
- `conda init fish`
- `conda init zsh`
- `conda init --help # for an exhaustive list of available shell`

You might need to reopen the shell window for change to occurs on osx (this
will reload the shell environment).

cf. `https://stackoverflow.com/questions/54544967/conda-init-for-conda-4-6-not-working-on-macos-mojave`

## Create the package environment

The main official and documented way to create an environment in conda is the 
following.
cf. `https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html#deactivating-an-environment`

```sh
# DO NOT RUN!
#
# Add the additional required package channels.
# $ conda config --add channels conda-forge # for nilearn only
#
# Create the package environment.
# $ conda create --name myenv python=3.7 pandas rise jupyter nilearn ...
```

In order to make such en environment sharable we have to run the following
command:


```sh
# DO NOT RUN!
# $ conda env export > environment.yml
```

This command exports os-specific packages into the environment file. Thus, 
preventing user using other platforms from installing the packages.
cf. `https://stackoverflow.com/questions/39280638/how-to-share-conda-environments-across-platforms`

Instead, create the environment file manually. You can check latest package
versions on `https://anaconda.org/`. Although setting package version is not
mandatory, this saves a lot of trouble. It's preferable to not follow the
official doc's convention of using the lastest PATCH version (using `x.x.*`
syntax). This is a bit less secure, but actually ensure future user wont use
broken package version since they're using a version you've tested.


```sh
# This creates and fills an environment.yml file through command line.

echo >environment.yml "\
name: pnplab_mlcourse
channels:
    # ...default conda channels already set up
    - conda-forge # for nilearn and rise
dependencies:
    - python=3.7
    - jupyter=1.0.0
    - rise=5.5.1
    - numpy=1.17.2
    - pandas=0.25.1
    - nilearn=0.5.2
    - matplotlib=3.1.1
"
```

Once written, you can install the environment's package on your local machine
relying on the generated file.

```sh
# The --force attribute will override previous environment with the same name
# (as set through the name attribute of the environment.yml file). Just added 
# it in order to make it easy to update dependencies later on.
conda env create --force --file environment.yml
```

Also note JupyterLab (the new official Jupyter Notebook IDE) doesn't work
(yet) with Rise, `https://github.com/damianavila/RISE/issues/270`.

## Activate the package environment

Since conda v4.4, use the following command instead of documented ones.
cf. `https://askubuntu.com/questions/1068768/when-using-conda-source-activate-env-name-doesnt-work-but-conda-activate`

```sh
conda activate pnplab_mlcourse
```

## Launch the jupyter notebook server

```sh
jupyter notebook
```



