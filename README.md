# ansiterm Package

ansiterm - a simple library to generate ANSI escape sequences

# DESCRIPTION

This manual page documents **ansiterm** module, a Python module providing
functions for generating ANSI escape sequences.

A majority of terminal emulators support ANSI escape sequences.  **ansiterm**
module provides a very limited set of functions for changing the color and the
style of the characeters displayed on the screen. 

Please refer to https://en.wikipedia.org/wiki/ANSI_escape_code for the
introduction of ANSI escape sequences.

# EXAMPLE

```python
from ansiterm import color

for bold in (False, True):
    for reverse in (False, True):
        for name in [
                'reset', 'bold', 'underline', 'reverse', 'gray', 'red',
                'green', 'yellow', 'blue', 'magenta', 'cyan', 'white'
        ]:
            astr = color('text in {} with bold={}, reverse={}'.format(
                name, bold, reverse),
                         name,
                         bold=bold,
                         reverse=reverse)
            print(astr)
```

# FUNCTIONS

**ansiterm** module provides the following functions.

- color(astr, name='bold', bold=False, reverse=False)

  Embed ANSI escape sequences around string ASTR to change the text style to
  NAME.  Make the text boldface and reversed video if BOLD or REVERSE is True,
  respectively.

The following functions are provided as short-cuts.

- reset(astr, bold=False, reverse=False)

- bold(astr, bold=True, reverse=False)

- gray(astr, bold=False, reverse=False)

- red(astr, bold=False, reverse=False)

- green(astr, bold=False, reverse=False)

- yellow(astr, bold=False, reverse=False)

- blue(astr, bold=False, reverse=False)

- magenta(astr, bold=False, reverse=False)

- cyan(astr, bold=False, reverse=False)

- white(astr, bold=False, reverse=False)

# INSTALLATION

```python
pip3 install ansiterm
```

# AVAILABILITY

The latest version of **ansiterm** module is available at PyPI
(https://pypi.org/project/ansiterm/) .

# SEE ALSO

perl(1), perlfunc(1), getopt(3), Getopt::Std(3perl)

# AUTHOR

Hiroyuki Ohsaki <ohsaki[atmark]lsnl.jp>
