fluentcms-button
===================

.. image:: https://img.shields.io/travis/edoburu/fluentcms-button/master.svg?branch=master
    :target: http://travis-ci.org/edoburu/fluentcms-button
.. image:: https://img.shields.io/pypi/v/fluentcms-button.svg
    :target: https://pypi.python.org/pypi/fluentcms-button/
.. image:: https://img.shields.io/pypi/dm/fluentcms-button.svg
    :target: https://pypi.python.org/pypi/fluentcms-button/
.. image:: https://img.shields.io/badge/wheel-yes-green.svg
    :target: https://pypi.python.org/pypi/fluentcms-button/
.. image:: https://img.shields.io/pypi/l/fluentcms-button.svg
    :target: https://pypi.python.org/pypi/fluentcms-button/
.. image:: https://img.shields.io/codecov/c/github/edoburu/fluentcms-button/master.svg
    :target: https://codecov.io/github/edoburu/fluentcms-button?branch=master

Displaying a Bootstrap 3 Button_ in text.

This button can be used for navigation.


Installation
============

First install the module, preferably in a virtual environment. It can be installed from PyPI:

.. code-block:: bash

    pip install fluentcms-button

First make sure the project is configured for django-fluent-contents_.

Then add the following settings:

.. code-block:: python

    INSTALLED_APPS += (
        'fluentcms_button',
    )

    FLUENT_CONTENTS_PLACEHOLDER_CONFIG = {
        'slot name': {
            'plugins': ('ButtonPlugin', ...),
        },
    }

The database tables can be created afterwards:

.. code-block:: bash

    ./manage.py migrate


Frontend styling
================

The button is rendered with the HTML that Bootstrap prescribes:

.. code-block:: html+django

    <a class="btn btn-default" href="#" role="button">Link</a>

The standard Bootstrap 3 CSS will provide a reasonable styling for this,
which can either be overwritten, or replaced in your own CSS files.
The defaults provided by Bootstap 3 is: https://github.com/twbs/bootstrap-sass/blob/master/assets/stylesheets/bootstrap/_buttons.scss

When you use Sass, you can also override the Sass variables.

Contributing
------------

If you like this module, forked it, or would like to improve it, please let us know!
Pull requests are welcome too. :-)

.. _django-fluent-contents: https://github.com/edoburu/django-fluent-contents
.. _Button: http://getbootstrap.com/css/#buttons
