Stdio Mask
======

THIS MODULE HAS BEEN RENAMED TO PWINPUT. See https://pypi.org/project/pwinput/

No more updates will be made to this module. Please switch to pwinput instead.

You'll need to change `import stdiomask` to `import pwinput` and `stdiomask.getpass()` to `pwinput.pwinput()`.


Original README
---------------

A cross-platform Python module for entering passwords to a stdio terminal and displaying a **** mask, which getpass cannot do.

Installation
------------

To install with pip, run:

    pip install stdiomask

Quickstart Guide
----------------

The `getpass.getpass()` function in the Python Standard Library won't display "mask" characters as you type; it only displays nothing as you type. If you want mask characters to appear, you can use the `stdiomask.getpass()` function instead.

Typical usage:

    >>> import stdiomask
    >>> stdiomask.getpass()  # Show * for each typed character.
    Password: *********
    'swordfish'
    >>> stdiomask.getpass(prompt='PW: ')  # Show a custom prompt.
    PW: *********
    'swordfish'
    >>> stdiomask.getpass(mask='X')  # Show a different character when user types.
    Password: XXXXXXXXX
    'swordfish'
    >>> stdiomask.getpass(mask='') # Don't show anything when user types (falls back and calls getpass.getpass()).
    Password:
    'swordfish'

Contribute
----------

If you'd like to contribute to Stdio Mask, check out https://github.com/asweigart/stdiomask

Support
-------

If you find this project helpful and would like to support its development, [consider donating to its creator on Patreon](https://www.patreon.com/AlSweigart).
