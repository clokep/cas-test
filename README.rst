A local test server for CAS
###########################

This project servers a minimal local CAS server backed by Django. Users are
controlled via the standard Django ``User`` model.

Running the test server
=======================

1. Download this git repository.
2. Create a new virtualenv: ``python3 -m venv <your virtualenv>``
3. Activate your virtualenv: ``source /path/to/your/virtualenv/bin/activate``
4. Install the requirements: ``python -m pip install -r requirements.txt``
5. Setup the SQLite database: ``python manage.py migrate``
6. Create a user: ``python manage.py createsuperuser``
   1. Use whatever you want as the username and password.
   2. Leave the other fields blank.
7. Use the built-in Django test server to serve the CAS endpoints on port 8000:
   ``python manage.py runserver``

You should now have a Django project configured to serve CAS authentication with
a single user created.

Rebuilding this project
=======================

Follow the steps above, but after installing the requirements (step 4):

1. Create a new Django project: ``django-admin startproject cas_test .``
2. Follow the `install directions`_ for ``django-mama-cas``

.. _install directions: https://django-mama-cas.readthedocs.io/en/latest/installation.html#configuring
