# Cirq Setup
**Cirq** is one of the most popular quantum computing simulators as of 2022.
[Google](https://quantumai.google/cirq) has taken special interest in it and has active contributors woking on it.

All contributions are public and done on [Github](https://github.com/quantumlib/Cirq) and are widely accesible.
Releases are also published and registered inside `pip`, which we will also use in this session.

If you are using Google Colab or have any of the setup components already installed, you can jump to `Step 3`.

## Step 0 - Python Installation
To use Cirq, we must first install Python on our machine.

### Linux - Debian/Ubuntu
A usual installation set of commands is:
```shell
$ sudo apt-get update
$ sudo apt-get install python3
```

If it fails, you can also try:
```shell
$ sudo apt-get install software-properties-common
$ sudo add-apt-repository ppa:deadsnakes/ppa
$ sudo apt-get update
$ sudo apt-get install python3
```

### Windows
Manual GUI installation:
 1. Download Python from the official [page](https://www.python.org/downloads/windows/)
 2. Follow the instructions to install it

Chocolatey approach:
```shell
choco install python
```

### MacOS
First we need to install `Homebrew`:
```shell
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Then we can install Python:
```shell
$ brew install python
```

## Step 1 - Pip Installation
To download `Cirq` we need to use the `pip` package manager.
First check if it is already installed:
```shell
$ pip help
```

If you haven't already, you can install it with:
```shell
$ curl https://bootstrap.pypa.io/get-pip.py -o get-pip.py
$ python get-pip.py
```

## Step 2 - Ipython Notebook Installation
To make it easier to work on the laboratory content we will install the `ipython` notebook format.

```shell
$ pip install ipynb
$ pip install ipykernel
```

## Step 3 - Cirq Installation
### Local Setup
To install `Cirq` we need to use the `pip` package manager:
```shell
$ pip install cirq
```

### Google Colab Setup
Google Colab already has `Cirq` installed.
Still, we can check for it using this snippet at the beginning of the notebook:
```python
    try:
        import cirq
    except ImportError:
        print("installing Cirq...")
        !pip install --quiet cirq
        import cirq
        print("Installed Cirq")
```

## Step 4 - Using Cirq
### Local Setup
Locally we can just import Cirq and everything should be ready to go:
```python
    import cirq
```

### Google Colab Setup
By running the snippet from the previous step, Cirq will be already imported.

## Step 5 - Testing Cirq
Run the included `Hello World` program provided by Cirq and check if it works.
The notebook is called `hello-world.ipynb` and is located in the `0-setup` folder.

## Uninstalling Cirq
If we want to uninstall Cirq, we can use the following command:
```shell
$ pip uninstall cirq ipynb ipykernel
```
