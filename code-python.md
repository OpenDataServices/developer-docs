Notes about Open Data Services Python Code
==========================================

Python2 vs Python3
------------------

We use Python 3 for new applications, and support Python 2 and 3 for libraries. We still have some legacy Python 2 only code. 

Python Minor Versions
---------------------

Where we support Python 2 we support only Python 2.7. Where we support Python 3, we generally support Python 3.3+. Generally the version of Python 3 we actually deploy with is determined by the version available in the latest Ubuntu LTS, currently 3.4.

Common Dependencies
-------------------

A lot of our software has dependencies in common:

* Django
* py.test - a no-boilerplate testing framework

Coding style
------------

Mostly this is PEP8, and the additional suggestions that Flake8 provides. Some projects e.g. Cove are automatically tested with flake8 by Travis.  We have a few exceptions, mostly inherited from the Django project, which are declared in setup.cfg, e.g. https://github.com/OpenDataServices/cove/blob/master/setup.cfg

Pinned Dependencies
-------------------

We pin all our dependencies (including dependencies of dependencies) to an exact version in requirements.txt. This makes deployment more deterministic and reproducible. It also means that we can use requires.io to track out of date dependencies.

virtualenv
----------

In order to install multiple version of the same dependency for different projects, we use [virtualenv](https://virtualenv.pypa.io/en/latest/).

Python Packages
---------------

Our libraries like flatten-tool build as Python packages, but none of these are currently on PYPI. Where other code has dependencies on these we use pip's git support to point at a particular commit.
