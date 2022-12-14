Visual Studio 10 2010
---------------------

Deprecated.  Generates Visual Studio 10 (VS 2010) project files.

.. note::
  This generator is deprecated and will be removed in a future version
  of CMake.  It will still be possible to build with VS 10 2010 tools
  using the :generator:`Visual Studio 11 2012` (or above) generator
  with :variable:`CMAKE_GENERATOR_TOOLSET` set to ``v100``, or by
  using the :generator:`NMake Makefiles` generator.

For compatibility with CMake versions prior to 3.0, one may specify this
generator using the name ``Visual Studio 10`` without the year component.

Project Types
^^^^^^^^^^^^^

Only Visual C++ and C# projects may be generated (and Fortran with
Intel compiler integration).  Other types of projects (Database,
Website, etc.) are not supported.

Platform Selection
^^^^^^^^^^^^^^^^^^

The default target platform name (architecture) is ``Win32``.

.. versionadded:: 3.1
  The :variable:`CMAKE_GENERATOR_PLATFORM` variable may be set, perhaps
  via the :option:`cmake -A` option, to specify a target platform
  name (architecture).  For example:

  * ``cmake -G "Visual Studio 10 2010" -A Win32``
  * ``cmake -G "Visual Studio 10 2010" -A x64``
  * ``cmake -G "Visual Studio 10 2010" -A Itanium``

For compatibility with CMake versions prior to 3.1, one may specify
a target platform name optionally at the end of the generator name.
This is supported only for:

``Visual Studio 10 2010 Win64``
  Specify target platform ``x64``.

``Visual Studio 10 2010 IA64``
  Specify target platform ``Itanium``.

Toolset Selection
^^^^^^^^^^^^^^^^^

The ``v100`` toolset that comes with Visual Studio 10 2010 is selected by
default.  The :variable:`CMAKE_GENERATOR_TOOLSET` option may be set, perhaps
via the :option:`cmake -T` option, to specify another toolset.
