Security considerations
=======================

When building tools for Open Data data there are several security issues to be aware
of.

XML
---

When parsing XML, you should be aware of entity based attacks.

User Supplied Files
-------------------

You should make sure that

* user supplied files aren't executable (e.g. if a PHP file is uploaded to the
  web directory)

Fetching Remote Files
^^^^^^^^^^^^^^^^^^^^^

Working with Open Data often involves fetching data from arbitrary URLs. You
should check

* The URLs don't begin file:// as this will expose data on the local filesystem
* The URLs don't point at any sensitive local HTTP(S) services


