.. _index:
.. module:: podcast

.. image:: _static/img/logo.svg

Django Apple Podcast
*********************

|PyPI version|_ |Build status|_

.. |PyPI version| image::
   https://badge.fury.io/py/django-applepodcast.svg
.. _PyPI version: https://pypi.python.org/pypi/django-applepodcast

.. |Build status| image::
   https://travis-ci.org/richardcornish/django-applepodcast.svg?branch=master
.. _Build status: https://travis-ci.org/richardcornish/django-applepodcast

**Django Apple Podcast** is a `Django <https://www.djangoproject.com/>`_ podcast `application <https://docs.djangoproject.com/en/1.11/intro/reusable-apps/>`_ optimized for the `Apple Podcasts <https://podcastsconnect.apple.com/>`_. Formerly *Django iTunes Podcast*.

* `Package distribution <https://pypi.python.org/pypi/django-applepodcast>`_
* `Code repository <https://github.com/richardcornish/django-applepodcast>`_
* `Documentation <https://django-applepodcast.readthedocs.io/>`_
* `Tests <https://travis-ci.org/richardcornish/django-applepodcast>`_

An online demo also exists.

* `Online demo <https://djangoapplepodcastdemo.herokuapp.com/podcast/>`_
* `Online demo code repository <https://github.com/richardcornish/django-applepodcast-demo>`_

Install
=======

.. code-block:: bash

   $ pip install django-applepodcast

Add to ``settings.py``.

.. code-block:: python

   INSTALLED_APPS = [
       # ...
       'podcast',
   ]

Add to ``urls.py``.

.. code-block:: python

   from django.conf.urls import url, include

   urlpatterns = [
       # ...
       url(r'^podcast/', include('podcast.urls')),
   ]

Migrate the database.

.. code-block:: bash

   $ python manage.py migrate

Load the fixtures.

.. code-block:: bash

   $ python manage.py loaddata podcast_category.json

Usage
=====

Run the local server.

.. code-block:: bash

   $ python manage.py runserver

Visit either the show view or the admin.

- `http://127.0.0.1:8000/podcast/ <http://127.0.0.1:8000/podcast/>`_
- `http://127.0.0.1:8000/admin/podcast/ <http://127.0.0.1:8000/admin/podcast/>`_

Contents
========

.. toctree::
   :maxdepth: 2

   install
   usage
   settings
   feed
   admin
   documentation
   tests
   resources


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
