# Git

## Update commit dates

On your feature branch, commit whenever you want. Right before doing a pull request/merge, run this command to set all the commit dates to now:

`git rebase origin/master --exec "git commit --amend --reset-author --no-edit"`

and then this to override the remote commits for your branch:

`git push --force`

To change to a specific date:

`git rebase origin/master --exec "git commit --amend --date="Fri Oct 31 14:00 1975 +0100" --no-edit"`
