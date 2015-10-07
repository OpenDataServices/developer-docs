Open Data Services Code Checklist
=================================

About
-----

Our code checklist is based on a set of principles that provide a
framework against which code projects can be measured.

It may help to read each item as a question (that we should know the
answer to).

E.g. Is this 'our' code? Is it on our server? Does it have a licence?
etc.

The creation of this checklist allows us to:

-  communicate with new team members, external contractors, and other
   developers, about the way we do things.
-  allows us to audit current projects to find and fix gaps.
-  allows us to test new work against the framework to make sure all the
   bases are covered.

Each code repository in our [GitHub account](https://github.com/opendataservices/) 
should have a CHECKLIST.rst file

The checklist
-------------

### 1. We should know which code is 'ours'

Generally Open Data Services Code can be found here: https://github.com/opendataservices

There may be rare instances of code that have yet to make it into the
GitHub organisation account, but it is our desire and intention for all
Open Data Services code to be there.

### 2. All code should have a lead person identified

This makes it easy for others to work out who they might need to talk to.
This could be a project manager who does not actually code themselves.
In that case a code lead, who is ultimately responsible for merges, etc,
should be indentified. This responsibility may be delegated, but generally 
they are the only one to push to important branches such as master/live.

### 3. Our projects/code should be appropriately branded

### 4. Each piece of code should have a document, a roadmap, and estimate of resources, and a licence

Generally we're probably using a open source or free software compatible
licence.

There will usually be discussion as to whether or not we use a
permissive or copyleft licence.

### 5. We should be confident that updates to our code will not break existing functionality

Deployment of new features, especially in feature rich environments, or
of new website configurations has the potential to mess up existing
data, layouts, functionality.

Writing tests is one way of checking that large application are still
doing what they are supposed to be doing.

Does this mean everything should have a suite of tests? Probably!

### 6. It should make sense in the way people access our tools/code

Essentially the domains we use to host applications should make sense.

Code should be kept in one place e.g. GitHub organisation

### 7. Our code should be on our servers

As opposed to, for example, a developers personal server.

We should be able to monitor the performance of those servers.

We should be able to monitor the performance of the software.

### 8. Status of the software should be indicated in the deployments

For example, much of our code is deployed on development servers. 
Some of it is actively shared (i.e. we email people links, talk about
it openly), other stuff is thrown up for testing, but may still be
discoverable. It should be clear to visitors as to the status of that
software (e.g. they are using a development version of the software). 
Moreover, we may be deploying software/service that are considered
pre-Alpha, Alpha, Beta, properly stable etc..

### 9. We should know how our code is being used - logs!

Are we gathering and making use of:

- server analytics

- piwik analytics

- built in loggers

### 10. Our code will need to adapt with schema changes and changes to external systems upon which it relies

If, for example, standard schema, or apis we rely on change then our code
should also change.

When creating code these dependencies should factored into the design
and upkeep of the software.

### 11. Developers should be able to find useful resources and help easily

Developers within the existing team, externally and for anyone that
joins the team.

### 12. Each project should clearly describe how other developers can get involved

Each repository in GitHub should have a CONTRIBUTING.md document

### 13. We should be able to communicate with the users of our code

This could be by:

- technical blog

- messages

- email

### 14. Users should be able to communicate with us about our code

There should be pathways for

- technical users/queries

- non-technical users/queries

### 15. We should protect our users privacy

For example:

- good password security

- delete data that we don't need to keep

### 16. We should be clear about how we work with contractors

For example:

- systems we use

- licensing

### 17. If our code works with open data, have we considered how it will work as the datasets grow, both in terms of individual file size and as a corpus?

We should be aware that it is hard to  estimate the size of data we can
expect to see in e.g. 3, 6, 12 months time.

### 18. Our code should be secure

When relying on external code (e.g. wordpress) - we should be on an
alert list, we should update as soon as possible where necessary.

We should assess our own code for vulnerability.

### 19. We should know that our deployed code is working properly

For example, this could mean monitoring that the application is 'up', using
services like Uptime Robot, and we should know that cron jobs have run.

### 20. Our code should be simple to deploy and update

When creating an application, consideration of the ease of deployment, 
including upgrades should be considered. 

### 21. Are we using any other tools to help us monitor our code?

For example, linking into webhooks or services such as Travis

### 22. Is this code language aware?

Can it handle unicode correctly?
Does it need to handle translations and display text in differnet scripts?

### 23. Our code/projects should be in version control and present links to issue trackers and source code

Usually this would be in our [GitHub account](https://github.com/opendataservices/).

Code in development, where possible should also be in our GitHub
account.

If code is speculative, potentially sensitive, or has just not been
given the green light our current practice is to build it in private or
in personal developers own online repositories (GitHub, BitBucket, etc).

### 24. Does our code perform under load?

We should know that our code can handle expected load / file sizes - 
and fails gracefully e.g. for large files.
 
### 25. Is our code accessible

Wherever possible, we should support browsers without javascript  
See: http://kryogenix.org/code/browser/everyonehasjs.html)
