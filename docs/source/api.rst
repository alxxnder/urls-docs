===============
API (version 1)
===============

Base URL: ``https://my.shorten-url.com/api/v1``

API uses Bearer authorisation tokens to authorise the user. In order to use the API you will need to generate your API key and use it as a token. This can be done in your account, API Keys section. 

API uses ``GET``, ``POST``, ``PATCH`` and ``DELETE`` methods. If you are unable to use ``PATCH`` and ``DELETE`` methods due to network restrictions then send request using ``POST`` method and add ``_method`` field with required method name to root of each request.

`Postman <https://www.postman.com/>`_ desktop application json collection with samples of all API requests is available for download `here <https://shorten-url.com/files/shorten-url-v1.postman_collection.zip>`_. Download, unzip and import to Postman. You will need to generate your own API key and set it as a Bearer authorisation token on the collection level. Some of the requests uses collection level variables for certain object (group, link, etc) IDs. Replace them with your own object IDs. 

----------
System API
----------

System API conatins requests to do a system related functions e.g. ping API host and retrieve miscellaneous data dictionaries.

system: echo
^^^^^^^^^^^^

System echo request. Returns API key user details. Can be used to test the connection and API key setup.

Sub-URL: ``/system/echo``

Method: ``GET``

system: link-types
^^^^^^^^^^^^^^^^^^

Get supported short link types e.g. link to a web page, phone number, email address, social profile, etc. Link type ID should be used to create new short links. Variable {data} in link type format will be replaced with actual user data when creating a new link.

Sub-URL: ``/system/link-types``

Method: ``GET``

system: domains
^^^^^^^^^^^^^^^

Get available public and user custom domains for short URLs. Variable {key} in domain format will be replaced with generated short URL key when creating a new link.

Sub-URL: ``/system/domains``

Method: ``GET``

system: countries
^^^^^^^^^^^^^^^^^

Get available countries and their codes. Country codes can be used in redirect rules and filters.

Sub-URL: ``/system/countries``

Method: ``GET``

system: languages
^^^^^^^^^^^^^^^^^

Get available browser languages and their codes. Language codes can be used in redirect rules and filters.

Sub-URL: ``/system/languages``

Method: ``GET``

system: os-families
^^^^^^^^^^^^^^^^^^^

Get available operating system names. Can be used in redirect rules and filters.

Sub-URL: ``/system/os-families``

Method: ``GET``

system: browser-families
^^^^^^^^^^^^^^^^^^^^^^^^

Get available browser names. Can be used in redirect rules and filters.

Sub-URL: ``/system/browser-families``

Method: ``GET``



----------
Groups API
----------

Link group actions, e.g. create, update and delete link groups.

groups: list
^^^^^^^^^^^^

Get list of current user link groups. Group ID should be used when creating new short link.

Sub-URL: ``/groups``

Method: ``GET``




---------
Links API
---------

Short link (short URLs) actions, e.g. create, update and delete links.


