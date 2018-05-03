# git

## How we use git

In general each repository has:
* a `master` branch - and this is deployed on a dev site
* a `live`  branch which is fast-forward merged to update to the current master when it's ready to go live - this is deployed on the live site
* feature branches - most of the work should be done on these. In general these should be free of merge commits (rebased onto master instead of merging master in) and squashed (e.g. `rebase -i master`) into usefully sized commits.

When merging from a feature branch into master, the "Create a merge commit" strategy should be used.

More specific information about the branches in a repository should be in the CONTRIBUTING.md file in each repository. Merges should be performed or overseen by the person listed in CONTRIBUTING.md.

### Issues
We use #issueno to reference a GitHub issue from a commit (or OpenDataServices/reponame#issueno to reference an issue from another repository). Where a commit relates to one issue we use [#issueno] at the start of the commit messages to make it easier to scan by eye what issues commits relate to. We generally don't use "fixes #issueno" in order to leave closing issues until it's been checked that they're "Done"


### Temporary Branches
In general having temporary commits on temporary branches is better than using git stash. It's harder to lose your work this way, and they can also be pushed to the server. `tmp-some_name` is our current ad hoc naming convention for temporary branches. If you have a temporary commit you can update it using  `git commit --amend -a --date="`date``

### Branches or Forks?
We tend to work on branches within the repo in the OpenDataServices (or other relevant repository), rather than in personal forks, as this allows us all to take advantage of the same TravisCI setup etc. (Obviously external contributors will generally not have permissions for this, so will use their personal forks instead.).

## git tips

Although we expect our devs to have a good understanding/experience of 
using git, we may work on repos with other members of the team. Very 
often these members have some git basics - e.g. cloning, pulling, 
pushing commiting etc., but there may be some useful intermediate tips 
we want to collect - e.g. the different ways of identifying a commit 
- tags, branches, HEAD~2, hash, short hash 0 for use with the git diff 
etc.

### Push to 2 remotes at once 

http://stackoverflow.com/questions/14290113/git-pushing-code-to-two-remotes#answer-14290145

`git remote set-url --add`

### git blame a diff

See https://github.com/dmnd/git-diff-blame and http://stackoverflow.com/questions/5098256/git-blame-prior-commits

## Flow chart of steps if you mess up git commits

http://justinhileman.info/article/git-pretty/

### git blame a diff

See: https://github.com/dmnd/git-diff-blame and http://stackoverflow.com/questions/5098256/git-blame-prior-commits

### tig

tig is a curses (interactive CLI) git history browser - it's quite a nice middleground between the basic git commands, and firing up some sort of gui.

`tig --all` is particularly useful, which shows all commits, not just ones in the branch you're currently on.


