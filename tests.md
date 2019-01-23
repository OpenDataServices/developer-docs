# Tests

## flake8

flake8 will test the quality of your python code. It should run before 
each commit.
You can set this up as a git hook so that it is run automatically on 
git commit.

### Set up flake8 to run on every git commit:

.. code:: bash

    flake8 --install-hook

By default this still opens your text editor to make the commit message, and prints the flake8 errors to STDOUT where you might miss them. Only show the flake8 errors and not open the editor (until the flake8 errors are fixed), set ``STRICT`` to ``True`` in ``.git/hooks/pre-commit``.

## pytest

pytest: helps you write better programs  
a mature full-featured Python testing tool  
http://pytest.org/latest/  

## Sites hosted on Read The Docs

Always test your branch builds on Read The Docs. Do not assume a successful build on Travis means it will build on Read The Docs.

For this you will need to be an admin in the Read The Docs project.

Enable your branch in https://readthedocs.org/dashboard/PROJECTNAME/versions/

Note that Read The Docs does not always pick up new branches - you may have to go to 
https://readthedocs.org/projects/PROJECTNAME/builds/ and trigger a new build (on any branch) before new branches will 
be picked up and appear in the admin page.

### Tips

General help

```bash
  py.test --help
```

To stop at the first failure

```bash
  py.test -x 
```

You can run all the tests in a certain directory

```bash
  py.test <directory>
```

or all the tests in a certain file

```bash
  py.test <path to file>
```

To run selected tests:

```bash
  py.test -k <string>
```
e.g. `py.test -k humanize` will run all the tests with the word humanize in them
e.g. `py.test -k 'humanize or index'` will run all the tests with the word 'humanize' and the tests with the word 'index' in them

