# Python Libraries we have written

## Which repositories?

Some of our repositories are used as libraries and included as a requirement in other repositories.
eg https://github.com/OpenDataServices/flatten-tool/releases

For these libraries, we want to version them to make it easier to do this.

Some of our Libraries are:

 *  Flatten-Tool [GitHub](https://github.com/OpenDataServices/flatten-tool) [PyPi](https://pypi.org/project/flattentool/)
 *  Lib-Cove [GitHub](https://github.com/OpenDataServices/lib-cove) [PyPi](https://pypi.org/project/libcove/)

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

[Read our how to guide on this](/howto/release-python-library.md) 

## Changelog

All repositories that are versioned using the scheme described on this page should keep a changelog. A file called CHANGELOG.md should be in the root of the repository.

Definitions of sections, terms and format can be found at https://keepachangelog.com/en/1.0.0/; read this before adding to a changelog (it's short, don't worry!)

To start a new repository that has no releases, the initial changelog should be:

```
# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]
```


## Regular Maintenance

You may want to use the check-manifest tool to double check the MANIFEST.in file. https://pypi.org/project/check-manifest/

## OCP

We work on OCP repositories that are also versioned and released as libraries. 
[See their docs for more](https://ocds-standard-development-handbook.readthedocs.io/en/latest/coding/index.html#python-packages). 

