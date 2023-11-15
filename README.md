# SMRT_tuto_ECCC

Instead of figuring out how to run the notebook in this repository by yourself, you can try binder: [![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/m9brady/SMRT_tuto_ECCC/binder?labpath=SMRT_tuto_ECCC.ipynb)

*NB: the MyBinder service is free. It may be slow to launch and may experience downtime or general slowness due to varying system loads*

## Running this tutorial locally

You will need to have `git` installed on your system:
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

SMRT is developed with the highest stable version of Python but also work with python 2.7 series and 3.4 or higher. [Anaconda](https://www.anaconda.com/download) (or the more compact [miniconda](https://docs.conda.io/projects/miniconda/en/latest/)) is the recommended distribution to get Python as it contains numerous packages needed for scientific computations and analysis. This is an open source distribution available for Linux, Windows and MacOS.

In an anaconda/miniconda prompt, first clone this repository:
```console
git clone https://github.com/JulienMeloche/SMRT_tuto_ECCC
```

then create an virtual environment for SMRT:

```console
conda env create -f environment.yml
```

then activate the environment:

```console
conda activate jm-smrt
```

*NB: Here we use the environment name `jm-smrt` but you can choose to name your environment whatever you want with the `-n envname` argument to `conda env create`.*

With your environment ready, you have two option to install SMRT itself:

1. Install `smrt` from a cloned version of the [main SMRT GitHub repository](https://github.com/smrt-model/smrt) (recommended)
2. Install `smrt` from [pypi](https://pypi.org/project/smrt/) (not recommended due to not including latest updates)

#### 1. Install from a cloned repository
Make sure you are inside the `SMRT_tuto_ECCC` repository that you cloned earlier, and run the following commands:

```console
git clone https://github.com/smrt-model/smrt
conda activate jm-smrt
cd smrt
pip install .
cd ..
```

This will install `smrt` into the `jm-smrt` conda environment we created earlier. When you want to run the notebook, simply type:

```console
jupyter notebook SMRT_tuto_ECCC.ipynb
```

a web browser should launch and you can begin using the notebook.

If/when you need to pull the latest changes from the SMRT repository, it will be as easy as:

```console
cd /path/to/smrt_tuto_ecc/folder/smrt
conda activate jm-smrt
git fetch && git pull --ff-only
pip install . --upgrade
cd ..
```

#### 2. Install from PyPI

While this method is "simpler", you will be limited by having to wait for SMRT developers to push new updates to PyPI. To install this way:

```console
conda activate jm-smrt
pip install smrt
```

That's it! Now you should be able to run jupyter as before:

```console
jupyter notebook SMRT_tuto_ECCC.ipynb
```

#### Optional extra: the SMRT developers also provide some tutorials for SMRT that may interest you: https://github.com/smrt-model/tutorials**