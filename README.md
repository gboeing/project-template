# Research project template

This is a template for rapidly starting new projects that include data, code, and a LaTeX paper.

## Setup

1. Git clone this repository to your computer.
2. Open a terminal and change directories to the repository's root.
3. Run `conda create -f environment.yml` to set up the conda environment.
4. Run `conda activate env_name` to activate the environment.
5. Run `pre-commit install` to install the pre-commit hooks.
6. Run `python -m ipykernel install --user --name env_name --display-name "Python (env_name)"` to install an IPython kernel.

## Contributing guidelines

### Project organization

**Code**: keep all code in the `code` folder. Code should be type-annotated, use numpy-style docstrings, and pass all pre-commit hooks. Prefer .py Python scripts to .ipynb IPython notebooks whenever possible.

**Data**: keep all data *outside* of this repo (such as a shared Google Drive) and provide direct links (accessible only to people explicitly granted access) in the readme file at `data/README.md`.

**Paper**: keep the paper in the `paper` folder and follow the guidelines there.

**Dependencies**: ensure every (non-[standard library](https://docs.python.org/3/library/index.html)) package imported anywhere in the code is added to the `environment.yml` dependencies. Pin each dependency to its minor version.

### Workflow and quality control

Work in branches and open pull requests to propose merging your code changes into main.

Whenever you do work, first `git pull` the latest changes to your local computer.

Commit code changes frequently, and push at the end of every day you do work. If you didn't push code to Github, you didn't work on code that day.

Open a pull request on Github and confirm the CI tests have passed, then @ ping your code reviewer there when it's all passing and ready for review.

Install the pre-commit hooks locally (see setup above) and always fix any pre-commit errors (use the line numbers and error messages as hints). The pre-commit hooks in `.pre-commit-config.yaml` are automatically run by Github as a continuous integration (CI) workflow by `.github/workflows/tests.yml` for every push to main or PR opened on main. We can merge branches' pull requests into main after they pass these CI checks and receive reviewer approval. You can run the hooks manually locally with `pre-commit run -a` but they also run automatically on all `git commit` commands after you've installed them.
