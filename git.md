# Git

## new branch with current changes

`git checkout -b <new-branch>`

From [Move existing, uncommitted work to a new branch in Git](https://stackoverflow.com/questions/1394797/)

## unstage a single, not-yet-committed file from the staging area

`git reset HEAD -- <file>`

From <https://stackoverflow.com/a/1505968>

## Abandon everything local, including existing commits, just go back to (eg) origin/master

`git reset --hard origin/master`

From <https://stackoverflow.com/a/5097495/384316>

> [use git reset] to move back to where the origin is.  
> Doing a `git revert` makes *new* commits to remove *old* commits in a way that keeps everyone's history sane.

## delete/remove an unpushed commit, but keep the files from that commit

`git reset --soft HEAD~1`

In the above case, the files will now remain in place.

To remove the commit and also delete the files, run:

`git reset --hard HEAD~1`