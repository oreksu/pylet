# pyto
Simple python manager

Pyto abstracts over all tools you love to bring a uniform experince.

Pyto is a wrapper around other powerful tools that evolve and change, 
pyto in the same manner adapts to always use the most up-to-date convention by default.

Pyto can also be setup to used as simple project creation tool or something else.
Pyto know about all of the best tools for python and tries to use them, 
if we do not have support for some awsome tools, please open an issue.

Inspired by [cargo](https://doc.rust-lang.org/cargo/), [raco](https://docs.racket-lang.org/raco/) and [yeoman](https://yeoman.io).
Written in pure typed Python.

Whole Python ecosystem in one command line.

Even for simple projects we recommend using `pyto` as it structures all the code and makes sure all your project are consistent

Pyto works the same on all OS and has same commands.

Pyto always defaults to the newest PEPs to be shiny.
But you can ovveride behavioyr using `pyto.toml`

You live before Python 3.6? Do not have pyproject.toml? 
No problem `pyto` can be used with any setup even `distutils` !

# Info

### Project Structure

Strcuture of your project is very personal thing, however, as we are not only charming, but also very opninated manager, we decided to enforce standart project structure. You are probably already familier with it, as a large number of Python project are using same or very similar structure. Our was highly influnced by the following:

https://docs.python-guide.org/writing/structure/
https://github.com/navdeep-G/samplemod

## Todo
- Have autometic resolution of things like `setup.py` and only create them for versions that require it.
- Have generator declaration, so other can make other types of projects

## How setup looks
```shell

pyto new

Choose build:
    [*] setuptools
    [ ] poetry
    [ ] flit

```

## CLI
```shell

# initialize a new python package in current directory
# from existing setup or anew (easy to convert existing project)
pyto init

# create a new directory
pyto new NAME

# set default python
pyto set global python3

# install all packages
pyto install

# uninstall all packages
pyto uninstall

# Create new virtual env
pyto env

# run script
pyto run [--no-check] target=.

# compile code
pyto build

# clean env from unused dependencies
pyto clean

# run static checks
pyto check target=.

# generate docs
pyto docs

# extend pyto
pyto add COMPONENT

# pin python requirments
pyto pin

# publish package
pyto publish [--dry-run]
pyto publish [--testpypi]

# install locally
pyto install

# show dependency graph
pyto graph

```

--------

## Tools and what they do
- [build](https://github.com/pypa/build) : build
- [twine](https://github.com/pypa/build) : publish

- [poetry](https://github.com/pypa/build) : init build install publish dependency-tree

- [flit](https://github.com/pypa/flit) : init build install publish


--------


## Python Ecosystem


### Large Tool
- [conda](https://docs.conda.io/en/latest/)
- [pip-tools](https://github.com/jazzband/pip-tools/)

### Other
- [bumpver](https://github.com/mbarkhau/bumpver)

### Scaffolding / Package New
- [pyscaffold](https://github.com/pyscaffold/pyscaffold)
- [cookiecutter](https://github.com/cookiecutter/cookiecutter)
- [python-cli-tool-scaffold](https://github.com/dotanuki-labs/python-cli-tool-scaffold)
- [yehua](https://github.com/moremoban/yehua) - **@unmaintained**
- [carcass](https://github.com/MSAdministrator/carcass) - **@unmaintained**
- [scaffold-py](https://github.com/Aaronontheweb/scaffold-py) - **@unmaintained**
- [simplepkg](https://gitlab.com/b5n/simplepkg) - **@unmaintained**

### Versioning
- [pyenv](https://github.com/pyenv/pyenv)
- [p](https://github.com/qw3rtman/p) - **@unmaintained**
- [pew](https://github.com/berdario/pew)

### Execution
- [cpython](https://github.com/python/cpython)
- [pypy](https://www.pypy.org)
- [stackless](https://github.com/stackless-dev/stackless)
- [micropython](https://micropython.org)
- [rustpython](https://rustpython.github.io)
- [anaconda](https://www.anaconda.com)

### Packaging
History: `distutils -> setuptools -> ...`
- [distutils](https://docs.python.org/3/library/distutils.html) - **@deprecated** in favor of setuptools
- [bento](https://github.com/cournape/Bento) - **@unmaintained**

### Build
- [distutils](https://docs.python.org/3/library/distutils.html) - **@deprecated** in favor of setuptools
- [setuptools](https://github.com/pypa/setuptools)
- [build](https://github.com/pypa/build)
- [packaging](https://github.com/pypa/packaging)
- [pipenv](https://pipenv.pypa.io/en/latest/)
- [pybuilder](https://github.com/pybuilder/pybuilder)

### Dependecies
- [pip](https://github.com/pypa/pip)
- [pipx](https://github.com/pypa/pipx)
- [poetry](https://github.com/python-poetry/poetry)
- [easy_install](https://setuptools.pypa.io/en/latest/deprecated/easy_install.html) - **@deprecated** in favor of setuptools
- [rez](https://github.com/AcademySoftwareFoundation/rez)

### Publishing
- [twine](https://github.com/pypa/twine)
- [flit](https://github.com/pypa/flit)

### Environment
- [venv](https://docs.python.org/3/library/venv.html)
- [virtualenv](https://github.com/pypa/virtualenv)

### Dynamic Checks
#### Type Checker
- []

### Static Checks
#### Type Checker
- [mypy](https://github.com/python/mypy)
- [pytype](https://github.com/google/pytype)
- [pyright](https://github.com/microsoft/pyright)
- [pyre-check](https://github.com/facebook/pyre-check)
- [pyanalyze](https://github.com/quora/pyanalyze)

#### Security Checks
- [bandit](https://github.com/PyCQA/bandit)

### Linting
- [flake8](https://github.com/PyCQA/flake8)
- [pycodestyle](https://github.com/PyCQA/pycodestyle)
- [pyflakes](https://github.com/PyCQA/pyflakes)
- [mccabe](https://github.com/PyCQA/mccabe)
- [pydocstyle](https://github.com/PyCQA/pydocstyle/)
- [pylint](https://github.com/PyCQA/pylint)
- [pylama](https://github.com/klen/pylama)
- [radon](https://github.com/rubik/radon)
- [black](https://github.com/psf/black)
- [isort](https://pycqa.github.io/isort/)
- [pylava](https://github.com/pylava/pylava) - **@unmaintained**
- [autopep8](https://github.com/hhatto/autopep8)
- [pychecker](http://pychecker.sourceforge.net)
- [eradicate](https://github.com/myint/eradicate)
- [vulture](https://github.com/jendrikseipp/vulture)
- [yapf](https://github.com/google/yapf)
- [pep8ify](https://github.com/spulec/pep8ify) - **@unmaintained**

### Documentation
- [doxygen](https://www.doxygen.nl/index.html)
- [docutils](https://docutils.sourceforge.io)
- [sphinx](https://www.sphinx-doc.org/en/master/index.html)
- [autodoc](https://pypi.org/project/autodoc/)

### Testing
- [nose](https://nose.readthedocs.io/en/latest/)
- [unittest](https://docs.python.org/3/library/unittest.html)
- [tox](https://tox.wiki/en/latest/)
- [hypothesis](https://hypothesis.readthedocs.io/en/latest/)
- [pytest](https://docs.pytest.org/en/latest/)


### PEPs
- [PEP 518](https://peps.python.org/pep-0518/) - minimum build system 


## Read and Remove
- https://packaging.python.org/en/latest/key_projects/#virtualenv
- `pip install —editable .`
- [Sample Python Module](https://github.com/navdeep-G/samplemod)
- [Python Typing](https://github.com/typeddjango/awesome-python-typing)
- [Python Project Template](https://github.com/Kwpolska/python-project-template)
- [Awesome Python](https://github.com/vinta/awesome-python)
- [Testing & Packaging](https://hynek.me/articles/testing-packaging/)
- [Packaging a python library](https://blog.ionelmc.ro/2014/05/25/python-packaging/#the-structure)
- [Source distribution format](https://packaging.python.org/en/latest/specifications/source-distribution-format/)
- [PyPi publish package](https://realpython.com/pypi-publish-python-package/)


## Dev

https://click.palletsprojects.com/en/7.x/utils/
https://setuptools.readthedocs.io/en/latest/userguide/entry_point.html
