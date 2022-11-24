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

Firstly, you will need to install twine for uploads. This may not be a dev requirement of a project, and you may need to install it yourself:

    pip3 install twine

Build the new version:

    python setup.py clean --all
    python setup.py sdist bdist_wheel

(It's important to clean before building, as if you don't sometimes files from previous builds that have now been deleted can still end up in the new builds!)

At this stage you may want to look in "dist" directory, and check the new version by hand.

Upload the new version to PyPi:

    twine upload dist/PACKAGE-NAME-VERSION.tar.gz dist/PACKAGE_NAME-VERSION-py3-none-any.whl

(You may want a [.pypirc file](https://docs.python.org/3.6/distutils/packageindex.html#pypirc) to avoid typing your password every time.)


## Reference Pages

* [Libraries we have written](/reference/python/libraries-we-have-written-libs.md)
