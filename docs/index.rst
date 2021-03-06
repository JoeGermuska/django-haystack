Welcome to Haystack!
====================

Haystack provides modular search for Django. It features a unified, familiar
API that allows you to plug in different search backends (such as Solr_,
Whoosh_, etc.) without having to modify your code.

.. _Solr: http://lucene.apache.org/solr/
.. _Whoosh: http://whoosh.ca/


Getting Started
---------------

If you're new to Haystack, you may want to start with these documents to get
you up and running:

.. toctree::
   :maxdepth: 2
   
   tutorial
   
.. toctree::
   :maxdepth: 1
   
   faq
   installing_search_engines


Reference
---------

If you're an experienced user and are looking for a reference, you may be
looking for API documentation and advanced usage as detailed in:

.. toctree::
   :maxdepth: 2
   
   searchqueryset_api
   searchindex_api
   searchsite_api
   searchquery_api
   searchbackend_api
   
   architecture_overview
   backend_support
   settings


Developing
----------

Finally, if you're looking to help out with the development of Haystack,
the following links should help guide you on running tests and creating
additional backends:

.. toctree::
   :maxdepth: 1
   
   running_tests
   creating_new_backends
