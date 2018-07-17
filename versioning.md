Versioning our libraries
========================

Which repositories?
-------------------

Some of our repositories are used as libraries and included as a requirement in other repositories.
eg https://github.com/OpenDataServices/flatten-tool/releases

For these libraries, we want to version them to make it easier to do this.

Creating versions, and the branching scheme
-------------------------------------------

Versions are created as tags in GitHub, with the format "vX.Y.Z". Semantic versioning should be followed. https://semver.org/

Work is merged to the "master" branch, and versions are tagged directly on the master branch.

This means that when a later version is released, no bug fixes to earlier versions will be released any more.
(eg "v1.3.6" is followed by "v1.4.0" - this means there will never be a version "v1.3.7".)









