=================
Haystack Settings
=================

As a way to extend/change the default behavior within Haystack, there are
several settings you can alter within your ``settings.py``. This is a
comprehensive list of the settings Haystack recognizes.


``HAYSTACK_DEFAULT_OPERATOR``
=============================

**Optional**

This setting controls what the default behavior for chaining ``SearchQuerySet``
filters together is.

Valid options are::

    HAYSTACK_DEFAULT_OPERATOR = 'AND'
    HAYSTACK_DEFAULT_OPERATOR = 'OR'

Defaults to ``AND``.


``HAYSTACK_SEARCH_ENGINE``
==========================

**Required**

This setting controls which backend should be used. You should provide the
short name (e.g. ``solr``), not the full filename of the backend (e.g.
``solr_backend.py``).

Valid options are::

    HAYSTACK_SEARCH_ENGINE = 'solr'
    HAYSTACK_SEARCH_ENGINE = 'whoosh'
    HAYSTACK_SEARCH_ENGINE = 'dummy'

No default is provided.


``HAYSTACK_SEARCH_RESULTS_PER_PAGE``
====================================

**Optional**

This setting controls how many results are shown per page when using the
included ``SearchView`` and its subclasses.

An example::

    HAYSTACK_SEARCH_RESULTS_PER_PAGE = 50

Defaults to ``20``.


``HAYSTACK_SOLR_URL``
=====================

**Required when using the ``solr`` backend**

This setting controls what URL the ``solr`` backend should be connecting to.
This depends on how the user sets up their Solr daemon.

Examples::

    HAYSTACK_SOLR_URL = 'http://localhost:9000/solr/test'
    HAYSTACK_SOLR_URL = 'http://solr.mydomain.com/solr/mysite'

No default is provided.


``HAYSTACK_WHOOSH_PATH``
========================

**Required when using the ``whoosh`` backend**

This setting controls where on the filesystem the Whoosh indexes will be stored.
The user must have the appropriate permissions for reading and writing to this
directory.

Any trailing slashes should be left off.

Finally, you should ensure that this directory is not located within the
document root of your site and that you take appropriate security precautions.

An example::

    HAYSTACK_WHOOSH_PATH = '/home/mysite/whoosh_index'

No default is provided.
