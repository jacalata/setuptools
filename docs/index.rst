.. image:: images/banner-640x320.svg
   :align: center

Setuptools is a fully-featured, actively-maintained, and stable library designed for
packaging Python projects. It helps developers to easily share Python libraries,
tools and applications in standard formats that can be
uploaded to `PyPI <http://pypi.org>`_ and installed with :pypi:`pip`.

For a long time it was the semi-official replacement for ``distutils`` and de facto
specification for Python package management, bundling and installation.
In the build system model standardized in recent years by the Python community,
``setuptools`` is a modern *build backend* that supports interoperable
configuration via ``pyproject.toml``.

Setuptools has an active third party plugin ecosystem which includes
:pypi:`setuptools-scm`, :pypi:`setuptools-svn`, :pypi:`setuptools-rust`
and :pypi:`setuptools-golang`. It also integrates well with Python-to-C
compilers such as :pypi:`Cython` and :RTD:`mypyc`.


Documentation
=============

Check out our :doc:`User Guide </userguide/index>` for information on how to use ``setuptools``,
and if you are interested in contributing to the project, please have a look on
the :doc:`Development Guide </development/index>`.

.. toctree::
   :maxdepth: 1
   :hidden:

   User guide <userguide/index>
   build_meta
   pkg_resources
   references/keywords

.. toctree::
   :caption: Project
   :maxdepth: 1
   :hidden:

   roadmap
   Development guide <development/index>
   Backward compatibility & deprecated practice <deprecated/index>
   Changelog <history>
   artwork


Forum and Bug Tracker
=====================

Please use `GitHub Discussions`_ for questions and discussion about
setuptools, and the `setuptools bug tracker`_ ONLY for issues you have
confirmed via the forum are actual bugs, and which you have reduced to a minimal
set of steps to reproduce.

.. _GitHub Discussions: https://github.com/pypa/setuptools/discussions
.. _setuptools bug tracker: https://github.com/pypa/setuptools/


.. tidelift-referral-banner::
