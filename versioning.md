# Versioning our libraries


## Which repositories?

Some of our repositories are used as libraries and included as a requirement in other repositories.
eg https://github.com/OpenDataServices/flatten-tool/releases

For these libraries, we want to version them to make it easier to do this.


## Git, tags and branches

Versions are created as tags in GitHub, with the format "vX.Y.Z". Semantic Versioning should be followed. https://semver.org/

Work is merged to the "master" branch, and versions are tagged directly on the master branch.

This means that when a later version is released, no bug fixes to earlier versions will be released any more.
(eg "v1.3.6" is followed by "v1.4.0" - this means there will never be a version "v1.3.7".)


## Publishing a new version

We do not publish a new version every time some code is merged to master. Instead, we only publish when we need the changes 
to be released.

Whether a new version is a patch release, a minor release or a major release should be decided by 
following Semantic Versioning. https://semver.org/


## Changelog

All projects should keep a changelog. A file called CHANGELOG.md should be in the root of the repository.

It's format should follow https://keepachangelog.com/en/1.0.0/

To start a new repository that has no releases, the initial changelog should be:

```
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]
```


## Process for making a new release

These steps depend on each other so carry them out in order.

### Commit to master branch

A special commit should be made to the master branch.

This commit should:

  *  change the version number in setup.py
  *  change the version number and fix any problems with messages for this release in CHANGELOG.md

### Tag a commit

The GitHub web interface should then be used to create a new tag that points to the new commit on the master branch.

The tag should be named "vX.Y.Z".





