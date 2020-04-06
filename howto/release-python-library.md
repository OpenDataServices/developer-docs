# Releasing a Python Library

These steps depend on each other so carry them out in order.

## Update master branch

A special pull request should be made to the master branch.

This pull request should have one commit that should:

  *  change the version number in setup.py
  *  change the version number and fix any problems with messages for this release in CHANGELOG.md

Merge this pull request to master.

## Tag a commit

The GitHub web interface should then be used to create a new tag that points to the new commit on the master branch.

(You can also create a tag directly in git if you want.)

The tag should be named "vX.Y.Z".

## Publish to PyPi

Our libraries are usually also published to PyPi.

Build and upload the new version to PyPi:

    python setup.py sdist upload

(You may need a [.pypirc file](https://docs.python.org/3.6/distutils/packageindex.html#pypirc) for this to work.)


## Reference Pages

* [Libraries we have written](/reference/python/libraries-we-have-written-libs.md)