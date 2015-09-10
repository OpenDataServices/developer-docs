# Tests


## pytest

pytest: helps you write better programs  
a mature full-featured Python testing tool  
http://pytest.org/latest/  

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

