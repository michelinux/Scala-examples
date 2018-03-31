# Scala-examples
This repository contains some examples and simple experiments with the `scala` language.

## Notebooks

The interactive notebooks can be run interactively using [Jupyter](http://jupyter.org).

## Running the notebooks locally

### Install Anaconda

It's a complete distribution of Jupyter.[Download Anaconda](https://www.anaconda.com/download/) and install it.

### Install Scala Kernel

You can use the [jupyter-scala kernel](https://github.com/jupyter-scala/jupyter-scala). I tried the Apache Toree, but it's quite outdated.

```bash
cd /tmp
git clone https://github.com/jupyter-scala/jupyter-scala.git
cd jupyter-scala
./jupyter-scala
```

The `jupyter-scala` script will install several `jar` files in the `~/.coursier/cache`.

Verify that the new kernel is available:

```bash
jupyter kernelspec list
```

```
Available kernels:
  scala      /Users/michele/Library/Jupyter/kernels/scala
  python3    /Applications/anaconda3/share/jupyter/kernels/python3
```

### Launch the notebooks

```bash
jupyter notebook
```

## Uninstalling

```bash
conda install anaconda-clean
anaconda-clean —yes
sudo rm -rf /anaconda3/
rm -rf ~/.jupyter ~/.jupyter-scala
rm -rf ~/.coursier/cache/*
```

Edit the `~/.profile` and remove the following lines

```bash
# added by Anaconda3 5.1.0 installer
export PATH="/anaconda3/bin:$PATH"
```

Trash the `anaconda-navigator` application, which is just an alias.