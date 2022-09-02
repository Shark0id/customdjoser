======
djoser
======

REST implementation of `Django <https://www.djangoproject.com/>`_ authentication
system. **djoser** library provides a set of `Django Rest Framework <https://www.django-rest-framework.org/>`_
views to handle basic actions such as registration, login, logout, password
reset and account activation. It works with

Developed by `SUNSCRAPERS <http://sunscrapers.com/>`_ with passion & patience.

Requirements
============

To be able to run **djoser** you have to meet following requirements:

- Python (3.7, 3.8, 3.9, 3.10)
- Django (2.2, 3.1, 3.2, 4.0)
- Django REST Framework (3.11.1, 3.12.1, 3.13)

If you need to support other versions, please use djoser<2.2.

Installation
============

Simply install using ``pip``:

.. code-block:: bash

    $ pip install djoser


Contributing and development
============================

To start developing on **djoser**, clone the repository:

.. code-block:: bash

    $ git clone git@github.com:sunscrapers/djoser.git

We use `poetry <https://python-poetry.org/>`_ as dependency management and packaging tool.

.. code-block:: bash

    $ cd djoser
    $ poetry install -E test

This will create a virtualenv with all development dependencies.

To run the test just type:

.. code-block:: bash

    $ poetry run py.test testproject

We also prepared a convenient ``Makefile`` to automate commands above:

.. code-block:: bash

    $ make init
    $ make test

To activate the virtual environment run

.. code-block:: bash

    $ poetry shell

Without poetry
--------------

New versions of ``pip`` can use ``pyproject.toml`` to build the package and install its dependencies.

.. code-block:: bash

    $ pip install .[test]

.. code-block:: bash

    $ cd testproject
    $ ./manage.py test

Tox
---

If you need to run tests against all supported Python and Django versions then invoke:

.. code-block:: bash

    $ poetry run tox -p all

Example project
---------------

You can also play with test project by running following commands:

.. code-block:: bash

    $ make migrate
    $ make runserver

Commiting your code
-------------------

Before sending patches please make sure you have `pre-commit <https://pre-commit.com/>`_ activated in your local git repository:

.. code-block:: bash

    $ pre-commit install

This will ensure that your code is cleaned before you commit it.
Some steps (like black) automatically fix issues but the show their status as FAILED.
Just inspect if everything is OK, git-add the files and retry the commit.
Other tools (like flake8) require you to manually fix the issues.
