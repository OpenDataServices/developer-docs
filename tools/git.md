# git

## How we use git

* Our workflow has some similarities to, but is not gitflow
* Working on feature branches, and rebasing/squashing these (rebase -i) 
to give a useful clean, usefully broken down view of history. 
(including rebasing on master rather than meging master in, if 
possible)
* Using [#issueno] rather than fixes #issueno in order to leave 
closing issues until it's been checked that they're "Done"

Also maybe:

* Committing tmp commits to tmp branches as an alternative to git stash

## git tips

Although we expect our devs to have a good understanding/experience of 
using git, we may work on repos with other members of the team. Very 
often these members have some git basics - e.g. cloning, pulling, 
pushing commiting etc., but there may be some useful intermediate tips 
we want to collect - e.g. the different ways of identifying a commit 
- tags, branches, HEAD~2, hash, short hash 0 for use with the git diff 
etc.

### git blame a diff

See: https://github.com/dmnd/git-diff-blame and http://stackoverflow.com/questions/5098256/git-blame-prior-commits

### tig

tig is a curses (interactive CLI) git history browser - it's quite a nice middleground between the basic git commands, and firing up some sort of gui.

`tig --all` is particularly useful, which shows all commits, not just ones in the branch you're currently on.


