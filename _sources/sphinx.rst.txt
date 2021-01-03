======
Sphinx
======

Create a docs directory in your repository and open a terminal in that
directory and run sphinx-quickstart. The one thing I changed is shown below.
::

    sphinx-quickstart

    > Separate source and build directories (y/n) [n]: y
    > todo: write "todo" entries that can be shown or hidden on build (y/n) [n]: y
    > githubpages: create .nojekyll file to publish the document on GitHub pages (y/n) [n]: y
    > Create Windows command file? (y/n) [y]: n


Open the config.py file and find `html_static_path = ['_static']` and change it
to ``html_static_path = []``.

Next find `html_theme = 'alabaster'` and change it to
``html_theme = 'sphinx_rtd_theme'``

Next find `extensions` and add ``'sphinx.ext.githubpages',``. There may be more
extensions but it looks like this:
::

    extensions = [
        'sphinx.ext.githubpages',
        'sphinx.ext.todo',
    ]




