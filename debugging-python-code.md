# Debugging Python code

## pdbpp

pdb is the commandline python debugger. It's useful, but by installing
[pdbpp](https://pypi.python.org/pypi/pdbpp/) you get more features (colours,
tab completion etc.) for the same pdb interface.

## py.test --pdb

This command is useful because it runs py.test tests, dropping into the
debugger if one of them fails. If it's installed, pdbpp will be used.
