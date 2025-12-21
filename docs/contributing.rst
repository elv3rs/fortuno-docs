.. _contributing:

############
Contributing
############

Fortuno is a community-developed project, and we welcome contributions of all kinds! Whether you're a seasoned open-source contributor or a new user who has found a bug, your help is valuable.

Reporting Bugs
==============

If you encounter a bug, please report it on the `GitHub issue tracker <https://github.com/fortuno-repos/fortuno/issues>`_.

When reporting a bug, please include:

*   A clear and descriptive title.
*   A detailed description of the problem, including the expected behavior and the actual behavior.
*   A minimal, reproducible example that demonstrates the bug.
*   Information about your environment, such as the operating system, Fortran compiler, and Fortuno version.

Suggesting Features
===================

We are always open to new ideas! If you have a suggestion for a new feature or an improvement to an existing one, please open an issue on the `GitHub issue tracker <https://github.com/fortuno-repos/fortuno/issues>`_.

Development Setup
=================

To contribute code to Fortuno, you'll need to set up a development environment.

1.  **Fork the repository:** Start by `forking the Fortuno repository <https://github.com/fortuno-repos/fortuno/fork>`_ on GitHub.

2.  **Clone your fork:**

    .. code-block:: console

       $ git clone https://github.com/YOUR_USERNAME/fortuno.git
       $ cd fortuno

3.  **Create a new branch:**

    .. code-block:: console

       $ git switch -c my-new-feature

4.  **Make your changes.**

5.  **Run the tests:** Ensure that all tests still pass. You can run the tests using your preferred build system:

    **CMake**

    .. code-block:: console

       $ mkdir build && cd build
       $ cmake ..
       $ cmake --build .
       $ ctest

    **Fpm**

    .. code-block:: console

       $ fpm test

    **Meson**

    .. code-block:: console

       $ meson setup build
       $ meson test -C build

6.  **Submit a pull request:** Once you're happy with your changes, push your branch to your fork and `open a pull request <https://github.com/fortuno-repos/fortuno/compare>`_.


Building the documentation
==========================

To build the documentation locally, follow these steps:

1.  Create and activate a Python virtual environment:

    .. code-block:: console

       $ python3 -m venv venv
       $ source venv/bin/activate

2.  Install the required dependencies:

    .. code-block:: console

       $ pip install -r docs/requirements.txt

3.  Build the documentation using the Makefile in the ``docs`` directory:

    .. code-block:: console

       $ cd docs
       $ make html

4.  View the generated documentation in your browser:

    Simply open the generated html located at ``docs/_build/html/index.html``.


Coding Style
============

Please ensure your code is consistent with the existing coding style of the project. This includes:

*   Using 2 spaces for indentation.
*   Using lower-case for Fortran keywords.
*   Using ``implicit none`` in all modules and programs.
*   Using Doxygen-style comments (``!>``) for documentation.
