.. include:: ../README.rst

Dockerflow?
-----------

You may be asking 'What is Dockerflow_?'

Here's what it's documentation says:

.. pull-quote::

    Dockerflow is a specification for automated building, testing and
    publishing of docker web application images that comply to a common
    set of behaviours. Compliant images are simpler to deploy, monitor
    and manage in production.

.. _Dockerflow: https://github.com/mozilla-services/Dockerflow

Features
--------

.. glossary::

   environment

      Accept its configuration through environment variables.
      See: :ref:`Django <django-config>`

   port

      Listen on environment variable ``$PORT`` for HTTP requests.
      See: :ref:`Django <django-serving>`

   version

      Must have a JSON version object at ``/app/version.json``.
      See: :ref:`Django <django-versions>`

   health

      * Respond to ``/__version__`` with the contents of /app/version.json
      * Respond to ``/__heartbeat__`` with a HTTP 200 or 5xx on error.
        This should check backing services like a database for connectivity
      * Respond to ``/__lbheartbeat__`` with an HTTP 200.
        This is for load balancer checks and should not check backing services.

      See: :ref:`Django <django-health>`

   logging

      Send text logs to ``stdout`` or ``stderr``. See: :ref:`Django <django-logging>`

   static content

      Serve its own static content. See: :ref:`Django <django-static>`.

Contents
--------

.. toctree::
   :maxdepth: 2

   authors
   changelog
   django
   api

Indices and tables
------------------

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`
