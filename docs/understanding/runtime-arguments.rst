.. _understanding-runtime-arguments:

Runtime Arguments
=================

A Fortuno test executable is a command-line application that can be run with several arguments to control its behavior.

Usage
-----

.. code-block:: console

   $ ./testapp [-h] [-l] [--disable-strict-matching] [--allow-empty-run] [tests]

Arguments
---------

* ``tests``: (Optional) A list of tests and test suites to include or exclude.
  
  * To include a test or suite, provide its name (e.g., ``test_addition``, ``math_suite``).
  * To exclude a test or suite, prefix its name with a tilde (``~``).
  * You can combine inclusions and exclusions. For example, ``math_suite ~math_suite/test_division_by_zero`` would run all tests in the ``math_suite`` except for ``test_division_by_zero``.

Options
-------

* ``-h``, ``--help``: Show the help message and exit.

* ``-l``, ``--list``: Show the list of tests that would be run based on the current selection and exit, without actually running them.

* ``--disable-strict-matching``: By default, Fortuno will raise an error if a test selection argument does not match any existing test. This option disables that check, allowing selection arguments that have no effect.

* ``--allow-empty-run``: If the test selection results in no tests being run (e.g., due to an over-constrained selection), Fortuno will fail by default. This option allows an empty test run to be considered a success.
