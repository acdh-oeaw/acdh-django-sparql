=============================
acdh-django-sparql
=============================

.. image:: https://badge.fury.io/py/acdh-django-sparql.svg
    :target: https://badge.fury.io/py/acdh-django-sparql

Django-App providing a query interface and proxy for any common Triplestore.


Quickstart
----------

Install acdh-django-sparql:

    pip install acdh-django-sparql

Add it to your `INSTALLED_APPS`:

.. code-block:: python

    INSTALLED_APPS = (
        ...
        'sparql',
        ...
    )

Add django_sparql's URL patterns:

.. code-block:: python

    urlpatterns = [
        ...
        url(r'^sparql/', include('sparql.urls', namespace='sparql')),
        ...
    ]


Provide the endpoint and optional some log-in credentials for your Triplestore in some settings file:

.. code-block:: python

    BG_URL = "https://path-to-your-triple-store/sparql"
    BG_USER = "username"
    BG_PW = "password"


browse to https://my-project/sparql/query/ to reach the query interface

Via the django-admin interface you can create sample queries.

Licensing
---------

All code unless otherwise noted is licensed under the terms of the MIT License (MIT). Please refer to the file LICENSE in the root directory of this repository.
