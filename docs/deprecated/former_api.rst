Deprecated, Obsolete or Removed Setuptools APIs
===============================================

The following ``setuptools`` APIs are no longer considered available for public use.


Configuration and Metadata Parsing
----------------------------------
.. deprecated:: 61.0.0

.. currentmodule:: setuptools.config

.. function:: read_configuration(path, find_others=False, ignore_option_errors=False)

Some automation tools may wish to access data from a configuration file.
``Setuptools`` exposes a ``read_configuration()`` function for
parsing ``metadata`` and ``options`` sections into a dictionary:

.. code-block:: python

    from setuptools.config import read_configuration
    conf_dict = read_configuration("/home/user/dev/package/setup.cfg")


By default, ``read_configuration()`` will read only the file provided
in the first argument. To include values from other configuration files
which could be in various places, set the ``find_others`` keyword argument
to ``True``.
If you have only a configuration file but not the whole package, you can still
try to get data out of it with the help of the ``ignore_option_errors`` keyword
argument. When it is set to ``True``, all options with errors possibly produced
by directives, such as ``attr:`` and others, will be silently ignored.
As a consequence, the resulting dictionary will include no such options.

.. admonition:: Alternatives for ``setuptools.config``

   Consider parsing the ``setup.cfg`` directly using the :class:`~configparser.ConfigParser`
   class available on Python's standard library.
   To access metadata from ``setuptools`` based projects you can also try
   the functionalities exposed by the :pypi:`build` package (e.g.
   :func:`build.util.project_wheel_metadata`, or
   :meth:`build.ProjectBuilder.prepare` combined with
   :meth:`importlib_metadata.Distribution.at`).
