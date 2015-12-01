.. |br| raw:: html

   <br />

.. |tab| raw:: html

   <span style="min-width: 5em">&nbsp;</span>

.. |small| raw:: html

   <span style="font-size: 0.8em">

.. |x-small| raw:: html

   <span style="font-size: 0.7em">

.. |xx-small| raw:: html

   <span style="font-size: 0.6em">

Kinto
#####

Lightweight JSON storage HTTP service made for synchronisation.

----

Key Features
============

* Simple diff-based synchronisation APIs
* CDN friendly
* Dev friendly
* Comes with an ecosystem

  - online-first JS lib - Kinto.js (**landed in Firefox**)
  - Python lib for servers (AMO, etc.)
  - admin web app
  - Ops-friendly !

* Data Signing (*)
* File storage (*)

----

Use Cases
=========

* Firefox continuous updates (ex: sec settings, amo blocklist)
* Offline-first JS apps (ex: Reading List, Firefox OS Sync)
* Manifest & Frontend for S3 (ex: Fennec "OTA")


----

Why not X ?
===========

* Firefox Sync
* PouchDB / CouchDB / Hoodie
* Firebase, Sparse
* RemoteStorage
* Balrog


----

Synchronisation API
===================

Diff-based::

    GET /data?_since=<timestamp>

    {
       "data": [
        {
          "id": "dc86afa9-a839-4ce1-ae02-3d538b75496f",
          "last_modified": 1430222877724,
          "name": "googlemail.com",
          "mode": "force-https",
          "pins": "google"
        },
        {
          "id": "11130c47-37a5-41f6-9112-32d46141804f",
          "deleted": true,
          "last_modified": 1430140411480
        }
      ]
    }


----

Timeline (PROD)
===============

- H1: OneCRL, AMO Blocklist, Fennect OTA
- H2: Your projects ?

----

**Talk to me**

