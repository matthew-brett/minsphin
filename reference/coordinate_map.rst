.. currentmodule:: nipy.core.reference.coordinate_map

##############
Coordinate map
##############

A coordinate map is:

* A *domain* or *input* :ref:`coordinate_systems`
* A *range* or *output* coordinate system
* A *mapping* function that maps coordinates in the *domain* to coordinates in
  the *range* coordinate systems.

For example, let say we have a 3D array of voxel values from the scanner.  A
particular voxel in the array has an *array* or *voxel* coordinate - say ``[2, 5
11]``.  The voxel coordinate, as for any coordinate, is defined within a
coordinate system.  In this cae, the coordinate system is the array axes. We
might give the first, second and third axes in the array the names $i, j, k$


.. respectively. In terms of the :class:`nipy.core.api.CoordinateSystem`, this

would be:

>>> from nipy.core.api import CoordinateSystem
>>> voxel_coordsys = CoordinateSystem(
