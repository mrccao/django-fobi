===============================================================================
fobi.contrib.themes.foundation5.widgets.form_elements.datetime_foundation5_widget
===============================================================================
A fancy datetime picker widget to the ``datetime`` plugin (for Foundation 5
theme).

Installation
===============================================
1. Add ``fobi.contrib.themes.foundation5.widgets.form_elements.datetime_foundation5_widget``
   to the ``INSTALLED_APPS`` in your ``settings.py``.

.. code-block:: python

    INSTALLED_APPS = (
        # ...
        'fobi.contrib.themes.foundation5',
        'fobi.contrib.themes.foundation5.widgets.form_elements.datetime_foundation5_widget',
        'fobi.contrib.plugins.form_elements.fields.datetime',
        # ...
    )

2. Specify ``foundation5`` as a default theme in your ``settings.py``:

.. code-block:: python

    FOBI_DEFAULT_THEME = 'foundation5'
