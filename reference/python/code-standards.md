Coding standards
----------------

Our older repositories were just checked with flake8.

We are now moving to checking all repositories with flake8, black and isort.

Note black will only work on Python 3.6+ so if the repository supports older version of Python, tricks will need to be used to make sure it only installs on 3.6+.

There are some config files we need.

`isort.cfg` should be:

    # From https://black.readthedocs.io/en/stable/the_black_code_style.html?highlight=isort#how-black-wraps-lines
    [settings]
    multi_line_output=3
    include_trailing_comma=True
    force_grid_wrap=0
    use_parentheses=True
    line_length=88

`setup.cfg` should be:

    [flake8]
    # Ignore style checking, because black does this for us
    ignore = E,W

.Travis should have lines to run isort, black and flake8.

      - black --check *.py */
      - isort --check-only --recursive *.py */
      - flake8




