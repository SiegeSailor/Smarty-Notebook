# Smarty Notebook

This repository contains Jupyter Notebooks that use the [Smarty Cloud API](https://www.smarty.com/docs/cloud) for various common tasks. Each notebook is designed to be self-contained and easy to use:

- [x] Fetch U.S. ZIP+4 Code by Address
- [ ] Fetch International Postal Code by Address

## Using the Notebooks

You can access the notebooks directly on [GitHub.dev](https://github.dev/SiegeSailor/Smarty-Notebook), or other means of accessing Jupyter Notebooks, such as such as [GitHub Codespaces](https://github.blog/changelog/2022-11-09-using-codespaces-with-jupyterlab-public-beta/) or [Google Colab](https://colab.google/). You can also clone this project to your local machine and follow the [Setting Up a Local Environment](#setting-up-a-local-environment) section below to run the notebooks locally.

### Setting Up a Local Environment

Follow the steps below to set up your local environment for development.

#### Prerequisites

- [`pyenv`](https://github.com/pyenv/pyenv): 2.6.5
- [`pyenv-virtualenv`](https://github.com/pyenv/pyenv-virtualenv): 1.2.4

#### Setting Up a Virtual Environment

Create a virtual environment for the project:

```shell
pyenv install 3.11.13
pyenv virtualenv 3.11.13 smarty-notebook
pyenv activate smarty-notebook
pip install poetry==2.2.1
```

> [!Tip]
> You can use `pyenv local smarty-notebook` to set the virtual environment for the current directory.

> [!Tip]
> You can use `pyenv uninstall smarty-notebook` to remove the virtual environment.

#### Installing Dependencies

To install the required dependencies, run the following command:

```shell
poetry install
```

#### Verifying the Installation

`pyenv version` should show output similar to the following:

```shell
smarty-notebook (set by PYENV_VERSION environment variable)
```

`poetry env info` should show output similar to the following:

```shell
Virtualenv
Python:         3.11.13
Implementation: CPython
Path:           /Users/user/.pyenv/versions/3.11.13/envs/smarty-notebook
Executable:     /Users/user/.pyenv/versions/3.11.13/envs/smarty-notebook/bin/python
Valid:          True

Base
Platform:   darwin
OS:         posix
Python:     3.11.13
Path:       /Users/user/.pyenv/versions/3.11.13
Executable: /Users/user/.pyenv/versions/3.11.13/bin/python3.11
```

`poetry show` should list the installed packages similar to the following:

```shell
certifi            2025.10.5   Python package for providing Mozilla CA Bundle.
charset-normalizer 3.4.4       The Real First Universal Charset Detector. Open, modern and actively maintained alternative to Chardet.
idna               3.11        Internationalized Domain Names in Applications (IDNA)
numpy              2.3.3       Fundamental package for array computing in Python
pandas             2.3.2       Powerful data structures for data analysis, time series, and statistics
python-dateutil    2.9.0.post0 Extensions to the standard Python datetime module
python-dotenv      1.2.1       Read key-value pairs from a .env file and set them as environment variables
pytz               2025.2      World timezone definitions, modern and historical
requests           2.32.5      Python HTTP for Humans.
six                1.17.0      Python 2 and 3 compatibility utilities
tzdata             2025.2      Provider of IANA time zone data
urllib3            2.5.0       HTTP library with thread-safe connection pooling, file post, and more.
```

#### Supplying Smarty API Credentials

To use the Smarty API, you need to provide your [key pairs](https://www.smarty.com/docs/cloud/authentication#keypairs). You can do this by creating a `.env` file with the following environment variables:

```shell
SMARTY_AUTH_ID="<smarty_auth_id>"
SMARTY_AUTH_TOKEN="<smarty_auth_token>"
```

> [!Note]
> You can obtain a free Smarty account and generate key pairs at [Smarty Sign Up](https://www.smarty.com/signup). You will see **API Keys** under your account dashboard. See the screenshot for _Smarty - Account - Dashboard - API Keys - Secret Keys_:
> ![Smarty - Account - Dashboard - API Keys - Secret Keys](./images/smarty-account-dashboard-api_keys-secret_keys.png)
