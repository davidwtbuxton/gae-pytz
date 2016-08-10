GAE pytz
========

A fork of pytz which works on [Google App Engine][1].

Based on [http://appengine-cookbook.appspot.com/recipe/caching-pytz-helper/][2] but modified so that it can be imported normally with `import pytz`.

Install from PyPI:

    $ pip install gae-pytz

The project home is on GitHub: https://github.com/potatolondon/gae-pytz/


How to update the zone info database
------------------------------------

Clone the gae-pytz repository and download the source distribution of pytz:

    $ git clone https://github.com/potatolondon/gae-pytz.git
    $ cd gae-pytz
    $ pip install --download . --no-binary :all: pytz

That should download the source tarball for pytz and save it in the current directory. Extract the zone info database and create a new zip (you need to change the name for the pytz source tarball):

    $ python makezoneinfo.py < pytz-2016.6.1.tar.gz > pytz/zoneinfo.zip


[1]: https://developers.google.com/appengine/
[2]: http://appengine-cookbook.appspot.com/recipe/caching-pytz-helper/
