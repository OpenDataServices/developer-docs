Notes about Open Data Services Python Code
==========================================

Python2 vs Python3
------------------

All of our currently deployed or actively developed code uses Python 3. Some libraries also support Python 2.

Python Minor Versions
---------------------

Where we support Python 2 we support only Python 2.7. Where we support Python 3, we generally support Python 3.3+. Generally the version of Python 3 we deploy with is the version available by default on that platform - generally this is Ubuntu LTS, so Python 3.4, but some of our travis-only code (e.g. schema tests) runs on 3.5.

We test libraries against all the minor versions they support, and our application code against the version it will be deployed with.

Common Dependencies
-------------------

A lot of our software has dependencies in common:

* Django
* py.test - a no-boilerplate testing framework

Coding style
------------

Mostly this is PEP8, and the additional suggestions that Flake8 provides. Some projects e.g. Cove are automatically tested with flake8 by Travis.  We have a few exceptions, mostly inherited from the Django project, which are declared in setup.cfg, e.g. https://github.com/OpenDataServices/cove/blob/master/setup.cfg

The one exception to PEP8 is line length, which can be up to 119 characters long.

You should configure Flake8 for that with a ".flake8" configuration file in the project (e.g. https://github.com/open-contracting/ocdsdata/blob/master/.flake8 ):


    [flake8]
    max-line-length = 119


Pinned Dependencies
-------------------

We pin all our dependencies (including dependencies of dependencies) to an exact version in requirements.txt. This makes deployment more deterministic and reproducible. It also means that we can use requires.io to track out of date dependencies.

Sometime we create a requirements.in to list the top level dependencies, with only the known version constraints. This can be used to install the latest versions of all dependencies. Sometimes a repo has a [script to do this](https://github.com/OpenDataServices/cove/blob/master/update_requirements.sh).

virtualenv
----------

In order to install multiple version of the same dependency for different projects, we use [virtualenv](https://virtualenv.pypa.io/en/latest/).

Python Packages
---------------

Our libraries like flatten-tool build as Python packages, but often these are not on PYPI. Where other code has dependencies on these we use pip's git support to point at a particular commit.
