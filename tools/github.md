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

We use GitHub's protected Branches feature for the master and live 
branches of CoVE

This means it is not possible to push directly to those branches - 
tests must pass on Travis before code can go in. If you try you get:

    ! [remote rejected] master -> master (protected branch hook declined)

A 'fastforward' will merge into master commits that have already passed 
- it's not necessary to use GitHub's merge interfaces.

We intend to set this up for all our live branches, and most of our 
master branches on our code repositories.
