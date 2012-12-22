.. currentmodule:: nipy.core.reference.coordinate_system

#################
Coordinate system
#################

A coordinate is a vector of numbers.  For example, a coordinate in 3D space
might be $(1, 3, 6)$.  These numbers refer to axes.  In the case of a classic
Cartesian 3D coordinate system, these axes are orthogonal, the first axis is
called $x$, the second $y$ and the third $y$.  Thus $(1.2, 3.3, 6.1)$ defines a
point at $1.1$ units along the $x$ axis, $3.3$ units along the $y$ axis and
$6.1$ units along the $y$ axis.

The :class:`CoordinateSystem` class contains the definition of a coordinate
system.  A coordinate system has ``ndim`` axes, identified by names
``coord_names``.  The values of coordinates are of numpy type ``coord_dtype`` -
usually float (``np.float64``).  The coordinate system has a ``name``. For
example, a set of Cartesian axes in the 3D real world might look this this:

.. image:: /images/coordinate_system.png

where the ``coord_names`` are ``(x, y, z)``, the ``coord_dtype`` is
``np.float64``, and the ``name`` is ``world``.

***********************
Coordinate system class
***********************

.. autoclass:: CoordinateSystem
    :members: __init__, __eq__, index, similar_to

    .. autoattribute:: CoordinateSystem.coord_names

    .. autoattribute:: CoordinateSystem.coord_dtype

    .. autoattribute:: CoordinateSystem.name

    .. autoattribute:: CoordinateSystem.ndim

    .. autoattribute:: CoordinateSystem.dtype

*****************************************
Functions operating on coordinate systems
*****************************************

.. autofunction:: is_coordsys

.. autofunction:: product

****************
Helper functions
****************

.. autofunction:: safe_dtype

**************
Helper classes
**************

.. autoclass:: CoordSysMaker
    :members: __init__, __call__
