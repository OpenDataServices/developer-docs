Python Pinned Dependencies for apps
===================================

We pin all our dependencies (including dependencies of dependencies) to an exact version in requirements.txt. This makes deployment more deterministic and reproducible.

Sometime we create a requirements.in to list the top level dependencies, with only the known version constraints. This can be used to install the latest versions of all dependencies. 

Sometimes a repo has a [script to do this](https://github.com/OpenDataServices/cove/blob/master/update_requirements.sh).

If an update script doesn't already exist, the basic procedure to add or update a requirement are:

* Update requirements.in or requirements_dev.in as needed.
* Delete the old virtual environment, and start and activate a new one. This is needed to make sure we don't have any extra packages installed.
* Run "pip install -r requirements.in" to install latest requirements.
* Run "pip freeze -r requirements.in > requirements.txt" to create a file listing the exact versions.
* Run "pip install -r requirements_dev.in".
* Run "pip freeze -r requirements_dev.in > requirements_dev.txt".
* Test!
