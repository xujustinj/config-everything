# Python

In modern times, Python 2 is deprecated from this universe, so "Python" automatically refers to Python 3 (preferrably with a two-digit minor version number).

## Installation (Linux)

### Anaconda / Mamba

Anaconda is a horrid mess of a package manager that data scientists still use because they don't know any better.

Not to be confused with [the Python web framework of the same name](https://github.com/PyMamba/mamba-framework), Mamba is a performant reimplementation of Anaconda that actually works.
For any `conda ...` command, you can run `mamba ...` instead and have it finish before the heat death of the universe.

That said, if you install `mamba` directly (as I do), it will automatically alias `conda` to `mamba` so you won't even need to replace the commands.

Even on Linux, the preferred way to install Mamba is via the Miniforge installer that can be downloaded from [GitHub](https://github.com/conda-forge/miniforge).
At the time of writing, the installer is a shell script, which can be executed with the `sh` command. For example:

```sh
# this may vary depending on the exact name/path of the installer
sh ~/Downloads/Miniforge3-Linux-x86_64.sh
```

Then, in the installation:

1. agree to the license agreement
2. install to the default location
3. **Do you wish ... conda init?** = `yes`

Afterwards, it is prudent to move the installation script somewhere in case you need to inspect or reuse it later.
This repository's `.artifacts` folder is a good place for this.

### pip

After installing Anaconda, `pip` is automatically available in the base environment.
However, if you must use `pip` on its own, run the following install command.

```sh
sudo apt-get install python3-pip
```

### Rendering Jupyter Notebooks as $\LaTeX$ PDFs

In order to use `nbconvert` to render Jupyter notebooks, we need to install [Pandoc](https://pandoc.org/).

```sh
# using conda (recommended)
conda install --channel=conda-forge pandoc

# using apt
sudo apt-get install pandoc
```
