About uPaaS
===========

uPaaS stands for "uWSGI Platform As A Service", think of it as a "poor man's PaaS".
uWSGI itself provides tons of features and uPaaS jobs is to add layer of management on top of it, creating simple, organized and secure way of managing web application deployments.

Features
--------

Currently uPaaS is still in early stages of development so only core features are implemented, but it is designed to provide:

* resource sharing without conflicts - deploy high number of web apps on single box without creating messy environment
* automated scalability - when application is under high load uPaaS will quickly add new nodes
* built in statistics - pretty graphs for every application out of the box
* monitoring and self-repair - uPaaS will constantly check if everything is running and it will try to fix itself when needed
* simple deployments - just do ``git push`` and uPaaS will take care of the reset (with git post-receive hook)

Components
----------

Database
~~~~~~~~

MongoDB is used to store all data, it provides easy to use replication and provides HA features out of the box.

Router nodes
~~~~~~~~~~~~

Routers are load balancers using uWSGI in FastRouter mode.

Backend nodes
~~~~~~~~~~~~~

Backends are running uPaaS admin web UI and task worker processes.

Notes
~~~~~

uPaaS is still under heavy develoment, many features are missing or incomplete.
