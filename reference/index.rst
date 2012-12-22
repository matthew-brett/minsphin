.. reference:

##############
NIPY reference
##############

:Release: |version|
:Date: |today|

.. module:: nipy

This part of the NIPY documentation describes how the code is arranged in
packages, and what these packages do.

These are the main packages:

.. toctree::
    :maxdepth: 2

    core
    algorithms
    io
    modalities
    labs
    interfaces

There are also packages that provide supporting routines:

.. toctree::
    :maxdepth: 2

    utils
    externals
    fixes
    testing

For nearly every sub-directory you will see a ``test`` directory, containing
tests for the code in the sub-directory.
