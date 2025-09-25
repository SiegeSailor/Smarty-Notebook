# Smarty Notebook

This repository contains Jupyter Notebooks that use the Smarty API for various common tasks. Each notebook is designed to be self-contained and easy to use.

- [x] [Fetch U.S. ZIP+4 Code by Address](https://github.dev/SiegeSailor/Smarty-Notebook/notebooks/fetch-us-zip4-by-address.ipynb)
- [ ] Fetch International Postal Code by Address

## Setting Up Local Environment

Follow the steps below to set up your local environment for development. You can skip this section if you have other means of managing Python environments, such as GitHub Codespaces or Google Colab.

### Prerequisites

- [`pyenv`](https://github.com/pyenv/pyenv)
- [`pyenv-virtualenv`](https://github.com/pyenv/pyenv-virtualenv)

### Setting Up a Virtual Environment

To create a virtual environment for the project, you can use `pyenv` and `pyenv-virtualenv`. Follow these steps:

```bash
pyenv install 3.11.13
pyenv virtualenv 3.11.13 smarty-notebook
pyenv activate smarty-notebook
```

> [!Note]
> You can use `pyenv local smarty-notebook` to set the virtual environment for the current directory.

### Installing Dependencies

To install the required dependencies, run the following command:

```bash
pip install --requirement ./requirements.txt
```
