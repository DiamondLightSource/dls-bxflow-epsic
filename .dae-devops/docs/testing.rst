.. # ********** Please don't edit this file!
.. # ********** It has been generated automatically by dae_devops version 0.5.1.
.. # ********** For repository_name dls-bxflow-epsic

Testing
=======================================================================

The package uses pytest for unit testing.

If you want to run the tests, first get a copy of the code per the instructions in the Developing section.

Then you can run all tests by::

    $ pytest

Or this, which is the command used by the CI runner.

    $ make -f .dae-devops/Makefile validate_pytest

To run a single test you can do::

    $ pytest tests/the_test_you_want.py

If you want to see more output of the test while it's running you can do:

    $ pytest -sv -ra --tb=line tests/the_test_you_want.py

Each test will write files into its own directory::

    /tmp/dls-bxflow-epsic/tests/....

The tests clear their directory when they start, but not when they finish.
This allows peeking in there to see what's been written by the test.

    


.. # dae_devops_fingerprint c4e9ece203206da35583dbf9f410372f
