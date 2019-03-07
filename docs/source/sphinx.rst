======
Sphinx
======

Create a docs directory in your repository and open a terminal in that
directory and run sphinx-quickstart. The one thing I changed is shown below.
::

    sphinx-quickstart

    > Separate source and build directories (y/n) [n]: y

Open the config.py file and find `html_static_path = ['_static']` and change it
to ``html_static_path = []``.

Next find `html_theme = 'alabaster'` and change it to
``html_theme = 'sphinx_rtd_theme'``





