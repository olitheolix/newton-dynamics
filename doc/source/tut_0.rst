Compiling And Linking A Trivial Program That Uses Newton
========================================================

Purpose: show how to compile a Newton simulation.

The simulation creates a Newton world, steps it sixty times, and then destroys
the world again. Literally nothing will happen since the world is empty. Here
is the :download:`code <./tut0.cpp>`:

.. literalinclude:: tut0.cpp
    :linenos:
    :language: c

Linux
-----
To compile, link, and run the program type:

.. code-block:: bash
    :linenos:

    $ g++ tut0.cpp -o tut0 -I ../../coreLibrary_300/source/newton/ -L ../../build/lib/ -lNewton -lpthread -Wl,"-rpath=../../build/lib/"
    $ ./tut0

This may look intimidating but is straightforward. The ``-I
../../coreLibrary_300/source/newton/`` flag tells the compiler where to find
``Newton.h``. Similarly,  ``-L ../../build/lib/`` tells the linker where to look
for additional libraries. The next flag (``-lNewton``) tells the linker to link
our prgram against the ``libNewton.so`` libray we built in :ref:`Installation`.
Finally, Newton uses threads internally and thus needs a ``-lpthread``.


Other
-----
Please submit pull request for instructions.
