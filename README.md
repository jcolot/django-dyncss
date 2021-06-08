[django-dyncss](https://github.com/jcolot/django-dyncss) is an extension
to [Django](https://github.com/django/django) which adds the possibility
to store a css file in the Django DB.

Installation
============

Install the latest version from pypi.python.org:

    pip install django-dyncss

Install the development version by cloning the source from github.com:

    pip install git+https://github.com/jcolot/django-dyncss.git

Configuration
=============

Add the package to your `INSTALLED_APPS`:

    INSTALLED_APPS += (
        'django_dyncss',
    )

Add the url path in your main urls.py.

    urlpatterns = [
        ...
        url(r'^dyncss/', include('dyncss.urls')),
    ]

Usage
=====

Create a CSS File from the Django Admin

Add a link to that file in your Django template

    <link rel="stylesheet" href="dyncss/example.css">

You can also use the template tag

    {% load dyncss %}

    {% dyncss 'example.css' inline=True %}

The parameter `inline` when `True` allows to render the file inline within `<style>` tags

License
=======

-   Released under MIT License
-   Copyright (c) 2021 Julien Colot <julien.colot@gmail.com>

Resources
=========

-   [Code](https://github.com/jcolot/django-dyncss)

