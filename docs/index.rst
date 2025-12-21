################################################
Fortuno: A Modern Fortran Unit Testing Framework
################################################

Fortuno is a flexible and extensible unit testing framework tailored for modern Fortran programming. It offers a simple, user-friendly interface requiring only a minimal amount of boilerplate code.

.. grid:: 1 2 2 2
    :gutter: 2

    .. grid-item-card:: Getting Started
        :link: tutorials/quickstart-cmake.html

        New to Fortuno? Start with our quickstart guide to learn the basics and write your first test.

    .. grid-item-card:: How-to Guides
        :link: howtos.html

        Explore our how-to guides for specific topics and advanced features like fixtures and parameterized tests.

    .. grid-item-card:: Understanding Fortuno
        :link: understanding.html

        Dive deeper into the philosophy and design of Fortuno to get the most out of the framework.

    .. grid-item-card:: Join the Development
        :link: contributing.html

        Fortuno is an open-source project. Learn how you can contribute.

.. toctree::
   :hidden:
   :maxdepth: 2

   tutorials
   howtos
   understanding
   about
   contributing

Key Features
============

*   **Simple and concise:** Write tests with minimal boilerplate code.
*   **Flexible:** Supports various testing styles, including fixtured and parameterized tests.
*   **Parallel testing:** Built-in support for MPI and Coarray testing.
*   **Extensible:** A modular design that is easy to extend.
*   **Great integration:** Works seamlessly with CMake, Meson, and the Fortran Package Manager (fpm).
