# Add Black and isort to an existing Python repository

## Get an up to date master branch and create a new branch to do the actual work in

Using usual Git tool.

## Add black and isort to dev requirements and upgrade any locked requirements

This may be in /requirements_dev.in or setup.py or other.

Lock black to version 19.10b0 (latest version at time of writing). If there is now a later version, it's ok to lock to that.

This is so that new major versions with breaking backwards changes don't unexpectedly cause issues in pull requests. We lock to an exact version rather than 19.* to avoid a  Travis bug we saw.

**NOTE** black will only work on Python 3.6 up! 

If your Python project is meant to run on versions both below and above that you will need to do something clever to install it on some versions only. 

Or if the project is meant to run on versions below Python 3.6 only, you will not be able to add it a this stage. Your choices are to continue with this guide, adding isort only, or give up.

For example, here's how to do it in setup.py:

```
extras_require_test = ["pytest", "flake8", "isort"]

if sys.version_info[0] >= 3 and sys.version_info[1] >= 6:
    extras_require_test.append("black==19.10b0")

```
## Add .isort.cfg

See [the Code Standards reference page](/reference/python/code-standards.md) to get the contents.

Add to Git, but don't commit yet.

## Add/Update setup.cfg

See [the Code Standards reference page](/reference/python/code-standards.md) to get the contents.

Add to Git, but don't commit yet.

## Run locally

You may need to activate virtual environments and install the new dependencies you just added to do this.

        black  *.py */
        isort  --recursive *.py */



## Add to Travis install section

This is not always needed; if your lucky adding it to the normal dev requirements will take care of this.

But in some cases, you may need to add something like:

    # Black only runs under Python >= 3.6
      - if [[ $TRAVIS_PYTHON_VERSION != 3.5 ]]; then pip install black==19.10b0; fi

## Add to Travis test section



```
  - black --check *.py */
  - isort --check-only --recursive *.py */
  - flake8
```

You may need to run black on some Python versions only.

```
  - if [[ $TRAVIS_PYTHON_VERSION != 3.5 ]] && [[ $TRAVIS_PYTHON_VERSION != 3.4 ]]; then black --check *.py */; fi
```

## Update Changelog if needed

As normal.

## Git commit into one large commit

Using usual Git tool.

## Amend Author

We want people looking at Git blame later to see useful names when possible, so edit the author:

         git commit --amend --author="Automated Reformatting <code+reformatting@opendataservices.coop>"


## Git push - Travis should pass!

Test by making a new branch from the branch where you did the actual work. Edit a formatting thing, commit and push your new branch - black should fail!

Try changing some double quotes around a string to single quotes:

setup(
    name='flattentool',
    version='0.11.0',

Test by making a new branch from the branch where you did the actual work. Reordering some imports, commit and push your new branch  - isort should fail!



## Reference Pages

* [Code Standards](/reference/python/code-standards.md)
