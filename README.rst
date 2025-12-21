*********************
Fortuno documentation
*********************

This repository contains the user documentation of the `Fortuno unit testing
framework <https://github.com/fortuno-repos/fortuno>`_. Its content is rendered
at the `Fortuno documentation <https://fortuno.readthedocs.io>`_ site.


License
=======

Fortuno documentation is licensed under the `Creative Common Attribution 4.0
International (CC BY 4.0) <https://creativecommons.org/licenses/by/4.0/>`_
license.


Building the documentation locally
==================================

To build the documentation locally, follow these steps:

1.  Create and activate a Python virtual environment:

    .. code-block:: console

       $ python3 -m venv venv
       $ source venv/bin/activate

2.  Install the required dependencies (sphinx):

    .. code-block:: console

       $ pip install -r docs/requirements.txt

3.  Build the documentation using the Makefile in the ``docs`` directory:

    .. code-block:: console

       $ cd docs
       $ make html

4.  View the generated documentation in your browser:

    Simply open the generated html located at ``docs/_build/html/index.html``.
