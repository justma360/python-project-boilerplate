# Python Project Template

## About The Project

This is a template that uses both Conda and Pre-commit, to ensure that everyone in the team has the same environment running on their device.

Pre-commit is used to ensure that certain commit standards are enforced.

## Built With

[![python][python3.8.13-shield]][python3.8.13-url]
[![conda][conda-forge-shield]][conda-forge-url]

This template is primary focused on Python 3.8.13 with Anaconda (using Conda-forge)

# Getting Started

## Prerequisites

- Python 3.8.13
- Anaconda

## Installation

### Windows
Below is instruction on how to install the custom Conda Environment

1. Move the requirements.txt (pip) or requirements.yaml (Conda) into `setup\requirements`
2. Open the folder directory in CMD / Terminal and Run the batch file in setup accordingly

   **Conda** install
   ```
   setup\pip_setup_venv.bat
   ```
   **Pip3** install
   ```
   setup\conda_setup_venv.bat
   ```
3. You will be prompted to enter the `<env_name>`, please select a suitable name and ensure that the environment does not already exist
4. The environment will be installed and `pre-commit` will also be installed.
5. The env comes with the below as standard
   1. numpy
   2. pandas
   3. pycrypto
   4. pre-commit - installed and applied after via command line


### MacOS: **TODO**



# Flow

To effectively use the template with Pre-Commit you have to ensure that your custom env is setup:

1. Conda environment is active when using python

   **Conda** env
   ```
   conda activate <env_name>
   ```
   **Pip3** venv
   ```
   <env_name>\Scripts\activate
   ```
2. pre-commit is installed
    ```
    pre-commit install
    pre-commit autoupdate
    pre-commit install --hook-type commit-msg
    pre-commit install --hook-type pre-push
    ```

## Working as a team with Git

1. Each person should create your branch according to feature (`git checkout -b feature/AmazingNewFeature`)
2. Add your changes (`git add -A`)
3. Commit your Changes (`git commit -a 'prefix: informative commit message'`)
   ```
   prefix must follow the following
   build | ci | docs | feat | fix | perf | refactor | style | test | chore | revert | bump
   ```
4. Push to the Branch (`git push`)
5. Open a Pull Request (PR) on GitHub to develop / main

# Roadmap

## Features
- [ ] MacOS setup batch equivalent
- [ ] Implement **init**.py into template
- [ ] Add more custom utils
- [ ] Convert to flask server
- [ ] Add docker compile template

## Bugs

Please raise any bugs found to me, Thank you.

[python3.8.13-shield]: https://img.shields.io/badge/Python-3.8.13-brightgreen
[python3.8.13-url]: https://www.python.org/downloads/release/python-3813/
[conda-forge-shield]: https://img.shields.io/conda/dn/conda-forge/python?label=Anaconda
[conda-forge-url]: https://www.anaconda.com/products/distribution
