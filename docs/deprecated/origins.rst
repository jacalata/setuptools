========================
The origin of Setuptools
========================

``Setuptools`` started out as a collection of enhancements to the
distutils_ module in Python's standard library,
allowing developers to more easily build and distribute Python
packages, especially the ones with dependencies on other packages.

Packages built and distributed using ``setuptools`` initially looked to the user like
ordinary Python packages based on the ``distutils``.

The main enhancements implemented in ``setuptools`` were:

* Ability to create `Python Eggs <http://peak.telecommunity.com/DevCenter/PythonEggs>`_ -
  a single-file importable distribution format

* Enhanced support for accessing data files hosted in zipped packages.

* Automatically inclusion of all packages in the source tree, without listing them
  individually in setup.py

* Automatically inclusion of all relevant files in source distributions,
  without needing to create a |MANIFEST.in|_ file, and without having to force
  regeneration of the ``MANIFEST`` file when your source tree changes
  [#manifest]_.

* Automatically generation of wrapper scripts or Windows (console and GUI) .exe
  files for any number of "main" functions in a project.  (Note: this was not
  a py2exe replacement; the .exe files rely on the local Python installation.)

* Transparent Cython support, so that ``setup.py`` can list ``.pyx`` files and
  still work even when the end-user doesn't have Cython installed (as long as
  the Cython-generated C files are included in the source distribution)

* Command aliases - project-specific, per-user, or site-wide shortcut
  names for commonly used commands and options

* Support for "development mode", such that it's available on
  ``sys.path``, yet can still be edited directly from its source checkout.

* Ability to add new ``distutils`` commands or ``setup()`` arguments, and distribute/
  reuse extensions for multiple projects, without copying code.

* Ability to create extensible applications and frameworks that automatically discover
  extensions, using simple "entry points" declared in a project's setup script.

* Full support for PEP 420 via ``find_namespace_packages()``
  (backwards compatible to the existing ``find_packages()`` for Python >= 3.3).

* Ability to build projects using configuration and metadata
  provided via ``setup.cfg`` without the need of an imperative ``setup.py``
  script (introduced in version 40.9.0).

----


.. [#manifest] The default behaviour for ``setuptools`` will work well for pure
   Python packages, or packages with simple C extensions (that don't require
   any special C header). See :ref:`Controlling files in the distribution` and
   :doc:`/userguide/datafiles` for more information about complex scenarios, if
   you want to include other types of files.

.. |MANIFEST.in| replace:: ``MANIFEST.in``
.. _MANIFEST.in: https://packaging.python.org/en/latest/guides/using-manifest-in/

.. _distutils: https://docs.python.org/3.9/library/distutils.html
