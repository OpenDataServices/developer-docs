Git and GitHub
==============


Temporary Branches
------------------

In general having temporary commits on temporary branches is better than using git stash. It's harder to lose your work this way, and they can also be pushed to the server.

Branches or Forks?
------------------

We tend to work on branches within the repo in the OpenDataServices (or other relevant repository), rather than in personal forks, as this allows us all to take advantage of the same TravisCI setup etc. (Obviously external contributors will generally not have permissions for this, so will use their personal forks instead.).


Commit Size
-----------

Git Commits should be [atomic](https://en.wikipedia.org/wiki/Atomic_commit#Revision_control); each commit should be self contained such that someone can check out a repository at any commit and have a working system; this allows the use of Git Bisect and makes it easy to look in the history for a change and see what else changed at the same time.

This does not mean that every pull request should only contain 1 commit - there may be cases where a pull request deals with several issues at once, and every issue is in a separate commit. Or a piece of work may be broken down into several stages, and every stage may be in it's own commit. But the number of commits in a pull request should generally be small, and each commit should have a message formatted as below and include any associated documentation and changelog changes.

Commit message format
---------------------

Git commit messages should follow a standard format and include links back to the issue/pull request/other.

This is based on the common format for Open Source GNU/Linux projects.

The subject line should contain a logical module identifier of the scope of the changes that uniquely identifies it in lower case and then a short sentence to describe the changes.

The logical module identifier is an Open Code List (ie there is no set list of values and it is up to the developer to pick an appropriate one. Look at existing ones in the same repository for some ideas.)

We use the full URL of issues instead of the shorthand (eg "#123") so that if commits are moved around between repositories, the links will not be broken.

```
Subject line:

<module submodule/file/some logical name to make it uniquely identifiable in the codebase>: <Change summary message>

Body:

<Longer message if needed to describe the change>
<Full URLs: github issues, pull requests if applicable>
```

Example -

```
tests: Add test blah to make sure blah-de blah doesn’t regress

This adds a test case to prevent the regression in the blah module loader by loading some sample data.
Fixes issue https://github.com/example/issue/123
```

### Real world examples

Some real examples:

In Flatten tool, commit 0ed440e33ac084a5d19af8192b77433f9c821e0a is:

```
Drop Python 2 support
https://github.com/OpenDataServices/flatten-tool/issues/299
```

This could be writen as:


```
pythonversions: Drop Python 2 support

As agreed and as Python 2 is now end-of-life, drop Python 2 support.
https://github.com/OpenDataServices/flatten-tool/issues/299
```

In Cove tool, commit c358ae02ac28544485478f65853394a280739015 is:

```
OCDS - Change to 1.1.4 and SSL
```

This could be writen as:

```
ocdsschema: Upgrade OCDS schema version and move standards site to SSL.

1.1.4 of schema has been released - set as latest version of 1.1 schema.
Standards site is now served by HTTPS - change URLs to that.
Upgrade Lib-cove-OCDS to 0.7.0
Update tests to pass under 1.1.4
```

### Git commit templates

Note that git has a commit template feature that can be configured to present you with a reminder. This needs to be configured by each developer. [To set this up on your machine, see here](https://medium.com/@alex.wasik/create-a-custom-git-commit-template-84468232a459). You can use the template below:

```
# <module submodule/file/some logical name to make it uniquely identifiable in the codebase>: <Change summary message>

# <Longer message if needed to describe the change>

# <Full URLs: github issues, pull requests if applicable>
```

WIP branches and pull requests
------------------------------

Git commits can be in any state on a WIP (Work In Progress) branch but they should be cleaned up and sorted out before being presented for review, as the git commits are one of the things the reviewer is reviewing.


Bringing a branch up to date with master
----------------------------------------

If you have a working branch that you need to bring up to date with master, you should do this by rebasing.
 
Do not do this by merging master into your branch.

Code Reviewers
--------------

It’s hard to create solid rules that could be automatically applied by a bot, or something similar. 
So in that way these could be thought of as guidelines, as there always may be some discussion about the best way to apply these to a particular situation.

But reviewers should feel empowered to push back, if they feel the commits on a pull request could be done better.

Merging a pull request into master
----------------------------------

In GitHub there are several different options you can select for the merge strategy to use when merging a pull request into master.

We normally use the Merge commits option.

However if: 

* it's a single commit and 
* there is no extra information or discussion in the pull request or the pull request is linked to in the commit

then it's ok to use the rebase option instead.

Email in commits
----------------

Anyone contributing to our GitHubs from the company should use their 
company email in their commits.

TODO How-to with old content steps?

GitHub's protected branches
---------------------------

We use GitHub's protected Branches feature for the master
branch of CoVE, and most of our repositories.

This means it is not possible to push directly to those branches - 
tests must pass on Travis before code can go in. If you try you get:

    ! [remote rejected] master -> master (protected branch hook declined)


GitHub Settings
---------------

These our are normal settings, but they may be different in special cases.

Turn On the "Require pull request reviews before merging" setting.

Turn On the "Dismiss stale pull request approvals when new commits are pushed" setting. 

(We do this because otherwise someone could get approval, and then add a commit that makes large changes to the work. This protects us from honest mistakes more than malicious activity.)

Turn On the "Require status checks to pass before merging" setting.

Turn On the "Include administrators" setting.

