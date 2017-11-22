# `nbconvert` Grader

An nbconvert preprocessor that grades a Jupyter notebook. To grade a notebook, you must create a grading script. Use `nbconvert` to run the grading script. The following example grades the notebook in the example directory of this project and outputs a PDF:

```bash
jupyter nbconvert --to PDF --Exporter.preprocessors=[\"nbconvert_grader.Example\"] "Example Notebook.ipynb" 
```

# Installation

```bash
pip install nbconvert_grader
```

# Development

Check out this repo on your `nbconvert` install, install from source, and enable it

```bash
# cd into the directory you checked out this project
pip install -e .
```

# Deploying

Register at https://pypi.org/ and save your credentials to `~/.pypirc`:

```
[pypi]
username:<username>
password:<password>
```

Create the distribution: 

```
python setup.py sdist
```

Use twine to upload:

```
twine upload dist/*
```

Tag and push:

```
git tag <tag>
git push origin <tag>
```
