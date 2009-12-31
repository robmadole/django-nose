================
Running the demo
================

You need `virtualenv`_ and `virtualenvwrapper`_ if you want to follow these
directions verbatim.  Adjust accordingly, it was meant to get you up and
running quickly.

Make the virtual environment
----------------------------

We use the :opt:`--no-site-packages` to give us a squeaky clean environment. ::

    $ mkvirtualenv --no-site-packages django-nose-demo
    New python executable in django-nose-demo/bin/python
    Installing setuptools............done.
    (django-nose-demo) $

The nice thing about making a new virtual environment with the wrapper is that
it immediately activates it for you.

Run the buildout script
-----------------------

First we bootstrap buildout itself. ::

    (django-nose-demo) $ cd demo
    (django-nose-demo) $ python bootstrap.py
    Creating directory '/Users/robmadole/Development/workbench/django-nose/demo/bin'.
    Creating directory '/Users/robmadole/Development/workbench/django-nose/demo/parts'.
    Creating directory '/Users/robmadole/Development/workbench/django-nose/demo/eggs'.
    Creating directory '/Users/robmadole/Development/workbench/django-nose/demo/develop-eggs'.
    Generated script '/Users/robmadole/Development/workbench/django-nose/demo/bin/buildout'.

And run `bin/buildout` ::

    (django-nose-demo) $ ./bin/buildout
    Getting distribution for 'setuptools'.
    Got setuptools 0.6c11.
    Upgraded:
      setuptools version 0.6c11;
    restarting.
    Generated script '/Users/robmadole/Development/workbench/django-nose/demo/bin/buildout'.
    Develop: '/Users/robmadole/Development/workbench/django-nose/demo/../'
    Getting distribution for 'djangorecipe'.
    Got djangorecipe 0.20.
    Getting distribution for 'zc.recipe.egg'.
    Got zc.recipe.egg 1.2.2.
    Installing django.
    django: Downloading Django from: http://www.djangoproject.com/download/1.1.1/tarball/
    Getting distribution for 'nose'.
    no previously-included directories found matching 'doc/.build'
    Got nose 0.11.1.
    Generated script '/Users/robmadole/Development/workbench/django-nose/demo/bin/django'.
    Generated script '/Users/robmadole/Development/workbench/django-nose/demo/bin/django.wsgi'.


.. _virtualenv: http://pypi.python.org/pypi/virtualenv
.. _virtualenvwrapper: http://www.doughellmann.com/projects/virtualenvwrapper/
