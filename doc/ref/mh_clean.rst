mh\_clean:
~~~~~~~~~~

Cleans the temporary files created by the other mh\_\* utilities. Add it
to the clean: target in debian/rules

Usage:

::

    mh_clean

In debian/rules, use:

::

    clean::
        mh_clean

