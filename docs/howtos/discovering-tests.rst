.. _how-to-discovering-tests:

Discovering tests
=================

Fortuno provides a CMake function ``fortuno_discover_tests`` to automatically discover and register tests with CTest. This is a more convenient alternative to manually adding tests with ``add_test``.

``fortuno_discover_tests`` queries the test executable for a list of its tests and registers them individually with CTest.

Usage
-----

.. code-block:: cmake

   fortuno_discover_tests(target
       [USE_PRE_TEST_DISCOVERY]
       [TEST_PREFIX prefix]
       [TEST_SUFFIX suffix]
       [TEST_PATTERN pattern]
       [WORKING_DIRECTORY dir]
   )

Arguments
---------

* ``target``: The name of the test executable target.

* ``USE_PRE_TEST_DISCOVERY``: (Optional) A flag to use pre-test discovery mode. By default, test discovery is performed after the build. When this flag is present, discovery is performed at test time.

* ``TEST_PREFIX prefix``: (Optional) A prefix to be added to the name of each discovered test.

* ``TEST_SUFFIX suffix``: (Optional) A suffix to be added to the name of each discovered test.

* ``TEST_PATTERN pattern``: (Optional) A pattern to filter tests. Only tests whose names match the pattern will be registered. By default, all tests are registered.

* ``WORKING_DIRECTORY dir``: (Optional) The working directory for the tests. Defaults to ``CMAKE_CURRENT_BINARY_DIR``.

Example
-------

.. code-block:: cmake

   add_executable(testapp test/testapp.f90)
   target_link_libraries(testapp PRIVATE mylib Fortuno::fortuno_serial)

   enable_testing()
   fortuno_discover_tests(testapp)

This will discover all tests in the ``testapp`` executable and add them to CTest.
