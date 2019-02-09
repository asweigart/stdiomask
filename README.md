Stdio Mask
======

A cross-platform Python module for entering passwords to a stdio terminal and displaying a **** mask, which getpass cannot do.

Installation
------------

To install with pip, run:

    pip install stdiomask

Quickstart Guide
----------------

The `getpass.getpass()` function in the Python Standard Library won't display "mask" characters as you type; it only displays nothing as you type. If you want mask characters to appear, you can use the `stdio.getpass()` function instead.

Typical usage:

    >>> import stdiomask
    >>> stdiomask.getpass()
    Password: *********
    'swordfish'
    >>> stdiomask.getpass(prompt='PW: ')
    PW: *********
    'swordfish'
    >>> stdiomask.getpass(mask='X')
    Password: XXXXXXXXX
    'swordfish'
    >>> stdiomask.getpass(mask='') # Falls back and calls getpass.getpass()
    Password:
    'swordfish'

Contribute
----------

If you'd like to contribute to Stdio Mask, check out https://github.com/asweigart/stdiomask
