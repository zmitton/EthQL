Adding SQL as a side DB while continuing regular levelDB + trie stuff



file: database.go
=================

NewLDBDatabase
--------------
reimplemented it to create a sql DB as well

put
---

get
---

delete
------

close
-----

batch?
------

file: node.go
=============

OpenDatabase
------------

file: service.go
================

OpenDatabase
------------

file: unknown
=============
There is a function for switching heads. We need to shim inside this and mark any orphaned data in the DB as such. Its the only way to determine it is no longer relevant(deleted). Note: all tables will need an indexed field (blockhash) specifying the blockhash it was last updated or creted or something. would work for tx/r not sure about state yet.






