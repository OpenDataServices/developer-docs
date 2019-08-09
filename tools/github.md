# GitHub

Anyone contributing to our GitHubs from the company should use their 
ompany email in their commits.

To set this up:

* Login to GitHub
* Edit profile to add company email address
* Edit 'Notifications' to send notifications from the Open Data 
Services organisation to your company email
* Set your email on each local repo you use:
* To check email: git config user.email
* To set new: git config user.email <new email address>


## GitHub's protected branches

We use GitHub's protected Branches feature for the master
branch of CoVE, and most of our repositories.

This means it is not possible to push directly to those branches - 
tests must pass on Travis before code can go in. If you try you get:

    ! [remote rejected] master -> master (protected branch hook declined)

A 'fastforward' will merge into master commits that have already passed 
- it's not necessary to use GitHub's merge interfaces.

### Settings

These our are normal settings, but they may be different in special cases.

Turn On the "Require pull request reviews before merging" setting.

Turn On the "Dismiss stale pull request approvals when new commits are pushed" setting. 

(We do this because otherwise someone could get approval, and then add a commit that makes large changes to the work. This protects us from honest mistakes more than malicious activity.)

Turn On the "Require status checks to pass before merging" setting.

Turn On the "Include administrators" setting.

