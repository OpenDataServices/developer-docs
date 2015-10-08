Open Data Services Code
=======================

What is Open Data Services Code?
--------------------------------

Open Data Services Code is defined as code that the Open Data Services Team look after directly.

This may be custom code that has been written specifically to perform
tasks for Open Data Services, or it could be 'off the shelf' code that we need to
maintain and update in order for it to run smoothly. Some of it will be
standalone applications, some of it could be customisations to other
people's projects/code.

Some code directly powers projects/web applications. Other code may be
command line tools that, for example, process data locally, or that
are 'recipes' for API's such as for communicating with a CKAN API.

There may also be code that the Open Data Services team does not own, but makes a
commitment to contributing to. We should also bear this in mind when
talking about Open Data Services code.

It is important for Open Data Services to know which code it is responsible for
resourcing.

So which code are we talking about?
-----------------------------------

Generally Open Data Services Code can be found here:
https://github.com/opendataservices

There may be rare instances of code that have yet to make it into the
GitHub organisation account, but it is our desire and intention for all
Open Data Services code to be there.

Code Checklist
--------------

We have agreed a set of 'coding principles', which provide a framework
that allows us to check that our code is being well managed. As such we
are able to audit each project that we maintain against our Open Data Services Code
Checklist.

Managing Code
-------------

Since we are clear about which code is ours to nurture, and with a
framework in place against which we test the health of our code, we want
to make sure our code is:

-  transferable - i.e. it could easily be handed over, or new staff
   could quickly understand it.
-  sustainable - i.e. properly resourced, future proofed, planned.
-  well managed - i.e. our code is working for us.

The following lays out some detail about how the Open Data Services Team has
chosen to work in order to achieve this.

Our code should be public...
----------------------------

... and our development processes should be public. We use GitHub public
repositories to help us achieve this.

GitHub
------

GitHub provides a place to 'host' code within a well known structure,
with access to key tools for managing that code:

-  issues
-  milestones
-  version control

etc - most of the things an open source code project needs

External Testing Services
-------------------------

We use the following external services to test our code in various ways:

* [Travis](https://travis-ci.org/) - runs unit tests every time a commit is made
* [Coveralls](https://coveralls.io/) - checks the coverage of those unit tests
* [Requires.io](https://requires.io) (Python specific) - tests to see whether the Python moudles listed in requirements.txt are up to date 
* [Landscape](https://landscape.io/) (Python specific) - calculates the quality of the code using static analysis, and tracks this over time

A public link to the results of each of these service can be found at the top of the README of each covered project.

Domains
-------

Open Data Services Code often needs to be deployed on a web address.
We try to make sensible choices based on past experience of working on 
projects with multiple domains.
Preferably we should be using subdomains.

### Why subdomains?

When it comes to putting our work on the web we have a choice of
using subdirectories, subdomains, or a new domain.

The problem with subdirectories (e.g. /validator, /query) won't work
well as different applications need different hosting requirements.
We're always going to need to 'point' at other servers. Subdirectories
could proxy (but this is not good) or redirect (also not really very
good) to other URLs.

The problem with domains is that applications and services can end up in
many different places and therefore hard to find. New domains can be
useful to distance applications from a certain domain if needed.

Licensing
---------

Open Data Services Code should be appropriately licensed.

Licences should be 'open' to allow re-use. The choice of licence is
something to be discussed for each project.

Documentation licensing is also important.

Branding
--------

Open Data Services has a coherent policy on branding, but often our work 
is done with and for other people, where their brand needs to be taken into
account. 

Projects should try to establish branding requirements and identify existing
brand assets early in a project's lifecycle.

Communicating
-------------

The Open Data Services Team needs to talk about the development of code
within the team, with other developers, bug reporters, and users of the
software.

Internally we need to talk about our code, projects, tasks, bugs, etc -
we may use third party services e.g. google group, or install third
party tools that we manage in order to do this (e.g. trac).

Current communication options with other audiences are via:

-  via GitHub 'issues'
-  support tickets to code@opendataservices.coop

Workplans
---------

Each piece of code should have a workplan. This should be carried out
via GitHub in the form of milestones and issues, wherever possible,
keeping development, bugs etc in the public domain.

