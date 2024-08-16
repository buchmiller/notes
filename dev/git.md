# Git

## Update commit dates

See <https://graphite.dev/guides/git-commit-date#changing-commit-dates>

On your feature branch, commit whenever you want. Right before doing a pull request/merge, run this command to set all the commit dates to now:

`git rebase origin/master --exec "git commit --amend --no-edit --date=now"`

(requires at least Git v2.1.4)

and then this to override the remote commits for your branch:

`git push --force`

To change to a specific date:

`git rebase origin/master --exec "git commit --amend --no-edit --date="Fri Oct 31 14:00 1975 +0100""`
